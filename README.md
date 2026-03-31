# Game Night Companion

A phone-friendly board game strategy and rules advisor — free, powered by Groq + Llama 3.

## Setup

### 1. Get a free Groq API key
Sign up at https://console.groq.com — no credit card required.

### 2. Add your key to config.js
Edit `config.js` and replace the placeholder:
```js
const GROQ_API_KEY = 'gsk_xxxxxxxxxxxxxxxx';
```

> `config.js` is in `.gitignore` — it will never be pushed to GitHub. Your key stays local only.

### 3. Push to GitHub (without config.js)
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/game-companion.git
git push -u origin main
```

### 4. Enable GitHub Pages
Go to your repo → Settings → Pages → Deploy from branch → main → root → Save

Your app will be live at: `https://YOUR_USERNAME.github.io/game-companion`

### 5. Use on your phone
On devices where you want it to work, you need `config.js` locally.

**Best phone workflow:**
- Clone the repo on your phone or PC
- Add `config.js` with your key
- Run locally: `python -m http.server 8000`
- Bookmark `http://localhost:8000` on your phone (on same WiFi)

Or just open the app before game night on your PC and keep the tab open.

## Features
- Load your full BGG collection by username — tap to select games
- Opening strategy tailored to player count
- Common beginner mistakes
- Faction / character advice
- Rules Q&A with optional rule text paste
- Dark mode support

## Notes
- Groq's free tier is very generous for personal use
- PDF upload removed (Groq doesn't support document inputs) — use the paste-a-rule box instead
- For rules disputes mid-game, paste the exact rule text for the most accurate answer
