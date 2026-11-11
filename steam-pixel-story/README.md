# What Makes a Game Popular? The pixel story

A scrolling pixel story about 81,117 Steam games, one pixel each. It shows how supporting more operating systems, more languages and DLC go with reaching 100,000+ estimated owners.

NMC5344 group project, November 2026. Made by Jingyi, [@absentminderic](https://github.com/absentminderic), [@Kenetizen](https://github.com/Kenetizen), [@letitgotia](https://github.com/letitgotia) and Vivian.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole page: HTML, CSS and JavaScript in one file. No build step and no libraries; fonts come from Google Fonts. |

The credits at the end of the page link to the written report in `../report/` (PDF and HTML), to Steam Town in `../steam-3d-city/` and to the project home, so this folder belongs next to those in the same repository.

## Where the numbers come from

- Data: [Steam Games Dataset 2025 on Kaggle](https://www.kaggle.com/datasets/artermiloff/steam-games-dataset), with store data up to 10 March 2025.
- The `CELLS` array in `index.html` holds game counts by operating systems, languages, DLC and owner tier. It was re-derived by following the steps in the report's R code: of 89,624 rows, 10 broken rows, 8,418 games with an owner estimate of "0 - 0" and 79 games with no language listed are left out, which leaves 81,117 games. Every group size and percentage on the page matches the report.
- Stage 9 re-runs the report's four regression models (log of the owner-range midpoint) with and without the "0 - 0" games. Adjusted R² goes from 0.053–0.055 to 0.145–0.154, and the language coefficient in model 1 turns from −0.039 to +0.010. The version without those games was made for this page; the written report uses the version with them.

## Easter eggs

Scroll to the end, or try ↑ ↑ ↓ ↓ ← → ← → B A on a keyboard.
