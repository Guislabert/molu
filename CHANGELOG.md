# Changelog / 更新日志

All notable changes to **molu** are documented here. Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), versioned with [SemVer 2.0.0](https://semver.org/).

## [1.1.0]

### Changed
- **License: CC BY-NC 4.0 → Apache-2.0** for the engine code and for the `SKILL.md` methodology. CC BY-NC is not an OSI-approved license: it forbids commercial use, so the repo was source-available, not open source. Apache-2.0 keeps the commercial worries covered (patent grant + trademark carve-out) without the non-commercial restriction.
- **License boundary made explicit**: `molu/*/references/` holds verbatim excerpts of published articles owned by their original authors. Those files are now formally carved out of the license instead of being lumped under one ambiguous label, and `NOTICE` says to delete them before mirroring or republishing.
- Every `SKILL.md` front-matter `license:` field restated as `Apache-2.0` plus the `references/` carve-out.
- README badges (EN / zh-CN) now read `License: Apache-2.0` and link to `LICENSE`.

### Added
- `LICENSE` — full Apache License 2.0 text. The README's `[License](LICENSE)` link used to 404 because no license file existed.
- `NOTICE` — attribution, the `references/` carve-out, the `molu` / 墨炉 trademark carve-out (§6), and the corpus provenance.

### Fixed
- Broken `LICENSE` link in the English README acknowledgements section.

## [1.0.3]

### Added
- **install.sh topology self-check**: when the resolved target directory is the same as the source directory (e.g. `~/.claude/skills` is itself a symlink to the repo), symlink writing is **skipped** with a hint to use `install.sh agents` for a physical install — preventing `molu-*` self-referencing dead links.

### Fixed
- Prevent `molu-*` self-referencing dead links when the skills directory is an in-place symlink.

## [1.0.2]

### Changed
- Module names stay as clean `molu-<module>` (no numbering).
- Panel ordering is alphabetical by agent; pipeline order is marked `①→⑪` at the start of each module description.
- Descriptions tightened to short phrases.
- Badges trimmed to **Version / Skills / License**.

## [1.0.1]

### Changed
- `/molu` popup-list display optimized: numbered names `molu-01` → `molu-11`, version badge `1.0.1`.

## [1.0.0]

### Added
- **公开发布层 (public release layer)**: 11 modules of methodology + `kb.py` data layer + `install.sh`.
- No verbatim corpus committed.

See [Releases](https://github.com/Guislabert/molu/releases) for authoritative tagged versions.