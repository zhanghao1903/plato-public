# Release Status

This repository currently publishes the Plato `1.1-beta` macOS Apple Silicon
local beta release.

## Latest Public Release

| Field | Value |
|---|---|
| Version | `1.1-beta` |
| Platform | macOS |
| Architecture | Apple Silicon / `arm64` |
| Asset | `Plato-1.1-beta-macos-arm64.dmg` |
| Runtime | Bundled Python sidecar candidate |
| Signed | No |
| Notarized | No |

Download:

- [Plato-1.1-beta-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1-beta/Plato-1.1-beta-macos-arm64.dmg)

Checksum:

```text
39e70ce0d356e4d05bd02280402480fe6fb3aa49bdbe072fd387fbe51fd562ec  Plato-1.1-beta-macos-arm64.dmg
```

Metadata:

- [manifest.json](../../releases/1.1-beta/manifest.json)
- [SHA256SUMS](../../releases/1.1-beta/SHA256SUMS)
- [Human-readable release notes](../releases/1.1-beta.md)

## What This Release Is

This release is a local beta for early evaluation of the Plato desktop
experience and the Product 1.1 inspection foundations.

It is intended to make the product loop visible:

```text
goal -> task structure -> execution -> result -> audit
```

It also exposes these Product 1.1 additions:

- token usage analytics for local sessions and workspace summaries;
- precision file tool foundations for line-range reads, search, guarded edits,
  append operations, and changed-line evidence;
- workspace inspection for git status, structured diffs, and file viewer paths.

## What This Release Is Not

This release is not:

- signed or notarized for normal macOS distribution;
- a source-code mirror;
- a public marketplace for agents or skills;
- a promise that every roadmap item in the docs is available in `1.1-beta`.
- a signed, notarized, auto-updating, or marketplace-ready release.

## Opening On macOS

Because this release is unsigned and non-notarized, macOS Gatekeeper may block
normal opening.

See [macOS local release usage](../usage/macos-local-release.md) for the
recommended local opening path.

For data, logs, and local workspace safety notes, see
[Privacy and safety](../security/privacy-and-safety.md).
