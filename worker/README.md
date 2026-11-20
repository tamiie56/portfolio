# Mr. Cold Coffee — Cloudflare Worker (Workers AI)

Model: `@cf/meta/llama-3.2-3b-instruct` (3.21B parameters)

## Deploy (CLI)
```
cd worker
npx wrangler login
npx wrangler deploy
```
Deploy hole URL pabe: `https://mr-cold-coffee.<tomar-subdomain>.workers.dev`

## Deploy (Dashboard, CLI chhara)
1. Cloudflare Dashboard → Workers & Pages → Create → Worker → `index.js` er code paste → Deploy
2. Worker → Settings → Bindings → Add → **Workers AI** → Variable name: `AI`
3. (Optional) Rate limit: Bindings → Rate limiting → name `RL`, 12 requests / 60s

## Site e connect
`index.html` e `var AI_URL = '...'` er moddhe oi Worker URL boshao.

## Notes
- `ALLOWED_ORIGINS` (index.js) e tomar site + localhost (jekono port) allowed. Notun domain hole add koro.
- Tamim er info change hole `FACTS` block update koro.
- Free plan: 10,000 Neurons/day — portfolio chatbot er jonno enough.
