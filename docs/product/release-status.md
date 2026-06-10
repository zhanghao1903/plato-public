# Release Status

This repository currently publishes the Plato `0.1.0` macOS Apple Silicon
local release candidate.

## Latest Public Release

| Field | Value |
|---|---|
| Version | `0.1.0` |
| Platform | macOS |
| Architecture | Apple Silicon / `arm64` |
| Asset | `Plato-0.1.0-macos-arm64.dmg` |
| Runtime | Bundled Python sidecar candidate |
| Signed | No |
| Notarized | No |

Download:

- [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg)

Checksum:

```text
34bc9a24dbf29c8ba5ebdeb1d92a4428d55e791562596e4303734b493fdfb212  Plato-0.1.0-macos-arm64.dmg
```

Metadata:

- [manifest.json](../../releases/0.1.0/manifest.json)
- [SHA256SUMS](../../releases/0.1.0/SHA256SUMS)

## What This Release Is

This release is a local release candidate for early evaluation of the Plato
desktop experience.

It is intended to make the product loop visible:

```text
goal -> task structure -> execution -> result -> audit
```

## What This Release Is Not

This release is not:

- signed or notarized for normal macOS distribution;
- a source-code mirror;
- a public marketplace for agents or skills;
- a promise that every roadmap item in the docs is available in `0.1.0`.
- a promise that workspace inspection screenshots represent an available
  `0.1.0` release feature.

## Opening On macOS

Because this release is unsigned and non-notarized, macOS Gatekeeper may block
normal opening.

See [macOS local release usage](../usage/macos-local-release.md) for the
recommended local opening path.
