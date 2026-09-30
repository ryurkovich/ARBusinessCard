# CHIO XR AR Business Card Workshop

Point a phone camera at the workshop QR code — **your** 3D model appears on top of it. No app required. Changes go live in ~4 minutes via GitHub Pages.

| Doc | Who | Purpose |
|-----|-----|---------|
| [`PREWORK.md`](PREWORK.md) | Learners | GitHub, Antigravity, download a `.glb` before class |
| [`LEARNER_GUIDE.md`](LEARNER_GUIDE.md) | Learners | 30-minute core path + take-home stretch |
| [`PROMPTS.md`](PROMPTS.md) | Learners | Copy-paste agent prompts |
| [`INSTRUCTOR_GUIDE.md`](INSTRUCTOR_GUIDE.md) | Instructors | Slides, demos, troubleshooting |
| [`AGENTS.md`](AGENTS.md) | AI agent | Project map and edit rules |

---

## Quick start (learners)

### 1. Prework
Complete [`PREWORK.md`](PREWORK.md): GitHub account, Antigravity, **Sign in with GitHub** (browser), download one `.glb` from [poly.pizza](https://poly.pizza/).

### 2. Use this template
On the instructor repo click **Use this template** → create a **public** repo named `chio-xr-ar-business-card`.

### 3. Enable GitHub Pages
**Settings → Pages → Source: GitHub Actions**

Live URL:
```
https://[your-username].github.io/chio-xr-ar-business-card
```

### 4. Clone with HTTPS in Antigravity
Green **Code** → copy **HTTPS** URL → `Cmd/Ctrl+Shift+P` → **Git: Clone** → Open.

Never paste SSH keys or tokens into the AI chat.

### 5. Paste prompts from `PROMPTS.md`
1. Help me get started  
2. Add my custom model (file in `models/custom/`)  
3. Commit and publish  

### 6. Test on your phone
- **iPhone/iPad:** Safari  
- **Android:** Chrome  

Scan the **printed default QR** from class. Your model should appear.

---

## Touch controls

| Gesture | Action |
|---------|--------|
| Double-tap | Cycle models |
| Two-finger pinch | Scale |
| Two-finger drag | Rotate |
| One-finger drag | Tilt |

---

## Project files

| Path | Purpose |
|------|---------|
| `index.html` | Complete AR experience |
| `models/` | Bundled fallbacks |
| `models/custom/` | Drop your Poly Pizza `.glb` here |
| `image-targets/` | Default QR tracking data |
| `assets/print/` | Printable default QR |
| `assets/business-card/` | CHIO XR card template (take-home) |
| `external/` | AR engine — do not edit |

---

## Credits
- 8th Wall Engine: © Niantic Spatial, Inc.
- Structure from [aframe-image-targets-example](https://github.com/8thwall/aframe-image-targets-example)
- A-Frame: MIT License
- Workshop branding: CHIO XR
