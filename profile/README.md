## Organizace 

Kefer Astrology slouží jako propojení pro výpočty napříč různými astrologickými systémy.
Základní nastavení provádí všechny výpočty přímo nad NASA JPL daty (švýcarské efemeridy je možno použít také).

## Architektura aplikace

- Udržujeme dvě prostředí s identickou funkcionalitou (v současné době ve vývoji)
  - [Python](https://kefer-astrology.github.io/function-wrapper/architecture/) (s grafickými nadstavbami kivy, streamlit, tkinter)
  - [Rust Tauri](https://kefer-astrology.github.io/tauri-application/docs/architecture/) (grafická nadstavba je na [React](https://kefer-astrology.github.io/tauri-application/docs/frontend-react/) / [Svelte](https://kefer-astrology.github.io/tauri-application/docs/frontend-svelte/))
- Zároveň zde máme i zdrojové kódy našich stránek
- Do budoucna se počítá ještě s několika podprojekty:
  - Databáze osobností a událostí (použitelná jako zdroj pro načítání horoskopů)
  - Podklady pro definice nových efemerid

## License defintion

Rust standalone path:
  backend_for_chart(chart)
    → SwissAstronomyBackend     → libswe → (AGPL)
    → JplAstronomyBackend       → anise → MPL-2.0 (Mozzila Public License)

Python sidecar path:
  SwissAstronomyBackend   → Kerykeion → pyswisseph → libswe (AGPL)
  JplAstronomyBackend     → Skyfield  → de421.bsp  → MIT + public domain


## Spustitelné programy

- Vydání nových verzí ještě nejsou plně zavedené
- V současné chvíli jsou k dispozici jako artefakty github workflows


## Testování

- Obě prostředí jsou testována seprátně (Python / Rust) - využíváme github actions kde to jde

