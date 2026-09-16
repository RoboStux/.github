<p align="center">
  <img src="https://media.robo.st/global/logo.png" width="300" alt="RoboStux">
</p>

# Contributing to RoboStux

RoboStux is split across five repos, each with its own `CONTRIBUTING.md`:

- **[Bot](https://github.com/RoboStux/Bot)** - the Discord bot itself
- **[Commons](https://github.com/RoboStux/Commons)** - shared utilities
- **[Lavalink](https://github.com/RoboStux/Lavalink)** - the Lavalink client library
- **[Update](https://github.com/RoboStux/Update)** - the self-update wrapper
- **[Website](https://github.com/RoboStux/Website)** - source for robo.st

Open your issue or PR on whichever of those the change actually belongs to.
This `.github` repo itself holds only the org profile
(`profile/README.md`) and org-wide defaults - contributions here are
typically fixes to those, or to files that fall back to this repo when a
target repo doesn't have its own (see GitHub's
[community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file-for-your-organization)).

## Versioning

Bump [`VERSION.md`](VERSION.md) and add a matching entry to
[`CHANGELOG.md`](CHANGELOG.md) in the same PR, following
[Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`),
independent of the other repos' own versions.
