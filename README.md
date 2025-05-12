# Devcontainer

[![GitHub stars](https://img.shields.io/github/stars/jmcombs/devcontainer)](https://github.com/jmcombs/devcontainer/stargazers) ![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/jmcombs/devcontainer/build-and-publish.yml?logo=github)
[![GitHub issues](https://img.shields.io/github/issues/jmcombs/devcontainer)](https://github.com/jmcombs/devcontainer/issues)

A collection of [Development Container](https://containers.dev/) definitions for creating consistent, reproducible development environments. This repository provides pre-configured `devcontainer` images to streamline setting up development environments in tools like Visual Studio Code, GitHub Codespaces, or other container-based IDEs.

## About

A **development container** is a running [Docker](https://www.docker.com) container with a well-defined tool/runtime stack and its prerequisites. It allows you to use a container as a full-featured development environment which can be used to run an application, to separate tools, libraries, or runtimes needed for working with a codebase, and to aid in continuous integration and testing.

This repository contains a set of **dev container images** which are Docker images built with [dev container features](https://github.com/devcontainers/features).

## Contents

- [`src`](src) - Contains reusable dev container images.
- [`scripts`](scripts) - Contains utility scripts, including `generate-docs.js` for updating documentation links in this README.

## Available Dev Containers

Below is a list of available Dev Container definitions in this repository:

| Name          | Description                                                  | Base Image                            | Documentation                              |
| --------      | ------------------------------------------------------------ | ------------------------------------- | ------------------------------------------ |
| `python`      | Python 3.x environment with common tools (e.g., pip, pylint) | `ghcr.io/jmcombs/devcontainer:python` | [Python Docs](src/python/README.md)        |
| `node`        | Node.js environment with npm/yarn and VS Code extensions     | `ghcr.io/jmcombs/devcontainer:node`   | [Node Docs](src/node/README.md)            |
| `base-ubuntu` | Base Ubuntu 22.04 image with essential tools                 | `ghcr.io/jmcombs/devcontainer:base-ubuntu` | [Base Ubuntu Docs](src/base-ubuntu/README.md) |

## Usage

To use these dev containers in Visual Studio Code or GitHub Codespaces:

1. **Open your project** in VS Code or Codespaces.
2. **Select the dev container**: Use the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P` on macOS) and choose `Dev Containers: Reopen in Container`.
3. **Choose a container definition**: Select one of the available dev containers from this repository (e.g., `python` or `node`).
4. **Start coding**: Your environment will be set up with all the necessary tools and extensions.

For more detailed instructions, refer to the [Dev Containers documentation](https://code.visualstudio.com/docs/remote/containers).
