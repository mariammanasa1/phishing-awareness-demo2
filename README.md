# Phishing Awareness Demo

## Deploy

This package is shaped for Cloudflare Workers with static assets.

Expected Cloudflare deploy command:

```sh
npx wrangler deploy
```

## Test

After deployment, open:

```text
https://YOUR-CLOUDFLARE-DOMAIN/login.html
```

To test click logging:

```text
https://YOUR-CLOUDFLARE-DOMAIN/click?rid=test001
```

The `/click` route logs `training_link_click`, then redirects to `login.html`.

## Email Link

Use a unique `rid` per recipient:

```html
<a href="https://YOUR-CLOUDFLARE-DOMAIN/click?rid=EMPLOYEE001">photo</a>
```

## Optional D1 Table

If you bind a D1 database as `DB`, create:

```sql
CREATE TABLE clicks (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  recipient_id TEXT NOT NULL,
  clicked_at TEXT NOT NULL,
  country TEXT,
  city TEXT,
  user_agent TEXT,
  referer TEXT
);
```
