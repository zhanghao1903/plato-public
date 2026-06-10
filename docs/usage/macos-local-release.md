# macOS Local Release Usage

This page explains how to use the current public macOS local release candidate.

## Download

Download the latest public asset:

- [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg)

Verify the checksum if needed:

```text
34bc9a24dbf29c8ba5ebdeb1d92a4428d55e791562596e4303734b493fdfb212  Plato-0.1.0-macos-arm64.dmg
```

## Open

The `0.1.0` release is unsigned and non-notarized.

macOS may block a normal double-click open. For local evaluation, mount the DMG
and use Finder's contextual Open action if Gatekeeper blocks the first launch.

## Status Caveats

- The app is a local release candidate.
- The package includes a bundled Python sidecar runtime candidate.
- Signing and notarization are not complete for this release.
- The public repository hosts release metadata and public docs, not private
  source code or internal diagnostics.

## Troubleshooting

If the app does not open:

1. Confirm you downloaded the macOS Apple Silicon asset.
2. Confirm the checksum matches the published SHA256 value.
3. Try opening from Finder with the contextual Open action.
4. Check [Release status](../product/release-status.md) for current caveats.
