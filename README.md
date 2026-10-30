# Repository Template

[![License](https://img.shields.io/github/license/bruzit/template)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/bruzit/template)](https://github.com/bruzit/template/commits)
[![MegaLinter](https://github.com/bruzit/template/actions/workflows/megalinter.yaml/badge.svg)](https://github.com/bruzit/template/actions/workflows/megalinter.yaml)
[![Semantic Release](https://github.com/bruzit/template/actions/workflows/semantic-release.yaml/badge.svg)](https://github.com/bruzit/template/actions/workflows/semantic-release.yaml)

<!-- Badges: license, last commit, then one GitHub workflow badge per required workflow in pipeline order: linting, formatting, verification, unit tests, integration tests, end-to-end tests, release, deployment. -->

Purpose of the project in one sentence or one short paragraph.

**This repository:**

Repository template for BruzIT projects: MegaLinter and semantic-release callers, release configuration, license and README skeleton.

## Features

<!-- Optional: delete when empty. -->

Feature list or key capabilities; subsections as needed.

**This repository:**

- README outline with required and optional sections.
- MegaLinter on pull requests and weekly: [`.mega-linter.yaml`](.mega-linter.yaml), with markdownlint [`.markdownlint.yaml`](.markdownlint.yaml) and zizmor [`zizmor.yaml`](zizmor.yaml) configurations.
- semantic-release from Conventional Commits ([`.releaserc.yaml`](.releaserc.yaml)): version, changelog and GitHub release.

## Requirements

<!-- Optional: delete when empty. -->

Platforms, tools, dependencies, and versions needed.

**This repository:**

- Platform: GitHub Actions.
- Dependency: [BruzIT GitHub Actions and Workflows](https://github.com/bruzit/github-actions-and-workflows).

## Installation and Setup

How to install and set up the project, step by step.

**This repository:**

1. Create the repository from this template, by hand ("Use this template") or as code with [BruzIT GitHub Organization as Code](https://github.com/bruzit/github-organization-as-code), which can also manage its settings, rulesets, environments and secrets.
2. Set up the GitHub Apps and environments, provisioned by BruzIT GitHub Organization as Code:
   - `release`: semantic-release ([BruzIT GitHub Actions and Workflows: Use Semantic Release Action](https://github.com/bruzit/github-actions-and-workflows#use-semantic-release-action)).
   - `autofix`: MegaLinter fixes, `GH_AUTOFIX_APP_ID` variable and `GH_AUTOFIX_APP_PEM_FILE` secret ([BruzIT GitHub Actions and Workflows: Use MegaLinter Workflow](https://github.com/bruzit/github-actions-and-workflows#use-megalinter-workflow)); without it, MegaLinter only reports.
3. Tag the initial commit `v0.0.0`, so the first release is `0.x` instead of `1.0.0` ([`.releaserc.yaml`](.releaserc.yaml) keeps breaking changes on minor):

   ```shell
   git tag v0.0.0 "$(git rev-list --max-parents=0 HEAD)" && git push origin v0.0.0
   ```

4. Make it yours:
   - In every section, replace the general line and the **This repository:** block with your project's content.
   - Make the first sentence of the description match the repository's GitHub description.
   - Search and replace `bruzit/template` in the badge URLs; add a workflow badge per required workflow in pipeline order.
   - Delete empty optional sections and the HTML comments.

## Usage

Common tasks with minimal examples.

**This repository:**

Copy this outline; replace each section's content (Installation and Setup, step 4).

## Maintenance

<!-- Optional: delete when empty. -->

How to keep it updated and healthy: updates, upgrades, backup and restore, uninstall.

**This repository:**

- Bump the `@v0` refs on a new major of [BruzIT GitHub Actions and Workflows](https://github.com/bruzit/github-actions-and-workflows).
- Keep this README aligned with the outline.

## Support

Where to ask for help and report problems; for paid products, the service level.

**This repository:**

Community, best effort; [open a GitHub issue](../../issues).

## Development

<!-- Optional: delete when empty. -->

Local development environment and project layout.

**This repository:**

Run MegaLinter locally: [BruzIT GitHub Actions and Workflows: Linting](https://github.com/bruzit/github-actions-and-workflows#linting).

## Testing

<!-- Optional: delete when empty. -->

How to run checks and tests.

**This repository:**

No unit tests; MegaLinter only (Integration and Deployment).

## Integration and Deployment

<!-- Optional: delete when empty. -->

Workflows that integrate, release, and deploy the project.

**This repository:**

| Workflow                                                            | Trigger                          | Purpose                                                                      |
|---------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------|
| [MegaLinter](.github/workflows/megalinter.yaml)                     | Pull request                     | Lint changed files; required check `Required (MegaLinter)`                   |
| [MegaLinter Scheduled](.github/workflows/megalinter-scheduled.yaml) | Weekly, Monday 06:00 UTC; manual | Lint the whole codebase                                                      |
| [Semantic Release](.github/workflows/semantic-release.yaml)         | Push to `main`                   | Version, changelog and GitHub release via the shared semantic-release action |

## Contributing

How to propose changes.

**This repository:**

Open a pull request to `main`. Commits follow the [Conventional Commits 1.0.0 specification](https://www.conventionalcommits.org/en/v1.0.0/), from which semantic-release sets versions and the changelog automatically.

## License and Copyright

License and copyright holder.

**This repository:**

MIT License: [`LICENSE`](LICENSE)  
Copyright © 2026 Martin Bružina

## References

<!-- Optional: delete when empty. -->

Related projects and documentation.

**This repository:**

- [BruzIT GitHub Actions and Workflows](https://github.com/bruzit/github-actions-and-workflows)
- [BruzIT GitHub Organization as Code](https://github.com/bruzit/github-organization-as-code)

## Stats

<!-- Optional: delete when empty. -->

Repository figures; stable products add selected usage or customer figures.

**This repository:**

| Metric           | Badges                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commits          | [![Commits total](https://img.shields.io/github/commit-activity/t/bruzit/template?label=commits%20total)](https://github.com/bruzit/template/commits/main)                                                                                                                                                                                                                                                                             |
| Issues           | [![Issues open](https://img.shields.io/github/issues/bruzit/template?label=issues)](https://github.com/bruzit/template/issues) [![Issues total](https://img.shields.io/github/issues-search?query=repo%3Abruzit%2Ftemplate%20is%3Aissue&label=issues%20total)](https://github.com/bruzit/template/issues?q=is%3Aissue)                                                                                                                 |
| Pull requests    | [![Pull requests open, not draft](https://img.shields.io/github/issues-search?query=repo%3Abruzit%2Ftemplate%20is%3Apr%20is%3Aopen%20draft%3Afalse&label=PRs%20open)](https://github.com/bruzit/template/pulls?q=is%3Apr+is%3Aopen+draft%3Afalse) [![Pull requests total](https://img.shields.io/github/issues-search?query=repo%3Abruzit%2Ftemplate%20is%3Apr&label=PRs%20total)](https://github.com/bruzit/template/pulls?q=is%3Apr) |
| Checks on `main` | [![Checks on main](https://img.shields.io/github/check-runs/bruzit/template/main?label=checks%20%28main%29)](https://github.com/bruzit/template/actions?query=branch%3Amain)                                                                                                                                                                                                                                                           |
| Releases         | [![Latest release](https://img.shields.io/github/v/release/bruzit/template)](https://github.com/bruzit/template/releases/latest) [![Commits since latest release](https://img.shields.io/github/commits-since/bruzit/template/latest)](https://github.com/bruzit/template/releases)                                                                                                                                                    |
| Community        | [![Stargazers](https://img.shields.io/github/stars/bruzit/template)](https://github.com/bruzit/template/stargazers) [![Forks](https://img.shields.io/github/forks/bruzit/template)](https://github.com/bruzit/template/forks) [![Contributors](https://img.shields.io/github/contributors/bruzit/template)](https://github.com/bruzit/template/graphs/contributors)                                                                    |
