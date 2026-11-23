# kixel.me

Luke Curley's links page: a big hand-drawn cat that watches your cursor, and links grouped as MoQ, Company, Misc, and Social.

It's static files served by Cloudflare static assets, with no build step:

```
public/
  index.html   the whole page
  avatar.svg   the cat, traced from the GitHub avatar; also the favicon
```

The page draws the cat with `<use href="/avatar.svg#...">`, so the eyes move on their own.
Edit the art in `avatar.svg` and keep the `body`, `eye-l`, and `eye-r` ids.

## Develop

```bash
bun install
bun run dev      # http://localhost:8788
```

## Deploy

```bash
bun run deploy
```

`wrangler.jsonc` claims `kixel.me` as a custom domain.
