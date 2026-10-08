# Project Name

One-sentence purpose.

## Setup

Delete this section once the repository is set up.

1. Create the repository from this template, by hand ("Use this template") or as code with [GitHub Organization as Code](https://github.com/bruzit/github-organization-as-code), which can also manage its settings, rulesets, environments and secrets.
2. Set up releases: [`.github/workflows/semantic-release.yaml`](.github/workflows/semantic-release.yaml) runs the [Semantic Release](https://github.com/bruzit/github-actions-and-workflows#use-semantic-release-action) action, which needs a GitHub App and a `release` environment; follow its README.
3. Tag the initial commit `v0.0.0`, so the first release is `0.x` instead of `1.0.0` ([`.releaserc.yaml`](.releaserc.yaml) keeps breaking changes on minor):

   ```shell
   git tag v0.0.0 "$(git rev-list --max-parents=0 HEAD)" && git push origin v0.0.0
   ```

4. Replace the title, purpose and Usage below.

## Usage

## Copyright and Licensing

[MIT License](LICENSE)  
Copyright © 2026 Martin Bružina
