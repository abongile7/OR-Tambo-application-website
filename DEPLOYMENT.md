# Demo deployment options

## Quickest: Netlify drag-and-drop (no CLI required)
1. Open https://app.netlify.com/drop
2. Zip this project folder and drop it on the page.
3. Netlify will immediately publish a shareable URL.
4. Optional: click **Site settings → Domain management** to rename the site.

## Netlify CLI (if you have an account + token)
```bash
npm i -g netlify-cli
netlify login
netlify deploy --prod --dir=.
```

## URLs after deploy
- `/` opens `index.html` directly (stable default behavior on Netlify).
- `/applicant-manage-applications` rewrites to `index.html`.
- `/applicant-manage-applications-demo.html` remains directly accessible.

## If you still see a Netlify error page
- Trigger a **Clear cache and deploy site** from Netlify Deploys.
- Confirm the deploy is using this repo root as the publish content.
- Verify `index.html` exists in the published output (Deploy details → files).
