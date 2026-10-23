# Changelog

All notable changes to this repo are documented here.

Since v26.10.23 this project uses [Date Versioning](https://datevers.ing) (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used Semantic Versioning.

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.8
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps
- The CI version check accepts `YY.MM.DD` and `YY.MM.DD-N` instead of `MAJOR.MINOR.PATCH`

## v1.0.8

### Added
- GitHub Actions CI (`.github/workflows/ci.yml`) checking on every push and pull request against `main` that the key repo files exist, workflow YAML is valid, and `VERSION.md` has a matching `CHANGELOG.md` release heading
- Release workflow (`.github/workflows/release.yml`) that publishes a GitHub Release whenever `commit.sh`'s `vX.Y.Z` tag is pushed, using the matching `CHANGELOG.md` section as the notes

## v1.0.7

### Added
- `generateMetrics.yml` workflow, matching every sibling org's `.github` repo — was missing entirely here, leaving `GaymerSocial/.github/metrics/stats.svg` broken wherever it's embedded (including on StuxGroup's own profile README family grid).
- An "Our Activity" `stats.svg` embed in `profile/README.md`, matching the per-org pattern used elsewhere (e.g. Stuxedo's profile README).

### Note
- The workflow needs an org-level `METRICS_TOKEN` Actions secret to actually run — every sibling org has one, but GaymerSocial's org currently has zero secrets configured. This needs to be added manually via GitHub org settings (Settings → Secrets and variables → Actions) before the workflow will succeed.

## v1.0.6

### Fixed
- `README.md`'s copyright line named `Stux.Group` (a brand, not a legal entity) — corrected to `Stux Group Ltd`.

## v1.0.5

### Added
- Bluesky and LinkedIn badges (`bsky.app/profile/stux.group`, `linkedin.com/company/stuxgroup`) in a new "Connect with Us!" section in `profile/README.md`, alongside a GitHub followers badge.

## v1.0.4

### Changed
- `CONTRIBUTING.md`'s "is a Stux.Group project" line now reads "is a Stux.Group Service", linking to `https://services.stux.group`.

## v1.0.3

### Fixed
- `README.md` and `profile/README.md`'s Stux.Group footer icon reference had a duplicated `/global/` path segment (`https://global.media.stux.group/global/icon.png`), a 404 — corrected to `https://global.media.stux.group/icon.png`

## v1.0.2

### Changed
- `assets/logo.png`/`assets/icon.png` moved from being vendored locally in this repo to the shared CDN at `https://global.media.gaymer.social/logo.png` / `/icon.png` (the same file was previously duplicated across all four GaymerSocial repos) — `README.md` and `profile/README.md`'s header logo references (the latter previously a `raw.githubusercontent.com` link, since org profile READMEs can't use relative paths) were updated accordingly

## v1.0.1

### Changed
- `README.md` and `profile/README.md`'s footer brand-attribution block updated to the new two-line format (Built & Maintained by Gaymer.Social, Hosted by Stuxedo / Gaymer.Social is a part of the Stux.Group brand of businesses), replacing the older single-line disclaimer

## v1.0.0

### Added
- Initial project scaffolding: `README.md`, `CHANGELOG.md`, `VERSION.md`, `CONTRIBUTING.md`, `commit.sh`/`commit.bat`
- `assets/logo.png`/`assets/icon.png` — the real Gaymer.Social logo/icon, vendored locally for the README header
- `profile/README.md` — the public GaymerSocial org profile page (rendered at github.com/GaymerSocial), carrying the Gaymer.Social/Gaymer.Coffee discontinuation notice and a link to gaymer.social
