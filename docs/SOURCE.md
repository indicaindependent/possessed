# Source provenance

**`possessed-source` is the live builder repository. `possessed` is the curated showcase.** The Base44 builder writes to [possessed-source](https://github.com/indicaindependent/possessed-source) and syncs to its `main` branch, so that repository is always the latest game. This repository is a hand-maintained showcase of it, with its own README, MIT licence and artwork.

## Imported revision

The game files were copied byte for byte from builder revision `fa991d56ec3e7c93ff30c36c3d1c3f52c8a6982c` (2026-11-05 13:49 UTC), the finished game. The previous showcase import was `e52739d727fa81bac1bbf562e79c47fa6f0cacd7` (2026-11-01), and before that `1c44b75acd4b5e9418ab9f5f20147116054bbb23` (2026-10-31) and `868a738bcb5145d2c7aae263b676ac9eb78a8231` (2026-10-30).

Changes since `e52739d7`, 24 builder commits:

- `2f4d10d1` Practice mode against the House, and clearer match feedback.
- `d566678d` Ghost taunts with cooldowns.
- `a9ac0c39` Gameplay polish, match animations and end-of-game results.
- `4df04d15` Ghost balance changes.
- `25359ac2` Match delay readout and live presence status.
- `0a6c9330`, `c31565ac`, `21eddce1`, `6e1fbb40`, `f198834d` The opening cinematic and its fog, framing and lighting.
- `8848ae92` The House's first search waits until after the first clue.
- `8df75473` The sound button becomes a Sound on / Sound off link; duplicate audio playback prevented.
- `8a3e6d13` Base44 package update.
- `fa991d56` Ghost path reveals, home panel improvements and difficulty settings.
- Other commits are builder file changes and auth templates.

Earlier, since `1c44b75a`: autoplay audio with a sound toggle, home and waiting-room ambience and a music loop fix (`30756362` to `e52739d7`). Since `868a738b`: background music (`6be7c45e`), mobile UI and typography (`81733b67`), design tokens in `src/index.css` (`3cac8859`) and a GhostMeter tweak (`1c44b75a`).

Application code, tests, assets, dependency manifests, lockfile and connector configuration are copied without modification. The builder repository's README and LICENSE are not copied; this repository keeps its curated ones. `src/components/possessed/screens/SoundToggle.jsx` was removed here because the builder removed it.

This repository is not a sync target. Changes here do not edit or deploy the live game.

## Verification

- Clean install with `npm ci` (2026-11-05, revision `fa991d56`).
- 118 tests passed across 14 files with `npx vitest@3 run` on Node 22. On Node 20 one audio test fails because Node 20 has no global `navigator`; the game code is unchanged.
- Production frontend compiled with `npm run build`; `npm run lint` passes.
- Application files verified by Git blob hash against the source revision before publication.
- Safety scan of the source found no keys, tokens or environment files.
- Screenshots in `docs/showcase/screens/` are staged sample states rendered by the Archivist seat from this revision's own development fixtures (`/dev/fixture`) and home screen at 1920x1080. They are not live play.
- Build warning: app ID is not configured for this standalone build. A successful compile is not a live deployment or a multiplayer test.

No dependency upgrades were run during this import.
