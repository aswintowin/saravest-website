# Saravest website

Single self-contained static page (`index.html`) — no build step, no dependencies. Fonts load from Google Fonts; everything else (colors, layout, the founder photo, the SVG logomark) is inline.

## Deploy — no install needed (fastest)

**Netlify (drag-and-drop):**
1. Go to https://app.netlify.com/drop
2. Drag the `saravest-website` folder onto the page.
3. Netlify gives you a live URL immediately (e.g. `random-name-123.netlify.app`).

**Vercel (dashboard import):**
1. Go to https://vercel.com/new
2. Choose "Deploy without Git" / drag-and-drop the folder, or push this folder to a GitHub repo first and import it.
3. Vercel auto-detects it as a static site — no build settings needed.

## Deploy via CLI (if you'd rather script it)

Neither CLI is installed in this environment. To use one, install it yourself first:

```bash
# Netlify
npm install -g netlify-cli
netlify deploy --prod --dir=.

# Vercel
npm install -g vercel
vercel --prod
```

Both will ask you to log in (browser OAuth) on first use.

## Custom domain

Once deployed:
- **Netlify:** Site settings → Domain management → Add a domain. Point your registrar's DNS (A/ALIAS or CNAME, Netlify tells you which) at Netlify.
- **Vercel:** Project → Settings → Domains. Same idea — add the domain, then update DNS as instructed.

Either platform issues a free HTTPS certificate automatically once DNS is pointed correctly (can take a few minutes to a few hours to propagate).

## Updating the site later

This file is a straight export of the version published as a Claude Artifact. To update:
1. Make the change in `index.html` directly, **or**
2. Ask Claude to update the artifact, then re-export it here the same way (wrap the artifact body in `<!DOCTYPE html><html><head>...</head><body>...</body></html>`).

Re-deploy by dragging the folder again (Netlify Drop) or running the CLI deploy command again — both create a new deployment without touching your DNS/domain setup.

## Known placeholder

The office address in the contact section is still a placeholder ("Amaravathi – Vijayawada Road, Andhra Pradesh, India") — replace it with the real address before going live.
