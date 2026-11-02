# clean-login-browser (private)

Slim Camoufox runtime builds used by the **clean-login** plugin (magpie plugin `@magpie-community/page-clean-login`).

This is not a public mirror of Camoufox. It is private on purpose: release assets of a private repository are not anonymously downloadable.

## What is here

Release `browser-v158.0.1-beta.41-slim.1`:

- `camoufox-slim-win-x86_64-158.0.1-beta.41.zip` — 176,170,139 bytes, sha256 `07bfbe8148b7b2b6a520074b6766b4aac493c6f2364e4d6af21c31b453026dd1`
- `camoufox-slim-win-x86_64-158.0.1-beta.41.zip.sha256`
- `inventory.json`
- `build-report.md`

## Provenance

Built from upstream `daijro/camoufox` release `v158.0.1-beta.41` (Windows x86_64), commit `c3ad3bf2c3c6e93225aa6587246c8b70f9314664`, `source_digest 27f9630cbeec9f70adc9abcd9e3cd5ce`.

`867` entries = all `866` non-`fonts/` entries + exactly one font file (`fonts/TwemojiMozilla.ttf`). The 1513 bundled font faces (2056.6 MiB) are removed: a Windows identity activates only that single file from `fonts/` (upstream `font-hijacker.patch`, `IsStockBundledFontFile`), so page text renders from the host's DirectWrite fonts. Rendering was verified byte-identical to the full bundle (1104/1104 family fields + 36/36 generic fields).

Upstream publishes no sha256 for its own zip; the checksum above is ours. `sourceZipSha256` in `inventory.json` is our local measurement, not an upstream value.

## Pending

- Release asset upload needs a token with access to this repository (the current fine-grained PAT cannot see it).
- Before shipping to end users this repository must become public, or the asset must move to a public host: private-repo release assets cannot be downloaded anonymously.
