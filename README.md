# picklepath.ai.web

Marketing site for PicklePath.ai — AI-powered pickleball training.

**Live site (custom domain):** https://picklepath.ai  
**GitHub Pages (until DNS is pointed):** https://livatechllc.github.io/picklepath.ai.web/

## Pages the iOS app opens

| App extra | URL |
|---|---|
| `privacyPolicyUrl` | https://picklepath.ai/privacy |
| `termsUrl` | https://picklepath.ai/terms |

Those paths are `privacy/index.html` and `terms/index.html` so they work on GitHub Pages with or without a trailing slash.

## GitHub Pages

Repo Pages is already on: **Settings → Pages → Deploy from branch `main` / (root)**.

To serve `https://picklepath.ai`:

1. Merge this repo to `main`.
2. In the domain registrar, point `picklepath.ai` (and optionally `www`) at GitHub Pages:
   - Apex: `A` records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - or `ALIAS`/`ANAME` to `livatechllc.github.io`
3. In **Settings → Pages → Custom domain**, enter `picklepath.ai` (GitHub will commit a `CNAME` file). Turn on **Enforce HTTPS**.
4. Do not add a `CNAME` file until that DNS is ready — it will make the `github.io` URL follow the custom domain.

Until the custom domain resolves, App Store / in-app links will 404. Do not submit the app before that.

## Local preview

```bash
python3 -m http.server 8080
# http://localhost:8080
# http://localhost:8080/privacy/
# http://localhost:8080/terms/
```
