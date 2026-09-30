# Instructor Guide — CHIO XR AR Business Card

Use this to build your slides and run the room. Learners follow [`LEARNER_GUIDE.md`](LEARNER_GUIDE.md) and [`PROMPTS.md`](PROMPTS.md).

**Session design:** ~30 minutes facilitated hands-on; expect Q&A to fill remaining time. Interleave short slides with live demos.

**Template URL (put on every relevant slide + chat):**
```
https://github.com/[INSTRUCTOR-ORG]/chio-xr-ar-business-card
```

---

## Before the event

### Publish checklist
- [ ] Repo is public and marked as a **Template repository** (GitHub → Settings → General → Template repository)
- [ ] GitHub Pages works on the instructor copy (Actions → green deploy)
- [ ] Print [`assets/print/default-qr-code.png`](assets/print/default-qr-code.png) — one per table (or per person)
- [ ] Optional: print blank [`assets/business-card/chio-xr-card-template.png`](assets/business-card/chio-xr-card-template.png) for take-home talk track
- [ ] Dry-run on a fresh GitHub account: template → HTTPS clone → custom `.glb` → push → phone scan
- [ ] Send [`PREWORK.md`](PREWORK.md) 3–5 days ahead
- [ ] Confirm Antigravity download link (non-agents installer)

### Screenshots to capture for slides
1. GitHub **Use this template**
2. Pages → Source **GitHub Actions**
3. Antigravity **Sign in with GitHub** (browser OAuth)
4. Green **Code** → **HTTPS** URL (highlight `https://`, warn against `git@`)
5. Command Palette **Git: Clone**
6. Drag `.glb` into `models/custom/`
7. `index.html` lines: `custom-model` asset + `gltf-model="#custom-model"`
8. Source Control Commit + Sync
9. Actions green check
10. Phone AR over printed QR

---

## Slide outline + speaker notes

Switch to **DEMO** when marked. Keep slides sparse: one idea per slide.

### Slide 1 — Title
**Title:** CHIO XR · AR Business Card  
**Point:** Build a real WebAR link in ~30 minutes.  
**Note:** Welcome; phones out later; laptops ready.

### Slide 2 — What you will leave with
**Point:** A URL you own + your 3D model on a shared QR.  
**Visual:** Phone mock / live photo.  
**Note:** Personalization = *their* Poly Pizza model, not picking a stock one only.

### Slide 3 — DEMO: finished experience
**DEMO:** Open instructor Pages URL → scan printed default QR → show model + pinch.  
**Note:** “Same QR for everyone today. Your model is what makes it yours.”

### Slide 4 — How it works (30 seconds)
**Point:** Phone browser + camera + image target + 3D file.  
**Note:** `index.html` is the whole app. No App Store.

### Slide 5 — Prework check
**Point:** GitHub account · Antigravity · signed in · `.glb` downloaded.  
**Note:** Raise hands for blockers; helpers roam.

### Slide 6 — Sign in to GitHub the safe way
**Point:** Browser OAuth inside Antigravity. Never paste keys into AI chat.  
**Visual:** Sign-in screenshot.  
**Note:** Explicitly ban SSH-key-in-chat.

### Slide 7 — DEMO: Use this template
**DEMO:** Click **Use this template** → public repo → create.  
**Note:** Prefer template over fork language for first-timers.

### Slide 8 — DEMO: Enable Pages
**DEMO:** Settings → Pages → GitHub Actions.  
**Note:** Do this before first push. Write URL pattern on slide.

### Slide 9 — DEMO: Easy HTTPS clone
**DEMO:** Code → HTTPS → copy → `Git: Clone` → Open.  
**Note:** Call out if anyone’s URL starts with `git@` — stop and switch to HTTPS.

### Slide 10 — Prompt 1: Help me get started
**Point:** Paste prompt from `PROMPTS.md`. Agent checks project quietly.  
**Note:** They should not learn npm today.

### Slide 11 — Drop your model
**Point:** Drag `.glb` into `models/custom/`.  
**DEMO:** Show drag once.

### Slide 12 — Prompt 2: Add my custom model
**Point:** Paste prompt with real filename.  
**Note:** Fallback prompt if no file — bundled model — then continue to deploy.

### Slide 13 — Prompt 3: Commit and publish
**DEMO:** Source Control → commit message → Commit → Sync.  
**Note:** Learners click; agent coaches. Watch Actions.

### Slide 14 — Phone test
**Point:** Safari (iOS) / Chrome (Android) · allow camera · printed default QR.  
**Note:** Roam; light and framing tips.

### Slide 15 — You did it + take-home teaser
**Point:** Celebrate. Stretch: Canva QR → retarget → CHIO XR card template.  
**Note:** Point to Learner Guide stretch section; end for Q&A.

---

## 30-minute facilitation clock

| Min | Mode | Beat |
|----:|------|------|
| 0–4 | Slide + DEMO | Title + live finished demo |
| 4–10 | DEMO + room | Template + Pages + HTTPS clone |
| 10–14 | Hands-on | Help me get started |
| 14–22 | Hands-on | Custom `.glb` + commit/sync |
| 22–30 | Hands-on | Phone scan + buffer / early Q&A |

---

## Troubleshooting cheat sheet

| Symptom | Likely cause | Fix |
|---------|--------------|-----|
| Clone asks for password / fails | Not signed into GitHub in IDE; or SSH URL | Sign in with GitHub; re-copy **HTTPS** URL |
| `git@github.com:...` | SSH clone | Code button → HTTPS; re-clone |
| 404 on Pages | Pages not enabled; Actions still running | Settings → Pages → Actions; wait / re-run job |
| Old model still shows | Cache or deploy not done | Wait for green Actions; hard-refresh |
| No model / tracking fails | Wrong QR; lighting; partial QR | Use printed workshop QR; full frame; brighter light |
| Model huge or tiny | Scale | Agent: try `0.2 0.2 0.2`; pinch on device |
| Huge `.glb` push slow | File too large | Suggest smaller Poly Pizza model; fallback bundled |
| Camera blocked | Wrong browser / permission | iOS Safari; Android Chrome; reset site permissions |
| Agent asks for a token | Bad prompt / confused agent | Stop; remind: OAuth only; re-paste Help me get started |

---

## Handouts
- Printed **default QR** (`assets/print/default-qr-code.png`) — required for core path  
- Optional blank **CHIO XR card** (`assets/business-card/chio-xr-card-template.png`)  
- Chat paste: template URL + link to `PROMPTS.md` on their repo after clone  

---

## Credits to mention (briefly)
8th Wall engine · A-Frame · GitHub Pages · Poly Pizza for models · structure from community WebAR image-target examples
