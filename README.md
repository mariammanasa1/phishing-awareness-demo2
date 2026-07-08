# Cloudflare Worker Deploy

This repo layout is intentionally simple:

```text
wrangler.jsonc
worker.js
public/login.html
public/rick-roll-video-meme-template-video-1da252ec.mp4
```

Cloudflare deploy command:

```text
npx wrangler deploy
```

Test after deploy:

```text
https://YOUR-DOMAIN/login.html
https://YOUR-DOMAIN/click?rid=test001
```

Use this in the email:

```html
<a href="https://YOUR-DOMAIN/click?rid=EMPLOYEE001">photo</a>
```
