# What Makes a Game Popular?

Our NMC5344 group project: a data-driven look at 81,117 Steam games. We ask how three design choices go with reaching 100,000 or more owners: running on more operating systems, supporting more languages and adding DLC.

**Start here: <https://absentminderic.github.io/steam-town/>**

| | What it is | Link |
|---|---|---|
| **Steam Town** | The analysis as a playable 3D city. One floor is one percent: forecast each tower's height, take the guided tour or roam freely. | [Play](https://absentminderic.github.io/steam-town/steam-3d-city/) |
| **Pixel story** | The same findings as a scrolling story where every game is one pixel. | [Open](https://absentminderic.github.io/steam-town/steam-pixel-story/) |
| **Final report (PDF)** | The written report: the data, four charts and four regression models. | [Open](https://absentminderic.github.io/steam-town/report/Group_Project_1111_1013.pdf) |
| **Report with R code (HTML)** | The same report as a web page, with every code chunk and its output. | [Open](https://absentminderic.github.io/steam-town/report/Group_Project_1111_1013.html) |

## What is in this repository

| Path | Contents |
|---|---|
| `index.html`, `steam-town.jpg` | The project home page. |
| `steam-3d-city/` | Steam Town: one HTML page plus 3D models, textures and the music track. See its README for how to read the city. |
| `steam-pixel-story/` | The pixel story: a single HTML page with no libraries. |
| `report/` | The report as knitted from R Markdown, in PDF and HTML. |

Everything is static: there is no build step, and GitHub Pages serves the files as they are.

## Notes on the numbers

- Every height in Steam Town and every count in the pixel story matches the charts in the report, which use the 81,117 games that have an owner estimate.
- The regression models in the report keep the games whose owner estimate is "0 - 0" and explain about 5.5% of the differences in owners. Steam Town's halo and Stage 9 of the pixel story also show our re-run of the same four models without those games (about 15.4%). That re-run was made for these pages and is not part of the written report.
- One code chunk in the report read the data from a folder on a teammate's computer. In the copies published here that folder name, which was his full name, is shortened to `ken`; nothing else in the report was changed.

## Credits

- Made by Jingyi, [@absentminderic](https://github.com/absentminderic), [Kenetizen](https://github.com/Kenetizen), [@letitgotia](https://github.com/letitgotia) and Vivian for NMC5344, November 2026.
- Data: Steam Games Dataset 2025 (Kaggle), store data up to 10 March 2025.
- 3D town models: KayKit City Builder Bits and Medieval Hexagon Pack by Kay Lousberg, CC0. Rendering: [three.js](https://threejs.org) (MIT). Fonts from Google Fonts (SIL Open Font License): Big Shoulders Display and Zen Maru Gothic in Steam Town and on the home page; Press Start 2P, Pixelify Sans and Space Grotesk in the pixel story.
- Music in Steam Town: "Not Quite a Masterpiece", made with Suno.
