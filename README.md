# ZX81-AI-micro-language-modell
**Pico AI** — Miniature Language Model for Sinclair ZX81 (16 KB)

> Valódi generálás, nem sablonválaszok. Egyetlen `.T81` multiload kazettafájlban.

## Projekt célja
Egy működő, 16 KB RAM-on futó mikro nyelvi modell a Sinclair ZX81-re, amely:
- Valódi tokenizálást és generálást használ (nem előre megírt mondatokat)
- Multiload `.T81` formátumban érkezik (boot + motor + alaptudás + későbbi tudáscsomagok)
- Tartós memóriát biztosít a felhasználói adatoknak
- Hőmérséklet, reasoning, chat history kezelést tartalmaz
- Angol nyelven működik (hely- és teljesítményoptimalizálás miatt)

## Fejlesztési fázisok
1. **Ötlet és koncepció** (architektúra, realitásvizsgálat)
2. **Tervezés** (memóriatérkép, `.T81` sávstruktúra, bitmezők, vezérlők)
3. **Kódolás és csomagolás** (motor, generátorok, `.T81` fájl)
4. **Adatbázis, tréning, tesztelés**

## Memória-elosztás (irányadó, 16 KB)
| Komponens              | Méret      |
|------------------------|------------|
| Motor / keretprogram   | 3–5 KB     |
| Tartós szótár / adatok | 2–3 KB     |
| Chat history           | 2–3 KB     |
| Tudásbázis             | 7–10 KB    |
| Tartalék               | 50–150 B   |

## Vezérlőbillentyűk (tervezett)
- `SHIFT + 1..4` — Temperature
- `SHIFT + 9`    — Reasoning on/off
- `SHIFT + 5/6`  — Chat history scroll
- `SHIFT + S`    — Mentés kazettára
- `SHIFT + SPACE`— Megszakítás

## Készítő
Made with GLM help by **Safar Sandor**  
Magyarországon élő autóbuszvezető, amatőr író és csillagász  
Kapcsolat: SAFIZX810GMAIL.COM (a ZX81-en inverz 0-val a @ helyett)

## Repository struktúra (tervezett)
```
.
├── README.md
├── docs/                 # Tervezési dokumentumok, memóriatérkép
├── src/                  # Z80 assembly források
├── tools/                # Python generátorok, tréning eszközök, .T81 builder
├── knowledge/            # Alaptudás és szakosított csomagok
├── releases/             # Kész .T81 fájlok
└── notes/                # Fejlesztési jegyzetek
```

## Állapot
**Fázis 1 – Koncepció** folyamatban.

---
*Ez a repository a GROK munkakönyvtárban fejlesztve.*
