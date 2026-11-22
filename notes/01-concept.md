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

## Következő lépések
- Memóriatérkép részletes kidolgozása
- Tokenizáló alapelvek
- Boot képernyő dizájn
