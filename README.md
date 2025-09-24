# Voice Backend (Render-ready)

A tiny Node server that mints short-lived OpenAI Realtime client tokens for your website voice widget.

## Quick start (local)
1) Install deps:
   ```bash
   npm install
   ```
2) Set your API key and run:
   ```bash
   export OPENAI_API_KEY="sk-..."
   node server.js
   ```
3) Test:
   - Open http://localhost:3000/  -> should say "OK"
   - Open http://localhost:3000/token -> should return {"client_secret":"..."}

## Deploy to Render
1) Create a new **Web Service** on Render and connect this folder (or upload).
2) Set:
   - Build Command: `npm install`
   - Start Command: `node server.js`  (or `npm start`)
   - Environment Variable: `OPENAI_API_KEY` = your key
3) Deploy. Copy the HTTPS URL, e.g. `https://your-app.onrender.com`.
4) In your site snippet, use: `https://your-app.onrender.com/token`.
