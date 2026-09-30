# CHIO XR AR Business Card — Learner Guide

**About 30 minutes of hands-on work.** You leave with a live URL: open it on your phone, point at the workshop’s printed QR, and **your** 3D model appears.

Full prompts: [`PROMPTS.md`](PROMPTS.md)  
Before class: [`PREWORK.md`](PREWORK.md)

---

## What you are building

A WebAR page on GitHub Pages. The camera looks for the **default QR** (image target). When it sees that image, it anchors your Poly Pizza model on top. No app install for anyone who views it — just a link and a camera.

---

## Part 1: Create your copy from the template (5–6 minutes)

### Use this template (easier than “fork”)

1. Open the instructor link (they will paste it in chat / on a slide).
2. Click the green **Use this template** button → **Create a new repository**.
3. Repository name: leave as `chio-xr-ar-business-card` (or match what the instructor says).
4. Set visibility to **Public**.
5. Click **Create repository**.

Your copy lives at:
```
https://github.com/[your-username]/chio-xr-ar-business-card
```

### Enable GitHub Pages (do this before you push)

1. In **your** repo, open **Settings** → **Pages**.
2. Under **Source**, choose **GitHub Actions**.
3. Save if needed.

Your future live URL:
```
https://[your-username].github.io/chio-xr-ar-business-card
```

Write it down. If you skip Pages and push first, open **Actions** later and re-run the deploy after enabling Pages.

---

## Part 2: Easy HTTPS clone into Antigravity (4 minutes)

1. Confirm you already signed in to GitHub **inside Antigravity** (see [`PREWORK.md`](PREWORK.md)).
2. On your GitHub repo page, click green **Code**.
3. Choose **HTTPS** and copy the URL. It must start with `https://github.com/` — **not** `git@`.
4. In Antigravity press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows).
5. Run **Git: Clone**, paste the HTTPS URL, choose Desktop or Documents, then **Open**.

If Antigravity asks you to sign in, use **Sign in with GitHub** in the browser. Never paste keys into the agent chat.

Stuck? Paste prompt **1. Help me get started** from [`PROMPTS.md`](PROMPTS.md).

---

## Part 3: Help me get started (2–3 minutes)

Open the agent panel. Paste:

```
Help me get started with this CHIO XR AR Business Card workshop.
```

(Or the full version in [`PROMPTS.md`](PROMPTS.md).)

When the agent says you are ready, continue.

---

## Part 4: Add your custom model (core personalization) (6–8 minutes)

1. In the left file tree, open `models` → `custom`.
2. Drag your Poly Pizza `.glb` from Desktop/Downloads into `models/custom/`.
3. Paste prompt **2. Add my custom model** from [`PROMPTS.md`](PROMPTS.md), with your real filename.

The agent will register the file in `index.html` and set `gltf-model="#custom-model"`.

**Fallback:** if you have no `.glb`, use the fallback prompt to pick a bundled model (`#crystal-model`, etc.), then add a custom model later at home.

---

## Part 5: Commit and publish (3 minutes)

1. Paste prompt **3. Commit and publish** or follow these clicks:
2. Open **Source Control** in Antigravity.
3. Message: `add my custom model`
4. **Commit** → **Sync Changes** / **Push**.
5. On GitHub, open the **Actions** tab and wait for a green check (~4 minutes).

---

## Part 6: Test on your phone (5–8 minutes)

1. On your phone open:
   `https://[your-username].github.io/chio-xr-ar-business-card`
2. **iPhone/iPad:** Safari · **Android:** Chrome  
3. Allow camera access.
4. Point at the **printed default QR** from the workshop (same handout for everyone).
5. Hold steady, good light, whole QR in frame, ~10–15 inches away.

You should see **your** model. Pinch to scale, two-finger drag to rotate, double-tap to cycle (if configured).

### If nothing appears
- Wait for Actions to finish; hard-refresh the page  
- Confirm you are on *your* username URL  
- Use the workshop printed QR (not a random QR yet)  
- Brighter light; full QR visible  

---

## Project map

```
chio-xr-ar-business-card/
├── index.html              ← the whole AR app (EDIT marked sections)
├── models/                 ← bundled fallbacks
│   └── custom/             ← drop YOUR .glb here
├── image-targets/          ← default QR tracking data (do not edit in class)
├── assets/print/           ← printable default QR
├── assets/business-card/   ← CHIO XR card template (take-home)
├── external/               ← AR engine — do not edit
├── PROMPTS.md              ← copy-paste prompts
├── PREWORK.md              ← before class
└── AGENTS.md               ← instructions for the AI agent
```

---

## Take-home stretch (optional)

Not required during the 30-minute session.

1. After Pages is live, create a Canva QR that encodes **your** Pages URL: [Canva QR generator](https://www.canva.com/qr-code-generator/).
2. Ask the agent (take-home prompt in [`PROMPTS.md`](PROMPTS.md)) to help retarget the image with the 8th Wall CLI.
3. Redeploy, then place that QR into [`assets/business-card/chio-xr-card-template.png`](assets/business-card/chio-xr-card-template.png) (“Insert your QR code here”) in Canva or an image editor.
4. Print your card — scan to open the site **and** use the same QR as the AR target once retargeted.

---

## Key terms

| Term | Meaning |
|------|---------|
| Template | Button that creates your own new repo from the instructor project |
| Clone | Download your repo to the laptop via HTTPS |
| Commit | Labeled snapshot of your files |
| Push / Sync | Send that snapshot to GitHub |
| GitHub Pages | Free hosting; updates after each push (~4 min) |
| Image target | The printed image the camera is trained to find (default QR in class) |
| `.glb` | 3D model file for the web |

---

*CHIO XR workshop · 8th Wall (open source) · A-Frame (MIT) · GitHub Pages*  
*Structure inspired by [aframe-image-targets-example](https://github.com/8thwall/aframe-image-targets-example) and community WebAR card projects*
