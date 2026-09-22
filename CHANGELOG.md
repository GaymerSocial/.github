# Changelog

All notable changes to this repo are documented here.

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
