# Source provenance

**`possessed-source` is the live builder repository. `possessed` is the curated showcase.** The Base44 builder writes to [possessed-source](https://github.com/indicaindependent/possessed-source) and syncs to its `main` branch, so that repository is always the latest game. This repository is a hand-maintained showcase of it, with its own README, MIT licence and artwork.

## Imported revision

The game files were copied byte for byte from builder revision `1c44b75acd4b5e9418ab9f5f20147116054bbb23` (pushed 2026-10-31 22:08 UTC). The previous showcase import was `868a738bcb5145d2c7aae263b676ac9eb78a8231` (2026-10-30).

Changes since `868a738b`:

- `6be7c45e` Fix audio playback bugs and add background music (new `src/lib/possessed/music.js`, procedural soundtrack).
- `81733b67` Refine mobile UI and typography across 16 files.
- `3cac8859` Further UI refinement, including design tokens in `src/index.css`.
- `1c44b75a` GhostMeter tweak.

Application code, tests, assets, dependency manifests, lockfile and connector configuration are copied without modification. The builder's own README is not copied; this repository keeps its curated one.

This repository is not a sync target. Changes here do not edit or deploy the live game.

## Verification

- Clean install with `npm ci`.
- 54 tests passed across 6 files with `npx vitest@3 run`.
- Production frontend compiled with `npm run build`.
- Application files verified by Git blob hash against the source revision before publication.
- Safety scan of the source found no keys, tokens or environment files.
- Build warning: app ID is not configured for this standalone build. A successful compile is not a live deployment or a multiplayer test.

No dependency upgrades were run during this import.
