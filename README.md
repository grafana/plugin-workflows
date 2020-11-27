# Plugin workflows for GitHub Actions

[![License](https://img.shields.io/github/license/grafana/plugin-workflows)](LICENSE)
[![PRs welcome!](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contribute)

This repository contains a set of workflows for building, testing, and releasing Grafana plugins.

## Workflows

These workflow require no modifications for you to use. To use them for your plugin, create a `.github/workflows/` directory in the root directory of your plugin, and add the workflows to it.

- **ci.yml:** Build and test your plugin on every commit
- **release.yml:** Create a GitHub release with the packaged plugin as a release asset. **Requires that you [create an encrypted secret](https://docs.github.com/en/free-pro-team@latest/actions/reference/encrypted-secrets) for your GRAFANA_API_KEY.**
