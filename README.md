# voidsim-wasm

WebAssembly binaries used by [voidsim.io](https://voidsim.io).

Each release ships a `simc.wasm` + `simc.js` pair compiled from upstream
[SimulationCraft](https://github.com/simulationcraft/simc) at a pinned
commit.  See each release's body for the exact upstream SHA the binary
was built from.

The source for the build (Embind wrapper, build recipe, CI workflow)
lives at [`PwogSoupe/voidsim-simc`](https://github.com/PwogSoupe/voidsim-simc).
GPLv3.

## Reproducing a release

1. Clone `PwogSoupe/voidsim-simc` at the source-repo commit referenced
   in this release's body.
2. Follow `BUILDING.md` there.
3. Output `.wasm` should be byte-identical to the one attached here
   modulo the embedded build timestamp.

## Layout

- `simc.wasm`, `simc.js` at the root of `main`: the latest CI build,
  refreshed by the auto-publish workflow.
- Tagged releases on the [Releases page](https://github.com/PwogSoupe/voidsim-wasm/releases):
  historical builds, each pinned to a specific upstream SimC SHA.
