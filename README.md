# QuasarAPP-build

Public build half of the Quasar branded-build farm. Holds **only** the CI
workflow — no source. `build.yml` checks out the private `codeman9528/QuasarAPP`
repo (read-only deploy key), compiles a branded client on free runners with a
throwaway signing key, uploads unsigned artifacts to R2 staging, then dispatches
the private repo's `sign.yml` to re-sign with the real key.

Setup + secrets: see `docs/build-farm/SETUP.md` in the private repo.
