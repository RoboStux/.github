# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
