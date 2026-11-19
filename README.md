# Sanchari Love Experience

A cinematic 3D love story made by Agnik, for Sanchari. Three.js + GSAP, no build step.

## Run it
Browsers block photos and 3D models when a page is opened by double-clicking, so use the tiny local server:
- Windows: double-click `start-windows.bat`
- Mac/Linux: run `./start-mac-linux.sh`
- Or manually: `python -m http.server 8000` in this folder, then open http://localhost:8000 in Chrome or Edge.

## Your files (keep the names exactly)
| What | Path |
|---|---|
| Song | `assets/audio/background-music.mp3` |
| Your voice ("I love you, Sanchari.") | `assets/audio/my-voice.mp3` |
| Photos (portrait 3:4 works best) | `assets/photos/photo-01.jpg`, `photo-02.jpg`, `photo-03.jpg` |
| 3D people (optional) | `assets/models/male-character.glb`, `female-character.glb` |

Until you add the song and voice, the browser console shows two 404 messages. That is expected. The film still plays (soft synthesized music; spoken fallback line).
The three photos included are placeholders. Replace them.

## 3D models
The built-in couple is stylised, not photorealistic. For realistic people, put rigged GLB models (with idle / walk / dance animation clips) in `assets/models/` and set `useModels:true` in `js/config.js`. If a model fails to load, the built-in couple is used.

## Edit text
Everything (letters, captions, star quotes, title) is in `js/config.js`.

## Controls
Begin, Skip intro, letters (click, Esc or click outside to close), Continue, Watch again, Sound on/off (or `M`), Reduce motion.

## Structure
index.html · css/style.css · js/{config,audio,scenes,characters,animations,main}.js · vendor/ (Three r128, GSAP, GLTFLoader, bloom) · assets/

## Notes
Tested with scripted Chrome clicks: zero JavaScript errors, all buttons working. Visual quality was not checked on a real GPU, and the GLB path and glow effect were not exercised.
