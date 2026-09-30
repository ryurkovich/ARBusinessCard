# Copy-paste prompts

Open the **agent chat** in Antigravity. Paste one prompt at a time. Wait until that step finishes before the next.

**Never** paste passwords, SSH private keys, or personal access tokens into chat.

---

## 1. Help me get started

Use this after your project folder is open (or if you are stuck cloning).

```
Help me get started with this CHIO XR AR Business Card workshop.

Please:
1. Read AGENTS.md and WORKSHOP_AGENT_CONFIG.md first and follow those rules.
2. Confirm this folder is the workshop project (index.html, models/, image-targets/, external/).
3. Check that the git remote uses HTTPS (https://github.com/...), not SSH (git@...). If it is SSH, tell me how to fix it with Antigravity UI only — do not ask me for keys or tokens.
4. If I do not have the project open yet, coach me step-by-step through: Use this template on GitHub → enable Pages (GitHub Actions) → Git: Clone with the HTTPS URL → Open the folder. Prefer the IDE Git: Clone command over terminal git.
5. Quietly verify the project is ready. If Node.js is already installed, you may run any needed install in the background without teaching me npm. If Node is missing, skip installs and rely on GitHub Pages — do not make me install Node unless I ask.
6. Never ask for passwords, PATs, or SSH private keys.
7. When ready, reply with one short sentence that I am ready for the next prompt: Add my custom model.
```

---

## 2. Add my custom model (core personalization)

First drag your `.glb` into `models/custom/` in the file tree, then paste this (replace the filename):

```
I added my Poly Pizza model file to models/custom/. The filename is: YOUR-FILE.glb

Please personalize the project:
1. Read AGENTS.md / WORKSHOP_AGENT_CONFIG.md and explain each change before you make it.
2. Register the file in index.html <a-assets> as id="custom-model" pointing at ./models/custom/YOUR-FILE.glb
3. Set gltf-model="#custom-model" on the #active-model entity.
4. Choose a sensible default scale (start around 0.2 0.2 0.2) and position so it sits above the QR.
5. Optionally add custom-model to the double-tap models array so I can cycle to it later.
6. Do NOT change image-targets, targetData, or anything under external/.
7. Show me the exact lines you changed.
```

### Fallback (only if your download failed)

```
My custom model download failed. Set the active model in index.html to #crystal-model
(or ask me which bundled model I prefer). Explain the one-line change. Do not touch image targets.
```

---

## 3. Commit and publish

```
Guide me to publish my change with the Antigravity Source Control UI (not the terminal).

Steps I need coached through:
1. Open Source Control
2. Write a short commit message like: add my custom model
3. Click Commit
4. Click Sync Changes / Push
5. Tell me how to watch the Actions tab and when to open
   https://MY-USERNAME.github.io/chio-xr-ar-business-card on my phone

Remind me: I click the buttons; you do not need my GitHub password or any keys.
After push, remind me to scan the printed DEFAULT QR from the workshop (not a new Canva QR yet).
```

---

## Take-home prompts (optional stretch)

### Wire a Canva QR as a new image target

```
I generated a new QR PNG that points at my GitHub Pages URL and saved it in the project.
Help me update the image target using the 8th Wall image-target CLI workflow described in AGENTS.md.
Explain each step. Do not ask for secrets. Keep HTTPS remotes only.
```

### Place the QR on the business card template

```
Show me where the CHIO XR business card template is (assets/business-card/) and how to
insert my QR into the "Insert your QR code here" area using Canva or a simple image editor.
Keep instructions non-technical and step-by-step.
```
