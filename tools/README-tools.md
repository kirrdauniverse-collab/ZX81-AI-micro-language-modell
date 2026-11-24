# Tools for Pico AI

## Planned tools
- `bas2p.py` – Convert ZX81 BASIC source to .P file (memory image starting at $4009)
- `make-t81.py` – Combine multiple .P / named blocks into a single .T81 for EightyOne and compatible emulators
- `vocab-builder.py` – Build binary vocab + simple bigram tables from text lists
- `knowledge-pack.py` – Create replaceable knowledge blocks

## Current status (v0.1)
No binary generators yet. The BASIC loader is provided as source.  
Next version will include a minimal working bas2p converter so we can produce real loadable files and a multi-block .T81.
