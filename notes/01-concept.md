# Fázis 1 – Ötlet és koncepció

## Döntések (2026-11-22)

- Elsődleges nyelv: **angol** (hely- és CPU-spórolás)
- Valódi token-alapú generálás (kis vocab + egyszerű probabilisztikus modell)
- Multiload `.T81`:
  1. Boot + splash + user data bekérés → tartós memória
  2. Motor + alaptudás
  3. Későbbi tudáscsomagok (opcionális)
- Bitmezők a kétállapotú adatokhoz
- D_FILE felső része munkaterület (csak biztonságos karakterekkel, tilos 0x76 és parancskódok)
- Turbo tape rutin a kódban, de alapból kikapcsolva

## Fontos korlátok
- 16 KB összesen
- Nincs valódi lebegőpontos számítás
- Nagyon szűk vocab (cél: 200–400 token)
- Generálás sebessége lassú lesz (Z80)

## Elfogadott döntések (2026-11-23)
- Repo név: ZX81-AI-micro-language-modell ✓
- Elsődleges nyelv: angol ✓
- UI elválasztás: inverz karakterekkel a fejlécsorok, menük, chat üzenetek elkülönítésére ✓

## Haladás (2026-11-23)
- Képernyő/UI elrendezés: kész (`docs/02-screen-layout-and-ui.md`)
- Részletes memóriatérkép: kész (`docs/03-memory-map.md`)
- .T81 sávstruktúra + RAMTOP technika: kész (`docs/04-t81-structure-and-ramtop.md`)

## Elfogadott technikai döntés
- BASIC loader a szalag elején → tájékoztatás → RAMTOP beállítás + NEW → manuális következő blokk indítás
- Tartós adatok a védett (RAMTOP feletti) memóriában

## Következő lépések (Fázis 2 folytatás)
- Tokenizáló alapelvek
- BASIC loader szövegeinek megírása
- Memóriatérkép finomítása a RAMTOP-hoz
