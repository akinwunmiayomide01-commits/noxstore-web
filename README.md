# Noxstore Web 🎮

> Single-file web version of Noxstore — open in VS Code, push to GitHub, done.

## Setup (30 seconds)

1. Open `index.html` in VS Code
2. Change the backend URL on line ~5 of the `<script>` tag:
   ```js
   const BASE_URL = 'http://localhost:5000'; // ← your backend URL
   ```
3. Open with Live Server extension or just double-click the file

## Push to GitHub

```bash
git init
git add .
git commit -m "feat: Noxstore web MVP"
git remote add origin https://github.com/YOUR_USERNAME/noxstore-web.git
git push -u origin main
```

## Deploy Free (no server needed for frontend)

- **Vercel**: drag the folder to vercel.com
- **Netlify**: drag the folder to netlify.com  
- **GitHub Pages**: push to GitHub → Settings → Pages → Deploy from main

## Screens

| Screen | How to reach it |
|---|---|
| Splash | App start |
| Auth | Auto after splash (if not logged in) |
| Home | After login |
| Top-Up | Click any game |
| Payment | Click "Proceed to Pay" |
| Success | After Paystack callback |

## Dev Shortcut

Press `Shift + D` anywhere in the app to skip login and jump to Home screen.
Remove that block before going live.

## API Contract (same as Flutter version)

```
POST /api/auth/register    { email, password }
POST /api/auth/login       { email, password }
POST /api/payments/initialize  { amount, game }
```

Built by NOXAXIS Ltd
