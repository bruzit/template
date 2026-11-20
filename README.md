# Repository Template

[![License](https://img.shields.io/github/license/bruzit/template)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/bruzit/template)](https://github.com/bruzit/template/commits)
[![MegaLinter](https://github.com/bruzit/template/actions/workflows/megalinter.yaml/badge.svg)](https://github.com/bruzit/template/actions/workflows/megalinter.yaml)
[![Semantic Release](https://github.com/bruzit/template/actions/workflows/semantic-release.yaml/badge.svg)](https://github.com/bruzit/template/actions/workflows/semantic-release.yaml)

<!-- Badges: license, last commit, then one GitHub workflow badge per required workflow in pipeline order: linting, formatting, verification, unit tests, integration tests, end-to-end tests, release, deployment. -->

State the project's purpose in one sentence or one short paragraph.

**This repository:**

Repository template for BruzIT projects: MegaLinter and semantic-release callers, release configuration, license, security policy and README skeleton.

## Features

<!-- Optional: delete when empty. -->

List the features or key capabilities; add subsections as needed.

**This repository:**

- A README outline with required and optional sections.
- MegaLinter, one tool that runs many linters, checks every pull request and, weekly, the whole repository: [`.mega-linter.yaml`](.mega-linter.yaml). Linter configurations: markdownlint [`.markdownlint.yaml`](.markdownlint.yaml), zizmor (GitHub Actions security linter) [`zizmor.yaml`](zizmor.yaml).
- semantic-release reads the Conventional Commits and sets the version, changelog and GitHub release: [`.releaserc.yaml`](.releaserc.yaml).

## Requirements

<!-- Optional: delete when empty. -->

List the platforms, tools, dependencies, and versions needed.

**This repository:**

- Platform: GitHub Actions.
- Dependency: [BruzIT GitHub Actions and Workflows](https://github.com/bruzit/github-actions-and-workflows).

## Installation and Setup

Give every install and setup step, in order.

**This repository:**

1. Create the repository from this template: by hand (**Use this template**) or as code with [BruzIT GitHub Organization as Code](https://github.com/bruzit/github-organization-as-code), which can also manage its settings, rulesets, environments and secrets.
2. Set up the GitHub Apps and environments; BruzIT GitHub Organization as Code provisions them:
   - `release`: semantic-release. On its first run it tags the initial commit `v0.0.0`, so the first release is `0.x`, not `1.0.0` ([BruzIT GitHub Actions and Workflows: Use Semantic Release Action](https://github.com/bruzit/github-actions-and-workflows#use-semantic-release-action)).
   - `autofix`: MegaLinter fixes; needs the `GH_AUTOFIX_APP_ID` variable and the `GH_AUTOFIX_APP_PEM_FILE` secret ([BruzIT GitHub Actions and Workflows: Use MegaLinter Workflow](https://github.com/bruzit/github-actions-and-workflows#use-megalinter-workflow)). Without it, MegaLinter only reports.
3. Make it yours:
   - In every section, replace the general line and the **This repository:** block with your project's content.
   - Make the first sentence of the description match the repository's GitHub description.
   - Replace `bruzit/template` in the badge URLs; add one workflow badge per required workflow, in pipeline order.
   - Delete empty optional sections and the HTML comments.

## Usage

Show common tasks with minimal examples.

**This repository:**

Copy this outline and replace each section's content (Installation and Setup, step 3).

## Maintenance

<!-- Optional: delete when empty. -->

Describe how to keep the project updated and healthy: updates, upgrades, backup and restore, uninstall.

**This repository:**

- Bump the `@v0` refs when [BruzIT GitHub Actions and Workflows](https://github.com/bruzit/github-actions-and-workflows) ships a new major.
- Keep this README aligned with the outline.

## Support

Say where to ask for help and report problems; for paid products, state the service level.

**This repository:**

[Open a GitHub issue](../../issues). I answer best effort, as a community project.

## Development

<!-- Optional: delete when empty. -->

Describe the local development environment and project layout.

**This repository:**

Run MegaLinter locally: [BruzIT GitHub Actions and Workflows: Linting](https://github.com/bruzit/github-actions-and-workflows#linting).

## Testing

<!-- Optional: delete when empty. -->

Show how to run checks and tests.

**This repository:**

There are no unit tests; MegaLinter runs the checks (Integration and Deployment).

## Integration and Deployment

<!-- Optional: delete when empty. -->

List the workflows that integrate, release, and deploy the project.

**This repository:**

| Workflow                                                            | Trigger                          | Purpose                                                                      |
|---------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------|
| [MegaLinter](.github/workflows/megalinter.yaml)                     | Pull request                     | Lint changed files; required check `Required (MegaLinter)`                   |
| [MegaLinter Scheduled](.github/workflows/megalinter-scheduled.yaml) | Weekly, Monday 06:00 UTC; manual | Lint the whole codebase                                                      |
| [Semantic Release](.github/workflows/semantic-release.yaml)         | Push to `main`                   | Version, changelog and GitHub release via the shared semantic-release action |

## Contributing

Explain how to propose changes.

**This repository:**

Open a pull request to `main`. Write commits per the [Conventional Commits 1.0.0 specification](https://www.conventionalcommits.org/en/v1.0.0/); semantic-release sets the version and changelog from them.

## License and Copyright

State the license and copyright holder.

**This repository:**

MIT License: [`LICENSE`](LICENSE)  
Copyright © 2026 Martin Bružina

## References

<!-- Optional: delete when empty. -->

List related projects and documentation.

**This repository:**

- [BruzIT GitHub Actions and Workflows](https://github.com/bruzit/github-actions-and-workflows)
- [BruzIT GitHub Organization as Code](https://github.com/bruzit/github-organization-as-code)

## Stats

<!-- Optional: delete when empty. -->

Show repository figures; stable products add selected usage or customer figures.

**This repository:**

| Metric           | Badges                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commits          | [![Commits total](https://img.shields.io/github/commit-activity/t/bruzit/template?label=commits%20total)](https://github.com/bruzit/template/commits/main)                                                                                                                                                                                                                                                                             |
| Issues           | [![Issues open](https://img.shields.io/github/issues/bruzit/template?label=issues)](https://github.com/bruzit/template/issues) [![Issues total](https://img.shields.io/github/issues-search?query=repo%3Abruzit%2Ftemplate%20is%3Aissue&label=issues%20total)](https://github.com/bruzit/template/issues?q=is%3Aissue)                                                                                                                 |
| Pull requests    | [![Pull requests open, not draft](https://img.shields.io/github/issues-search?query=repo%3Abruzit%2Ftemplate%20is%3Apr%20is%3Aopen%20draft%3Afalse&label=PRs%20open)](https://github.com/bruzit/template/pulls?q=is%3Apr+is%3Aopen+draft%3Afalse) [![Pull requests total](https://img.shields.io/github/issues-search?query=repo%3Abruzit%2Ftemplate%20is%3Apr&label=PRs%20total)](https://github.com/bruzit/template/pulls?q=is%3Apr) |
| Checks on `main` | [![Checks on main](https://img.shields.io/github/check-runs/bruzit/template/main?label=checks%20%28main%29)](https://github.com/bruzit/template/actions?query=branch%3Amain)                                                                                                                                                                                                                                                           |
| Releases         | [![Latest release](https://img.shields.io/github/v/release/bruzit/template)](https://github.com/bruzit/template/releases/latest) [![Commits since latest release](https://img.shields.io/github/commits-since/bruzit/template/latest)](https://github.com/bruzit/template/releases)                                                                                                                                                    |
| Community        | [![Stargazers](https://img.shields.io/github/stars/bruzit/template)](https://github.com/bruzit/template/stargazers) [![Forks](https://img.shields.io/github/forks/bruzit/template)](https://github.com/bruzit/template/forks) [![Contributors](https://img.shields.io/github/contributors/bruzit/template)](https://github.com/bruzit/template/graphs/contributors)                                                                    |
