# Mega Man Battle Chip Challenge — Recompiled 
**AI Label**:
***Created using the help of Meta's Muse***

Static recompilation of **Mega Man Battle Chip Challenge (USA, GBA)** into
portable C++ using the [gbarecomp](https://github.com/mstan/gbarecomp)
framework (ARM7TDMI machine code translated ahead-of-time to native C++).

## Contents

- `src_native/generated/` — recompiled C++ shards (8 translation units),
  dispatch table, and symbol map, generated from the cartridge image.
- `src_native/CMakeLists.txt`, `build.ps1`, `build.sh` — build the
  generated static library (`gbarecomp_game`).
- `src_native/framework/include/` — runtime headers needed to compile.
- `game.toml` — per-cartridge recompiler configuration (SHA-1/MD5 pinned).
- `docs/` — notes.

## Building

Requires CMake, a C++20 compiler, and SDL2 (for the host runner, later
phases). The generated library step:

```sh
cd src_native
cmake -S . -B build
cmake --build build
```

A playable integration (host app/launcher, cartridge config, Android
packaging) is tracked as follow-up work.

## Legal

This repo contains **no game ROM, BIOS, or extracted game assets**.
The generated C++ is derived from a cartridge image the owner dumped
themselves; the runtime verifies the ROM SHA-1 before use. Keep this
repository private and do not redistribute the generated sources.
