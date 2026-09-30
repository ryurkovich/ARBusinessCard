# Publish checklist — instructor template repo

Local workshop files are ready. An initial `main` commit already exists in this folder.
You still need to authenticate `gh` once, create the remote, and mark it as a Template.

## 0. Sign in to GitHub CLI (one time)

```bash
gh auth login --hostname github.com --git-protocol https --web
```

Use the browser OAuth flow. Do not paste tokens into an AI chat.

## 1. Create the GitHub repo and push

```bash
cd /Users/ohitson/Documents/GitHub/ARBusinessCard
gh repo create chio-xr-ar-business-card --public --source=. --remote=origin --push
```

Replace the owner if you use an org:
```bash
gh repo create YOUR-ORG/chio-xr-ar-business-card --public --source=. --remote=origin --push
```

## 2. Mark as a Template repository

GitHub → repo **Settings** → **General** → check **Template repository** → Save.

Learners will use **Use this template** (not Fork).

## 3. Enable GitHub Pages on the instructor copy

**Settings → Pages → Source: GitHub Actions**

Confirm `.github/workflows/deploy.yml` runs green on `main`.

Instructor demo URL:
```
https://[owner].github.io/chio-xr-ar-business-card
```

## 4. Print handouts

- `assets/print/default-qr-code.png` — required for the 30-minute core path  
- Optional: `assets/business-card/chio-xr-card-template.png`

## 5. Dry-run (fresh account or private browser profile)

1. Use this template → public repo  
2. Enable Pages (GitHub Actions)  
3. Sign in to GitHub in Antigravity (browser OAuth)  
4. HTTPS Git: Clone → Open  
5. Paste **Help me get started**  
6. Drop a Poly Pizza `.glb` into `models/custom/`  
7. Paste **Add my custom model**  
8. Commit + Sync  
9. Wait for Actions → open Pages URL on phone → scan **printed default QR**

## 6. Share with learners

- Prework link: `PREWORK.md`  
- Template URL on slides + chat  
- Day-of: `PROMPTS.md` after clone  

## Security reminders for the room

- HTTPS remotes only  
- Sign in with GitHub in the IDE  
- Never paste SSH private keys or PATs into the agent chat  
