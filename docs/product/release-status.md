# Release Status

This repository publishes two public macOS Apple Silicon channels:

| Channel | Current version | Role | Release notes |
|---|---:|---|---|
| Stable | `0.1.0` | Conservative public baseline for the task-first product loop. | [0.1.0 notes](../releases/0.1.0.md) |
| Beta | `1.1-beta` | Latest Product 1.1 inspection foundations. | [1.1-beta notes](../releases/1.1-beta.md) |

For a feature-by-feature comparison, see [Public versions](versions.md).

## Latest Beta Release

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
bdf1d719546c84569dae4c6610ed9a609acb77c971d00a938ff59c6510caa6e1  Plato-1.1-beta-macos-arm64.dmg
```

Metadata:

- [manifest.json](../../releases/1.1-beta/manifest.json)
- [SHA256SUMS](../../releases/1.1-beta/SHA256SUMS)
- [Human-readable release notes](../releases/1.1-beta.md)

## What The Beta Release Is

The beta channel is for early evaluation of the Plato desktop experience and
the Product 1.1 inspection foundations.

It is intended to make the product loop visible:

```text
goal -> task structure -> execution -> result -> audit
```

Compared with stable `0.1.0`, beta `1.1-beta` adds:

- [token usage analytics](../releases/1.1-beta.md#token-usage-analytics) for
  local sessions and workspace summaries;
- [precision file tool foundations](../releases/1.1-beta.md#precision-file-tools)
  for line-range reads, search, guarded edits, append operations, and
  changed-line evidence;
- [workspace inspection](../architecture/trust-and-audit.md#workspace-inspection-direction)
  for git status, structured diffs, and file viewer paths.

## Stable Baseline

The stable channel is currently `0.1.0`. It is the conservative public baseline
for reviewing Plato's task-first model, visible task plan, ASK direction, Main
Page control surface, and Audit Page trust surface.

Stable is still an unsigned, non-notarized local release. It is stable relative
to the public beta channel, not a signed app-store-quality distribution.

## What Public Releases Are Not

The public channels are not:

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
