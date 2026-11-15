<p align="center">
  <img src="https://global.media.robo.st/logo.png" width="300" alt="RoboStux">
</p>

# Contributing to RoboStux

RoboStux is split across these repos, each with its own `CONTRIBUTING.md`:

- **[DiscordBot](https://github.com/RoboStux/DiscordBot)** - the Discord bot itself
- **[Website](https://github.com/RoboStux/Website)** - the RoboStux website, robo.st
- **[Status](https://github.com/RoboStux/Status)** - RoboStux Status, status.robo.st
- **[Commons](https://github.com/RoboStux/Commons)** - shared utilities
- **[Lavalink](https://github.com/RoboStux/Lavalink)** - the Lavalink client library
- **[Update](https://github.com/RoboStux/Update)** - the self-update wrapper
- **[errorpages](https://github.com/RoboStux/errorpages)** - the branded nginx error pages
- **[robostux.github.io](https://github.com/RoboStux/robostux.github.io)** - the GitHub Pages redirect

Open your issue or PR on whichever of those the change actually belongs to.
This `.github` repo itself holds only the org profile
(`profile/README.md`), its workflows and org-wide defaults - contributions here are
typically fixes to those, or to files that fall back to this repo when a
target repo doesn't have its own (see GitHub's
[community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file-for-your-organization)).

## Branches and going live

- Work on `test`, or on a feature branch off it that's merged back into it. Releases are made on `test` too: `commit.sh`/`commit.bat` refuse to run on `staging` or `main`. Never push to `staging` or `main`
- `staging` is the last check before live: it changes only when a pull request from `test` into `staging` is merged
- `main` is what's live: it changes only when a pull request from `staging` into `main` is merged. Both pull requests need CI to pass and are reviewed and merged by Leo
- `main` is what GitHub shows on the organisation page; release commits and tags are made on `test` (`git push origin test --tags`) and go live once they've been through `staging` and its pull request into `main` is merged

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.
5. Push `test` with its tag (`git push origin test --tags`) and open a pull request into `staging` (`gh pr create --base staging --head test`). Once it's merged and staging checks out, open one from `staging` into `main` (`gh pr create --base main --head staging`).

When a repo is added to or retired from the organisation, update the repo tables in `profile/README.md` and `README.md`
and the list above in the same release.
