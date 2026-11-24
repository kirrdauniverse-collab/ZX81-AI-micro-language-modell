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

## Haladás (v0.1 – 2026-11-24)
- Tokenizáló és generálási alapelvek: kész
- BASIC loader első változat: kész
- Vocab első vázlat: kész
- Teljes verziódokumentáció: `docs/versions/v0.1-RELEASE-NOTES.md`
- Minden kész dokumentum verziózva a `docs/versions/` alatt

## Következő lépések (v0.2 felé)
- bas2p + make-t81 eszközök (egyetlen .T81 fájl az emulátorokhoz)
- Loader továbbfejlesztése (user adatok bekérése)
- Persistent block bináris elrendezés
- Második blokk (egyszerű demo vagy motor stub)
- Vocab bővítés + első bigram adatok
