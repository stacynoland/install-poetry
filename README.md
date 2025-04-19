![Poetry Package Manager](https://img.shields.io/endpoint?url=https%3A%2F%2Fpython-poetry.org%2Fbadge%2Fv0.json)
![Python Versions](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12%20%7C%203.13-blue?logo=python&logoColor=yellow)
[![GitHub Release](https://img.shields.io/github/v/release/stacynoland/install-poetry?label=Current%20Release)](https://github.com/stacynoland/install-poetry/releases)
[![Tests](https://github.com/stacynoland/install-poetry/actions/workflows/test.yml/badge.svg)](https://github.com/stacynoland/install-poetry/actions/workflows/test.yml)

# Install Poetry Official

This action installs Poetry, a dependency management tool for Python projects, using the official installer and adds it to the runner's `$GITHUB_PATH`, so you can invoke the`poetry` command directly in your workflow.

See the Poetry official installer documentation for details on this installation method:
https://python-poetry.org/docs/#installing-with-the-official-installer

## Usage

Poetry currently supports Python 3.9 or later. This action assumes a Poetry supported version of Python is installed.

Basic usage of the action inside a workflow:

```yaml
name: Install Poetry
uses: stacynoland/install-poetry@v1
```

This will install the latest version of Poetry.

You can use the optional `poetry-version` input to specify `preview` or a specific version number to install.

```yaml
name: Install Poetry
uses: stacynoland/install-poetry@v1
with:
  poetry-version: preview
```
or

```yaml
name: Install Poetry
uses: stacynoland/install-poetry@v1
with:
  poetry-version: 1.8.0
```