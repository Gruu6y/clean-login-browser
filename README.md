# clean-login-browser

Slim Camoufox runtime builds used by the **clean-login** plugin (magpie plugin `@magpie-community/page-clean-login`).

This is not a public mirror of Camoufox. It hosts exactly one build: the slim Windows x86_64 runtime the plugin downloads by default.

## Release `browser-v158.0.1-beta.41-slim.1` (prerelease)

- `camoufox-slim-win-x86_64-158.0.1-beta.41.zip` — 176,170,139 bytes
- sha256 `07bfbe8148b7b2b6a520074b6766b4aac493c6f2364e4d6af21c31b453026dd1`
- plus `.sha256`, `inventory.json` and `build-report.md`

## How the plugin consumes it

The plugin's default download source is this release's zip URL, and it verifies the download against that sha256 before it unpacks anything. `MAGPIE_CLEAN_LOGIN_BROWSER_URL` overrides the source; an override only counts as verified when `MAGPIE_CLEAN_LOGIN_BROWSER_SHA256` is set as well.

## Measured

| | |
|---|---:|
| download | 176,170,139 bytes (168.0 MiB) |
| installed | 432,910,039 bytes (412.8 MiB) |
| first-run install (download + verify + unpack) | 22 s |

Measured 2026-11-03 through the plugin's own installer against this release.

## Provenance

Built from upstream `daijro/camoufox` `v158.0.1-beta.41` (Windows x86_64), commit `c3ad3bf2c3c6e93225aa6587246c8b70f9314664`, `source_digest 27f9630cbeec9f70adc9abcd9e3cd5ce`. All 1513 bundled font faces are removed except the single file a Windows identity activates; the details, the entry inventory and the rendering-equivalence evidence are in `build-report.md` and `inventory.json`. Upstream publishes no sha256 for its own zip — the checksum above is ours.
