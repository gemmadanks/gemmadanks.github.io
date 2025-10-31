---
title: "How to migrate from Poetry to uv"
date: 2025-10-27 T21:34:00
categories:
  - tutorials
tags:
  - setup
  - packaging
  - poetry
  - tools
  - uv
  - python
---

I have recently been working on a template for new Python projects and of the first decisions I had to make was which tool to use for packaging and dependency management. I initially chose [Poetry][poetry-docs] since I am already familiar with it: Poetry is a mature tool that is widely used and works well. But several people have recently recommended [uv][uv-docs] as an alternative so I decided to try it. This post documents the steps I had to take to switch from Poetry to uv.

- Read more about what decisions are involved in setting up a new Python project in [my post on the template][template-post]
- Check out [my template on GitHub][template-repo]
- Read the [ADR][adr-post] I created to [document the rationale for my decision to switch to uv][adr-002]

To summarise the outcome of my testing: **uv is extremely fast (it is written in rust), manages python versions in addition to dependencies and is likely to become the new standard so I am adopting it for my new projects**.

From a google search, I saw that there are tools to automate this migration (e.g. [migrate-to-uv][migrate-to-uv]) but for a simple Python repository there are not that many steps to do it manually so that is what I did.

I also had to make additional changes to use uv in my CI/CD (GitHub workflow) pipelines, readthedocs configuration, dependabot configuration, pre-commit hooks and just recipes and to get [release-please][release-please] (which I am using to automate releases) to bump the version number in the uv lock file. 

You can see the actual changes I made to some of the files in [this pull request][poetry-to-uv-pr].

## How to switch from Poetry to uv
I was using Poetry version 2.2.0 and switched to uv version 0.9.4.

### Pre-requisites
- A Python project managed using Poetry (with a pyproject.toml file [listing your dependencies][pyproject-deps])
- Access to a terminal

### Basic steps

1. Open a terminal and navigate to the root of your repository.
1. Create and switch to a new branch.
1. Delete the `poetry.lock` file:
```bash
rm poetry.lock
```
1. [Install uv][uv-install]:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
1. Check installation (should show usage details):
```bash
uv
```
1. Create a `uv.lock` file:
```bash
uv lock
```
1. Test uv run with a development tool in your repository (e.g. ruff, black, pytest):
```bash
uv run ruff check .
```
1. Change the build backend in `pyproject.toml` to `uv_build` (or use another [build system to suit your needs][build-system]):
```toml
[build-system]
requires = ["uv-build>=0"]    # or pin a version
build-backend = "uv_build"
```
1. Add a module name for the build (replace `package_name` with the name of your package):
```toml
[tool.uv.build-backend]
module-name = "package_name"
module-root = ""
```
1. Commit your changes.

### Additional steps

These will be different for different repositories. Test that everything works as expected after each change.

#### Change `poetry run` to `uv run`

Change all `poetry run` commands to `uv run` in files that use them, e.g.:

- `justfile` (see [my template's justfile][justfile] for examples)
- `makefile`
- `devcontainer.json`
- GitHub workflows
- Pre-commit configuration file

#### Add a pre-commit hook for uv sync

You can add a pre-commit hook from uv to check that the `uv.lock` is up-to-date:

{% highlight yaml %}
repos:
  - repo: https://github.com/astral-sh/uv-pre-commit
    # uv version.
    rev: 0.9.4
    hooks:
      - id: uv-lock
{% endhighlight %}

#### Use uv in your Dockerfile

If you use a Dockerfile, you can install uv by adding the following:

```docker
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/uv
```

Then install your dependencies using uv instead of poetry:

```bash
uv sync --all-groups
```

#### Use uv in GitHub workflows

To use uv in GitHub workflows, replace your poetry setup with the following:

{% highlight yaml %}
- name: Install uv
  uses: astral-sh/setup-uv@v7
  with:
    version: "0.9.4"
    enable-cache: true

- name: Install dependencies
  run: uv sync --all-groups
{% endhighlight %}

#### Update dependabot config file

If you use dependabot, update the config file:

{% highlight yaml %}
- package-ecosystem: "uv"
{% endhighlight %}

#### Edit release-please configuration

If you use release-please, add `uv.lock` as an extra file in the release-please-config.json so that the version number of your package listed there will be bumped:

{% highlight json %}
"extra-files": [
    {
      "jsonpath": "$.package[?(@.name.value=='package-name')].version",
      "path": "uv.lock",
      "type": "toml"
    }
  ]
{% endhighlight %}

#### Edit Read the Docs configuration

If you are using Read the Docs to host your documentation, edit your `readthedocs.yaml` to [use uv to install docs dependencies][rtd-uv]:

{% highlight yaml %}
jobs:
  pre_create_environment:
      - asdf plugin add uv
      - asdf install uv latest
      - asdf global uv latest
  create_environment:
      - uv venv "${READTHEDOCS_VIRTUALENV_PATH}"
  install:
      - UV_PROJECT_ENVIRONMENT="${READTHEDOCS_VIRTUALENV_PATH}" uv sync --frozen --group docs
{% endhighlight %}

#### Update your README

Update your project `README` with instructions for how to use `uv` and optionally add the uv badge ([![uv](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/uv/main/assets/badge/v0.json)](https://github.com/astral-sh/uv)
):
```
[![uv](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/uv/main/assets/badge/v0.json)](https://github.com/astral-sh/uv)
```

[adr-post]: https://open-research.gemmadanks.com/planning/architectural-decision-records/
[adr-002]: https://open-research.gemmadanks.com/python-project-template/architecture/adr/002-manage-dependencies-with-uv/
[build-system]: https://packaging.python.org/en/latest/tutorials/packaging-projects/#choosing-a-build-backend
[justfile]: https://github.com/gemmadanks/python-project-template/blob/85438ed145b77c64328e22a7b9a044684f6dc6af/justfile
[migrate-to-uv]: https://github.com/mkniewallner/migrate-to-uv
[poetry-docs]: https://python-poetry.org/
[poetry-to-uv-pr]: https://github.com/gemmadanks/python-project-template/pull/16/files
[poetry-to-uv-adr]: https://open-research.gemmadanks.com/python-project-template/architecture/adr/002-manage-dependencies-with-uv/
[pyproject-deps]: http://packaging.python.org/en/latest/guides/writing-pyproject-toml/#dependencies-and-requirements
[release-please]: https://github.com/googleapis/release-please
[rtd-uv]: https://docs.readthedocs.com/platform/stable/build-customization.html#install-dependencies-with-uv
[template-post]: https://open-research.gemmadanks.com/tutorials/python-project-template/
[template-repo]: https://github.com/gemmadanks/python-project-template
[uv-docs]: https://docs.astral.sh/uv/
[uv-install]: https://docs.astral.sh/uv/getting-started/installation/