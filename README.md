[![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)
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