---
name: plato-public-release
description: Use when packaging a private Plato main-branch build and publishing a public GitHub release with public-safe notes, manifests, checksums, and release assets.
---

# Plato Public Release

Use this skill for public Plato desktop releases. The public repository is a
documentation and asset surface, not a source-code mirror.

## Preconditions

- Work from the private source repo `main` branch unless the user names another branch.
- Pull/fetch first and verify the source worktree is clean except intended release fixes.
- Confirm the public repo checkout is on `main` and clean before editing release docs.
- Confirm the release version, target platform, architecture, and feature list.
- For beta versions, publish the GitHub release as a pre-release.

## Version Rules

- Use `releaseVersion` for the public label and DMG name, for example `1.1-beta`.
- Use `packageVersion` for npm-compatible package metadata, for example `1.1.0-beta`.
- Use `bundleVersion` for macOS plist fields, for example `1.1.0`.
- Build with the explicit version flag:

```bash
VERSION=1.1-beta
npm run electron:package:installer -- --release-version "${VERSION}"
```

Do not patch generated app files by hand for version changes. If a version field
is wrong, fix the packaging script and rebuild.

## Build And Validate

Run focused checks before publishing:

```bash
VERSION=1.1-beta
DMG_PATH="frontend/dist-electron-installer/Plato-${VERSION}-macos-arm64.dmg"
npm run test -- sidecarProcess smokeRunner platoRuntime App
uv run pytest tests/test_multi_workspace_sidecar.py tests/test_workspace_inspection_api.py
npm run electron:smoke:launcher
npm run electron:check:release-assets -- --package-dir ./dist-electron-launcher
hdiutil verify "${DMG_PATH}"
npm run electron:smoke:installer -- --skip-package --installer "${DMG_PATH}"
```

If time or environment blocks a check, record the exact gap in the release notes.

## Public Repo Updates

For each release, update or create:

- `docs/releases/<version>.md`
- `docs/zh/releases/<version>.md` when Chinese docs are maintained
- `releases/<version>/manifest.json`
- `releases/<version>/SHA256SUMS`
- current release links in README, quickstart, FAQ, release status, and safety docs

The release notes must include:

- the download link;
- SHA256 checksum;
- added features;
- validation commands or validation summary;
- known caveats such as unsigned, not notarized, platform limits, and source-mirror limits.

## Public Safety Checks

- Do not publish source code, private paths, raw logs, API keys, provider secrets, or workspace data.
- Prefer renderer-safe labels over raw local filesystem paths in screenshots and docs.
- Keep unreleased roadmap language clearly marked as preview, planned, or conceptual.
- Keep generated release assets out of git unless they are intentionally small metadata files.

## Publish

After docs and metadata are committed and pushed to the public repo:

```bash
VERSION=1.1-beta
DMG_PATH="/path/to/private/source/frontend/dist-electron-installer/Plato-${VERSION}-macos-arm64.dmg"
gh release create "v${VERSION}" "${DMG_PATH}" \
  --repo zhanghao1903/plato-public \
  --target main \
  --title "Plato ${VERSION}" \
  --notes-file "docs/releases/${VERSION}.md" \
  --prerelease
```

Use `--prerelease` for beta builds. After publishing, verify GitHub's asset
digest, size, tag, target branch, and release URL against `manifest.json`.
