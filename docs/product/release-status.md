# Release Status

This repository publishes two public macOS Apple Silicon channels:

| Channel | Current version | Role | Release notes |
|---|---:|---|---|
| Stable | `1.1` | Current formal public Product 1.1 release. | [1.1 notes](../releases/1.1.md) |
| Beta | `1.1-beta` | Earlier Product 1.1 preview retained for comparison. | [1.1-beta notes](../releases/1.1-beta.md) |

The prior Product 1.0 public baseline was `0.1.0`; it remains available from
GitHub releases for historical comparison.

For a feature-by-feature comparison, see [Public versions](versions.md).

## Latest Stable Release

| Field | Value |
|---|---|
| Version | `1.1` |
| Platform | macOS |
| Architecture | Apple Silicon / `arm64` |
| Asset | `Plato-1.1-macos-arm64.dmg` |
| Runtime | Bundled Python sidecar |
| Signed | No |
| Notarized | No |
| Source commit | `8a766a96d7e3a78a60583318f6231475d312043e` |

Download:

- [Plato-1.1-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1/Plato-1.1-macos-arm64.dmg)

Checksum:

```text
fd9588592fcc8f0f04322dac8b84038bc3ebd713bdf68cf5a5b1cd4fd76e809e  Plato-1.1-macos-arm64.dmg
```

Metadata:

- [manifest.json](../../releases/1.1/manifest.json)
- [SHA256SUMS](../../releases/1.1/SHA256SUMS)
- [Human-readable release notes](../releases/1.1.md)

## What The Stable 1.1 Release Is

Stable `1.1` is the formal public release of the Product 1.1 local desktop
experience. Compared with the Product 1.0 public baseline `0.1.0`, it adds:

- Runtime Input Router and one routed input surface;
- durable Conversation / Activity history;
- read-only inquiry for no-effect questions;
- ASK and confirmation routing through Conversation;
- command-backed plan/task revision behavior;
- archived Plan access;
- token usage analytics;
- precision file tools;
- workspace inspection for git status, changed files, file viewer, and diff
  entry points;
- frontend interaction runtime improvements for submit responsiveness, focus,
  route return, overlay return, and scroll stability.

## Beta Channel

The beta channel currently points to `1.1-beta`. It is retained for reviewers
who need to compare the earlier Product 1.1 preview. New users should start with
Stable `1.1`.

## What Public Releases Are Not

The public channels are not:

- signed or notarized for normal macOS distribution;
- a source-code mirror;
- a public marketplace for agents or skills;
- a signed, notarized, auto-updating, or app-store-quality release;
- a guarantee that every roadmap item in the docs is available in every build.

## Opening On macOS

Because this release is unsigned and non-notarized, macOS Gatekeeper may block
normal opening.

See [macOS local release usage](../usage/macos-local-release.md) for the
recommended local opening path.

For data, logs, and local workspace safety notes, see
[Privacy and safety](../security/privacy-and-safety.md).
