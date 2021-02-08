# Plugin workflows for GitHub Actions

[![License](https://img.shields.io/github/license/grafana/plugin-workflows)](LICENSE)
[![PRs welcome!](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contribute)

This repository contains a set of workflows for building, testing, and releasing Grafana plugins.

These workflows require no modifications to use:

- Create a `.github/workflows` directory in the root directory of your plugin
- Add the workflows, e.g. `.github/workflows/ci.yml`.

## Workflows

- **ci.yml:** Build and test your plugin on every commit
- **release.yml:** Create a GitHub release with the packaged plugin as a release asset. **Requires that you [create an encrypted secret](https://docs.github.com/en/free-pro-team@latest/actions/reference/encrypted-secrets) for your `GRAFANA_API_KEY`.**

## Troubleshooting

### `error Command "sign" not found` when running `yarn sign`

Add the following script to your `package.json`:

```
"scripts": {
  "sign": "grafana-toolkit plugin:sign"
}
```
