# Source provenance

**`possessed-source` is the live builder repository. `possessed` is the curated showcase.** The Base44 builder writes to [possessed-source](https://github.com/indicaindependent/possessed-source) and syncs to its `main` branch, so that repository is always the latest game. This repository is a hand-maintained showcase of it, with its own README, MIT licence and artwork.

## Imported revision

The game files were copied byte for byte from builder revision `e52739d727fa81bac1bbf562e79c47fa6f0cacd7` (2026-11-01 00:07 UTC). The previous showcase import was `1c44b75acd4b5e9418ab9f5f20147116054bbb23` (2026-10-31), and before that `868a738bcb5145d2c7aae263b676ac9eb78a8231` (2026-10-30).

Changes since `1c44b75a`:

- `30756362` Autoplay audio and a home-screen sound toggle.
- `7f15cb2b` Ambient animation and sound on the home and waiting screens (creaks, pumpkin and room animation).
- `3f7a18a3` Fix overlapping music loops.
- `ada55379` Sound toggle behaviour and pill interaction.
- `e52739d7` Speaker icon on the sound toggle.

Earlier, since `868a738b`: background music (`6be7c45e`), mobile UI and typography (`81733b67`), design tokens in `src/index.css` (`3cac8859`) and a GhostMeter tweak (`1c44b75a`).

Application code, tests, assets, dependency manifests, lockfile and connector configuration are copied without modification. The builder's own README is not copied; this repository keeps its curated one.

This repository is not a sync target. Changes here do not edit or deploy the live game.

## Verification

- Clean install with `npm ci` (2026-11-01, revision `e52739d7`).
- 54 tests passed across 6 files with `npx vitest@3 run`.
- Production frontend compiled with `npm run build`; `npm run lint` passes.
- Application files verified by Git blob hash against the source revision before publication.
- Safety scan of the source found no keys, tokens or environment files.
- Screenshots in `docs/showcase/screens/` are staged sample states rendered from this revision by the Balladeer seat, checked by SHA-256 on receipt. They are not live play.
- Build warning: app ID is not configured for this standalone build. A successful compile is not a live deployment or a multiplayer test.

No dependency upgrades were run during this import.
