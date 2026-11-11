# Steam Town

A playable 3D data city for our NMC5344 Steam games project, made with three.js. Every tower is a bar from our report, and the whole city follows one rule: **one floor is one percent**. A tower's height is the share of games in that group with 100,000 or more estimated owners.

## Three ways in

The page opens on a title screen with three choices.

- **Play the forecast.** The city starts unbuilt. In six missions you guess a height with a slider, lock it in, and the real towers rise next to the outline of your guess. Each mission is worth 100 points, minus 5 for every floor you are off. The final score (out of 600) gives a rank from Common to Legendary analyst, with fireworks.
- **Guided tour.** Nine stops: the data, the owner tiers, three power-ups (systems, languages, DLC), the combo, the plot twist, a tower you build yourself, and the results. Each chart row is linked to one structure: tap a row to fly to its tower, tap a tower to find its row.
- **Free roam.** Drag to rotate, scroll or pinch to zoom, tap any tower or pin.

Adding `#play`, `#tour` or `#roam` to the address skips the title screen.

## How to read the city

| Structure | What it shows | Why it looks like that |
|---|---|---|
| Foundation under the old town | All 81,117 games in five owner tiers, 100 floors deep | Only the top 9.4 floors are Rare or better |
| Bundled glass shafts | Games on 1, 2 or 3 operating systems | One shaft per system |
| Round stone towers with flags | Number of supported languages | Babel towers: more languages, more flags on the roof |
| Stacked blocks | No DLC and has DLC | The bottom block is the base game, each block on top is an expansion |
| Housing blocks and braced glass megatowers | The combo: one-system games by DLC count, in 1 language (front) and 11+ languages (back) | The back row is where the three features stack up |
| Tower under construction | A build you choose yourself | 48 real combinations |
| The halo | How much of the difference in owners the three features explain | 5.5% lights up with the "0 – 0" games, 15.4% without them |

Other megastructures stand in the haze around the town (gates, ziggurats, domes, other towns on pillars). They are scenery, not data.

## Other controls

- **Time of day:** day, golden hour (the default) or night. After dark the windows light up, the accent stripes glow and searchlights sweep.
- **Music:** "Not Quite a Masterpiece" plays on a loop. It is on by default and starts with your first click or tap, because browsers do not let a page make sound before that. The button on the title screen or the note icon in the dock turns it off, and the page remembers that choice.
- **Icons in the dock:** miniature blur, falling petals, slow spin, music, photo mode (hides the controls and can save a picture) and reset view.
- Scores and achievements are kept in the browser's local storage on your own device only.

## Where this page lives

This folder is one part of the project site. It is a static page with no build step. The title screen, the credits and the last tour stop link to the written report in `../report/`, to the pixel story in `../steam-pixel-story/` and to the project home in `../`, so the folder belongs next to those in the same repository.

To view it on your own computer, serve the repository folder (for example `python -m http.server`) instead of opening `index.html` directly.

## Files

| Path | What it is |
|---|---|
| `index.html` | The page. It loads three.js 0.160.0 from jsDelivr, two fonts from Google Fonts and the models from `assets/`. |
| `assets/city/` | KayKit City Builder Bits: buildings, roads, bench, streetlights, cars, water tower. |
| `assets/nature/` | KayKit Medieval Hexagon Pack: rocks. |
| `assets/audio/` | The music track (MP3, 5.6 MB). It is fetched after the scene has loaded, unless the visitor turned the music off on an earlier visit. |

Each `.gltf` file has its geometry embedded, so a model is one file plus the shared palette texture (`.png`) in its folder.

## Credits and licenses

- 3D town models by Kay Lousberg ([kaylousberg.com](https://www.kaylousberg.com)), from KayKit City Builder Bits 1.0 and KayKit Medieval Hexagon Pack 1.0. Both packs are CC0 (public domain); the license files are in `assets/city/LICENSE.txt` and `assets/nature/LICENSE.txt`.
- The megastructures, jacaranda trees, clouds, sky, lighting and far skyline are generated in code. The pixel icons were drawn for this project.
- Music: "Not Quite a Masterpiece", made with Suno.
- Rendering: [three.js](https://threejs.org) (MIT), with `OrbitControls`, `GLTFLoader`, `OutlineEffect`, `UnrealBloomPass` and the tilt-shift shaders from its examples. Fonts: Big Shoulders Display and Zen Maru Gothic (SIL Open Font License).
- Data: Steam Games Dataset 2025 (Kaggle), store data up to 10 March 2025. Every height matches our report; the halo uses our re-run of the models without the "0 – 0" games.
