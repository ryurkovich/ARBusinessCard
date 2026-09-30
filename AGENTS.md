# AGENTS.md

## What This Project Does
WebAR application for the **CHIO XR** workshop. Opens on a phone, uses the camera, detects the **default printed QR** image target, and displays a 3D model anchored to it. Runs in the browser — no app install for viewers.

## IMPORTANT: Read WORKSHOP_AGENT_CONFIG.md First
Before taking any action, read `WORKSHOP_AGENT_CONFIG.md`. Guide step by step. Do not one-shot. Never request secrets, SSH keys, or personal access tokens.

## Stack
- 8th Wall Engine: `external/xr/xr.js` — DO NOT MODIFY
- 8-Frame (patched A-Frame): `external/scripts/8frame-1.5.0.min.js` — DO NOT MODIFY
- xrextras: `external/xrextras/xrextras.js` — DO NOT MODIFY
- Source reference: https://github.com/8thwall/aframe-image-targets-example
- No build step required for GitHub Pages: `index.html` is the complete application

## Deployment
Auto-deploys to GitHub Pages on push to `main` (`.github/workflows/deploy.yml`).
URL pattern: `https://[username].github.io/chio-xr-ar-business-card`
Deploy time: ~4 minutes.

## The Workshop Change (core personalization)
Learners add their own Poly Pizza `.glb` into `models/custom/`, then:
1. Add `<a-asset-item id="custom-model" src="./models/custom/FILENAME.glb">` inside `<a-assets>`
2. Set `gltf-model="#custom-model"` on `#active-model`
3. Optionally tune `scale` / `position` and add an entry to the `models` array for double-tap

Do **not** change `targetData` or image targets during the core workshop. The shared default QR is intentional.

## File Map
| File / folder | Purpose |
|---------------|---------|
| `index.html` | Complete AR application — EDIT marked sections only |
| `models/*.glb` | Bundled fallback models |
| `models/custom/` | Learner drops their Poly Pizza `.glb` here |
| `image-targets/` | Default QR target data — do not edit in-session |
| `assets/print/default-qr-code.png` | Printable handout of the default QR |
| `assets/business-card/chio-xr-card-template.png` | Printable card with QR placeholder (stretch) |
| `external/` | AR engine — never modify |
| `PROMPTS.md` | Copy-paste prompts for learners |
| `PREWORK.md` | Setup before class |
| `LEARNER_GUIDE.md` | Full walkthrough |
| `INSTRUCTOR_GUIDE.md` | Presentation + demo cues |
| `WORKSHOP_AGENT_CONFIG.md` | Agent behavior rules |
| `.nojekyll` | Prevents GitHub Pages Jekyll processing |

## Touch Interactions (Already Built)
- Double-tap: cycles models in the `models` array
- Two-finger pinch: scale
- Two-finger rotate: rotate
- One-finger drag: tilt

## Common Agent Tasks
- Wire custom `.glb`: asset item + `gltf-model="#custom-model"` (+ scale)
- Fallback bundled model: change `gltf-model` to `#robot-model` etc.
- Change spin speed: `dur: 6000` in the animation attribute
- Add text label: `<a-text>` inside the image target entity
- Take-home image target: `npx @8thwall/image-target-cli@latest`, paste JSON into `targetData`, update `name=`

## Security / Auth Rules for Agents
- Prefer HTTPS remotes (`https://github.com/...`)
- If remote is SSH (`git@...`), coach switching via IDE UI — never generate or request keys in chat
- Learner clicks Commit / Sync in Source Control; do not ask them to paste credentials into chat
