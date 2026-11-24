# Pico AI – Tryable files (v0.1 / v0.2 early)

## Loader (collects personal data)
- **pico-ai-loader-v0.2.p**  ← ajánlott
  - Bekéri: neved, nemed (M/F), dátum (DD/MM/YYYY), idő (HH:MM)
  - Megerősítteti
  - Beállítja a RAMTOP-ot 30000-re
  - NEW-t csinál
  - Utána manuálisan LOAD "" a következő blokknak

## Demo chat (egyszerű tudás)
- **pico-ai-demo-chat-v0.2.p**
  - Egyszerű hardcoded válaszok
  - Kipróbálható kérdések: hello, who are you, who made you, what is zx81
  - BYE-val kilép

## Használat
1. Töltsd be a loader-t → add meg az adatokat → ENTER
2. NEW után írd be: LOAD ""
3. Töltsd be a demo-chat-et (külön fájlként egyelőre)

A teljes egyetlen .T81 (loader + tudás egy fájlban) a következő lépés.

## Források
- src/loader-basic-v0.2.bas
- src/demo-chat-v0.2.bas
