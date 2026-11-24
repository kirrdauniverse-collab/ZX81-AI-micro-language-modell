# Pico AI v0.1 – Tryable Loader

## Files
- `pico-ai-loader-v0.1.p` – Standard ZX81 .P file (loadable in almost every emulator)
- `pico-ai-loader-v0.1.p81` – Same with filename header

## How to try
1. Download the `.p` file
2. Open in any ZX81 emulator (EightyOne, sz81, JtyOne online, etc.)
3. Load the file
4. Type `RUN` (or it may auto-run depending on emulator)
5. Read the screens, press a key, then ENTER when asked
6. The program sets RAMTOP and executes NEW

This is the first stage loader only. The full multi-block .T81 with engine will come in the next version.

## Source
See `src/v0.1/loader-basic-v1.bas` and the documentation in `docs/versions/`.
