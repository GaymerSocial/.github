# Changelog

All notable changes to this repo are documented here.

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
