# aphrody-labs/WebKit

Fork of oven-sh/WebKit used by aphrody-labs/bun. `main` follows oven-sh/WebKit `main`
(`.github/workflows/aphrody-upstream-sync.yml`, every 6 h). Prebuilts are produced by
`.github/workflows/aphrody-prebuilts.yml` with upstream's lanes, Dockerfiles and archive names
(`bun-webkit-<os>-<arch>[-musl][-debug|-lto][-asan].tar.gz`) and published as the release `autobuild-<sha>`.
Upstream's `ci.yml` needs oven-sh's private runners and is disabled here.

Patch flow: commit the JSC/WebKit patch on `main` here -> `gh workflow run aphrody-prebuilts.yml -f ref=<sha>` ->
bump `WEBKIT_VERSION` and `WEBKIT_REPO` in aphrody-labs/bun `scripts/build/deps/webkit.ts`.
