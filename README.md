# Snake Game (Capacitor-friendly)

A mobile-optimized Snake game with a cyberpunk look, touch D-pad, and persistent high score.

## Features
- Fullscreen canvas that auto-resizes to device size
- Touch D-pad for Android thumbs + keyboard arrows/WASD
- Swipe controls directly on the playfield
- Difficulty modes: Chill, Classic, Hard (speed changes live)
- Arena modes: solid walls or wrap-around edges
- LocalStorage high score, snake growth, wall/self collision
- Status badge and improved game-over messaging
- Dark neon UI with Start/Restart overlay

## Quick Start (web)
```bash
npm install --global serve
serve .
```
Open the served URL on your device/emulator.

## Run with Capacitor
```bash
npm init -y
npm install @capacitor/core @capacitor/cli
npx cap init snake-game com.example.snake
# Ensure index.html stays at project root or adjust webDir in capacitor.config.*
npx cap add android
npx cap copy android
npx cap open android
```
In Android Studio, build and run on a device/emulator. Set `android:usesCleartextTraffic="true"` in `AndroidManifest.xml` if loading from a local dev server.

## Controls
 - Pause/Resume: Space bar (auto-pauses on window blur)
 - Restart: Enter key or Start button

## Difficulty
 - Remembers last selected mode across sessions

## Arena Modes
- Walls: hitting a boundary ends the run
- Wrap: exiting one side of the screen re-enters from the opposite side

## Files
- `index.html` — all game code (HTML/CSS/JS)

## Notes
- Viewport meta disables zoom/scroll for a native feel
- Uses only Canvas + vanilla JS; no external deps
