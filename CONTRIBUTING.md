<p align="center">
  <img src="https://global.media.robo.st/logo.png" width="300" alt="RoboStux">
</p>

# Contributing to RoboStux

RoboStux is split across five repos, each with its own `CONTRIBUTING.md`:

- **[DiscordBot](https://github.com/RoboStux/DiscordBot)** - the Discord bot itself
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

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.
