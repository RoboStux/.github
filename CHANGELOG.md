# Changelog

All notable changes to this project will be documented in this file.

Each release lists its changes under Added, Changed, Fixed, Removed, Security and Deprecated, in that order. This
project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.11.06-1

### Added

- `.github/workflows/ci.yml`, which runs `tests/version.sh` on every push to `main` and `test` and on every pull request

### Changed

- Work happens on the new `test` branch and reaches `main` only through a pull request, reviewed and merged by Leo; releases are committed and tagged on `test`. `CONTRIBUTING.md` has a Branches section, the README's Versioning section says so, and `commit.sh`/`commit.bat` say to push `test`

## v26.11.06

### Added

- The organisation profile and README list **errorpages** (RoboStux's branded nginx error pages) and **robostux.github.io** (the GitHub Pages redirect), which were missing
- The profile's links line now has **Add RoboStux to your server** (robo.st/invite), **Support server** (robo.st/support) and **Status** (status.robo.st) next to the website, and the README links status.robo.st
- The README's Contents section covers `generateMetrics.yml`, the release scripts and `tests/version.sh`

### Changed

- The repo tables now link the Website and Status repos to their sites (robo.st, status.robo.st) and use each repo's current description, e.g. Lavalink is a Lavalink v3 client library for discord.py 2.x
- `CONTRIBUTING.md` lists all eight repos instead of "five repos", and asks for the tables to be updated whenever a repo is added or retired
- This changelog's intro states the section order (Added, Changed, Fixed, Removed, Security, Deprecated) instead of pointing to Keep a Changelog

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.1.0
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## [1.1.0] - 2026-09-30

### Added
- A **Service Status** section in `profile/README.md` with the live status badge and a status table (each service's group, status, uptime and response time, linking to [status.robo.st](https://status.robo.st)), kept up to date hourly by the new `.github/workflows/status.yml` using GitHup's `readme` mode and the data in `RoboStux/Status`

## [1.0.0] - 2026-09-29

The first release of the RoboStux organisation profile under a fresh version history. Earlier versions and their tags have been retired.

### Added
- The organisation profile (`profile/README.md`), README and `CONTRIBUTING.md`, with the table of RoboStux's repositories: DiscordBot, Commons, Lavalink, Update, Website and Status
- The `generateMetrics.yml` workflow and the "Our Activity" metrics image, published to the `metrics` branch
- `commit.sh`/`commit.bat` release scripts that read `VERSION.md` and tag `vX.Y.Z`
