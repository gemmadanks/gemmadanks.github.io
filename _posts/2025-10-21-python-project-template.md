---
title: "My opinionated template for new Python projects"
date: 2025-10-21 T12:54:30
categories:
  - tutorials
tags:
  - setup
  - github
  - python
  - ci
  - tools
excerpt_separator: <!--more-->
---

Over the years, I've experimented with different tools and learnt about various best practices in software engineering. These things are always in flux and so, in order to have a central place for collecting and updating the tools and practices I've found most useful for Python projects, and to help streamline starting future projects, I've created an opinionated template on GitHub that anyone can use:

- [Python Project Template (GitHub)](https://github.com/gemmadanks/python-project-template)

Using this template will save time doing the initial set up and avoid decision fatigue and analysis paralysis that can consume time and energy which is better spent getting stuck straight into the software development process.

This post briefly describes some of the decisions involved in setting up a modern Python project -- starting with a minimal package, then adding tools that help ensure code quality and finally automating workflows for continuous integration and delivery.

The template's [README](https://github.com/gemmadanks/python-project-template/blob/main/README.md) and [Architectural Decision Records (ADRs)](https://github.com/gemmadanks/python-project-template/blob/main/docs/architecture/adr/index.md) have up-to-date details on the choices I've made.

## A minimal Python package

Setting up a minimal Python project is fairly straightforward. You need a [`pyproject.toml`](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/) file (to specify dependencies and configuration for packaging), a licence file, a README file and the actual Python source code and tests. You can follow [a tutorial from the python packaging site](https://packaging.python.org/en/latest/tutorials/packaging-projects/) to learn more details. You'd end up with the following directory structure:

```
my_project_name/
├── LICENSE
├── pyproject.toml
├── README.md
├── src/
│   └── my_package/
│       ├── __init__.py
│       └── example.py
└── tests/
    └── test_example.py
```

It is also useful to include a CITATION.cff file so that others can easily cite your work and a directory for Jupyter notebooks that you can use as tutorials or demos of your project.

There are already some decisions you have to make when completing the steps to set up this basic structure:

1. What licence to choose (e.g. MIT, BSD 3-Clause)
2. What build backend to use (e.g. hatchling, uv_build)
3. What Python versions to support (e.g. >=3.11)

## Documenting your project

There are several tools (e.g. sphinx, MkDocs) available to help you generate html documentation for your project. You also need to decide where to host the documentation (e.g. GitHub pages or Read The Docs), and how best to communicate the rationale for your design choices to your future self or other developers (e.g. using ADRs).

## Tools to make developing Python code easier

There are also many tools that make your life easier when developing your project. The main ones are: 

- Linters to check your code and flag any issues (e.g. pylint, flake8, ruff)
- Formatters to ensure consistent code style (e.g. black, ruff)
- Testing frameworks to run your tests (e.g. pytest)
- Dependency managers (e.g. Poetry, uv, pipenv) to install and resolve other packages you want to use in your project (including the linters and formatters)

## Automating your workflows

Running your tests as well as the linters and formatters requires several steps that you may or may not remember to do when you commit your changes or merge to your main branch. Several ways exist to automate this, including:

- A Justfile or Makefile -- allows you to create short commands to make it easier to run common tasks.
- Pre-commit hooks -- scripts that run automatically whenever you try to commit a change and can include running your linter and formatter and checking your dependencies are in sync.
- GitHub workflows (or equivalent on other platforms) -- these can be configured to run automatically on GitHub whenever you push your commits or open a merge request. They can run your pre-commit hooks, tests, publish your package, generate test coverage reports and build your documentation. This forms a key part of continuous integration, which is a practice that helps ensure new changes don't introduce errors.
- Dependabot (from GitHub) -- automates updating dependencies.

## Releasing your software

Creating a release of your project allows you to tag, package, document and distribute a specific version to a wider audience. There are a number of different approaches for when and how to release, and how to label each version. This can also be automated for continuous delivery (e.g. via release-please and using conventional commits and semantic versioning).

## Managing your project

Templates for GitHub issues and pull requests allow you to standardise processes when managing a project. This is useful when collaborating with others and when working alone (your future self may not remember all the details of a bug you found last week or a feature idea you had a few months ago and templates will help you document these in a more thorough and structured way).

## Using the template

Follow the instructions in the template's README if you'd like to use it -- and feel free to leave a comment here or open an issue in the repository if you have any ideas for improvements.
