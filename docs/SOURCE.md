# Source provenance

The current game snapshot was copied from the builder-linked source revision `25c5a06e8e3d9acd122eb4daff13e5162a1188a1` on 2026-10-30.

Application code, tests, assets, dependency manifests, lockfile and connector configuration are copied without modification. The public repository maintains its own README, MIT licence and showcase artwork. The builder's generic README is not substituted for the game's curated documentation.

This public repository is a showcase and source snapshot, not the builder's two-way-sync target. Changes here do not automatically edit or deploy the live game. The source-sync repository remains private and was not changed by this publication.

## Verification

- Clean install with `npm ci`.
- 44 tests passed across 5 files with `npx vitest@3 run`.
- Production frontend compiled with `npm run build`.
- Application files verified by Git blob hash against the source revision after publication.
- Build warning: app ID is not configured for this standalone build. A successful compile is not a live deployment or multiplayer test.

No dependency upgrades were run during this publication.
