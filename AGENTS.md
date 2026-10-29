# AGENTS.md

## Project overview

Phaser 3 browser game template (vanilla JS + ES modules, no build step, no framework).

- Entry chain: `index.html` → loads Phaser from CDN → `./main.js` → `scenes/Game.js`.
- Only one scene exists: `scenes/Game.js` (class `Game extends Phaser.Scene`, scene key `"game"`).
- Phaser version is pinned via CDN in `index.html` (`//cdn.jsdelivr.net/npm/phaser@3.80.1/dist/phaser.min.js`).

## Commands

- No `package.json`, npm scripts, tests, lint, typecheck, or CI. Nothing to install or run locally.
- Run the game: serve the repo root with any static server (e.g. VS Code Live Server — configured port **5501** in `.vscode/settings.json`, or `python -m http.server`).
- Serve from repo root; asset paths are relative to the web root (`public/assets/...`).

## Architecture notes

- Real entrypoints are `index.html`, `main.js`, and `scenes/Game.js`; there is no src/ or lib/ split.
- To add a scene: import it and append to the `scene` array in `main.js`. Comment in `main.js` notes only the first scene shows by default.
- Assets live in `public/assets/` and are referenced in `preload()` with cache keys `map`, `tileset`, `star`, `dude`.
- Tilemap: `public/assets/tilemap/map.json` (Tiled JSON). Collision enabled per tileset property `esColisionable`.
- Tiled layer / object naming is in Spanish: layers `"Fondo"`, `"Plataformas"`, `"Objetos"`; object named `player` is the spawn point, objects of type `"star"` go into the stars group.

## Quirks / gotchas

- Game config (720×720, arcade physics gravity `{y: 200}`, `debug: true`) is in `main.js`; scene logic lives in `scenes/Game.js`.
- Press **R** in-game to restart the scene (`this.scene.restart()`).
- Score starts at 0, +10 per collected star; stars respawn when the active count hits 0.

## Instruction sources

- `README.md` — setup/customization steps for template users (update Phaser version in `index.html`, change `<title>`, commit messages like `Update Phaser version and title`).

# Instrucciones del proyecto

## Objetivo
Desarrollar ExploradorTP2 para cumplir la Propuesta 2 del TP de Phaser 3.

## Requisitos obligatorios
- Construir el laberinto mediante tilemaps de Phaser.
- Implementar objetos recolectables.
- Exigir al menos 5 objetos recolectados para completar cada nivel.
- Permitir avanzar a un nuevo mapa al cumplir la condición de llegada.
- Conservar el puntaje acumulado entre niveles.
- Crear un tercer nivel más grande que la pantalla.
- Implementar una cámara que permita explorar el tercer nivel.

## Forma de trabajo
- Antes de modificar código, inspeccionar la estructura y comprender la implementación existente.
- Trabajar en cambios pequeños y verificar cada cambio.
- No rehacer sistemas que ya funcionan sin una razón concreta.
- No eliminar funcionalidades existentes sin autorización.
- Utilizar Phaser 3, respetando la versión y las dependencias actuales del proyecto.
- Después de modificar código, ejecutar la compilación y corregir los errores relacionados con los cambios.
- Informar qué archivos se modificaron, qué se verificó y qué queda pendiente.
- No afirmar que una mecánica funciona si no se probó.

## Git
- Trabajar en la rama de desarrollo, no directamente en main.
- No hacer commits ni subir cambios a GitHub sin autorización.
