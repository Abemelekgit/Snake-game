# Snake Game (Capacitor-friendly)

A mobile-optimized Snake game with a cyberpunk look, touch D-pad, and persistent high score.

## Features
- Fullscreen canvas that auto-resizes to device size
- Touch D-pad for Android thumbs + keyboard arrows/WASD
- Difficulty modes: Chill, Classic, Hard (speed changes live)
- LocalStorage high score, snake growth, wall/self collision
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
- Touch: On-screen D-pad (bottom half)
- Keyboard: Arrow keys or WASD

## Difficulty
- Chill: slower
- Classic: default
- Hard: faster

## Files
- `index.html` — all game code (HTML/CSS/JS)

## Notes
- Viewport meta disables zoom/scroll for a native feel
- Uses only Canvas + vanilla JS; no external deps
