## Organizace 

Kefer Astrology slouží jako propojení pro výpočty napříč různými astrologickými systémy.
Základní nastavení provádí všechny výpočty přímo nad SPICE/JPL daty (švýcarské efemeridy je možno použít také).
Na pořadu d

## Architektura aplikace

- Udržujeme dvě prostředí s identickou funkcionalitou (v současné době ve vývoji)
  - [Python](https://github.com/kefer-astrology/function-wrapper/blob/main/docs/architecture.md) (s grafickými nadstavbami kivy, streamlit, tkinter)
  - [Rust Tauri](https://github.com/kefer-astrology/tauri-application/blob/main/docs/content/docs/architecture.md) (grafická nadstavba je na [React](https://github.com/kefer-astrology/tauri-application/blob/main/docs/content/docs/frontend-react.md) / [Svelte](https://github.com/kefer-astrology/tauri-application/blob/main/docs/content/docs/frontend-svelte.md))
- Zároveň zde máme i zdrojové kódy našich stránek
- Do budoucna se počítá ještě s několika podprojekty:
  - Databáze osobností a událostí (použitelná jako zdroj pro načítání horoskopů)
  - Podklady pro definice nových efemerid


## Spustitelné programy

- Vydání nových verzí ještě nejsou plně zavedené
- V současné chvíli jsou k dispozici jako artefakty github workflows


## Testování

- Obě prostředí jsou testována seprátně (Python / Rust) - využíváme github actions kde to jde

