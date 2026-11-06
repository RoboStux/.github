<p align="center">
  <img src="https://global.media.robo.st/logo.png" width="300" alt="RoboStux">
</p>

# RoboStux .github

### *One Bot, Multiple Features, Every Server!*

GitHub organisation profile for [RoboStux](https://github.com/RoboStux).

Website: https://robo.st  
Status: https://status.robo.st  
Repository: https://github.com/RoboStux/.github

## Contents

- **`profile/README.md`** — the public-facing organisation profile shown on
  the [RoboStux organisation page](https://github.com/RoboStux) on GitHub, including the
  **Service Status** table between the `<!-- githup:start -->` / `<!-- githup:end -->`
  markers (don't edit inside them).
- **`.github/workflows/status.yml`** — hourly, checks out
  [RoboStux/Status](https://github.com/RoboStux/Status) and runs
  [GitHup](https://githup.stux.group)'s `readme` mode to refresh that table, committing as
  `github-actions[bot]` only when it changed.
- **`.github/workflows/generateMetrics.yml`** — daily, builds the "Our Activity" image and
  publishes it to the `metrics` branch.
- **`commit.sh`** / **`commit.bat`** and **`tests/version.sh`** — the release scripts and the
  version check (see [CONTRIBUTING.md](CONTRIBUTING.md)).

## Repositories

| Repo | Description |
|------|-------------|
| [DiscordBot](https://github.com/RoboStux/DiscordBot) | The RoboStux Discord bot: music, moderation, trivia and stream alerts, fully modular |
| [Website](https://github.com/RoboStux/Website) | The RoboStux website, [robo.st](https://robo.st) |
| [Status](https://github.com/RoboStux/Status) | RoboStux Status, [status.robo.st](https://status.robo.st): uptime monitor and status page, powered by [GitHup](https://githup.stux.group) |
| [Commons](https://github.com/RoboStux/Commons) | Common utilities shared across RoboStux's projects |
| [Lavalink](https://github.com/RoboStux/Lavalink) | A Lavalink v3 client library for discord.py 2.x, built on asyncio and aiohttp |
| [Update](https://github.com/RoboStux/Update) | A wrapper that lets the bot update itself while running |
| [errorpages](https://github.com/RoboStux/errorpages) | RoboStux's branded error pages for nginx |
| [robostux.github.io](https://github.com/RoboStux/robostux.github.io) | Redirects robostux.github.io to this organisation |

### Our Activity

<div align="center">
  <img width="512" src="https://raw.githubusercontent.com/RoboStux/.github/metrics/stats.svg">
</div>

---

*Written & Maintained by <img src="https://global.media.stuxie.dev/icon.png" height="14" alt="StuxieDev" valign="middle"> [StuxieDev](https://stuxie.dev).*

*[A StuxieDev Project](https://projects.stuxie.dev)*

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.
