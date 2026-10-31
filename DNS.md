# Connect truedreamsconsultant.com (GoDaddy) → GitHub Pages

1. Create a public GitHub repo and upload everything in this folder (index.html, assets/, CNAME, .nojekyll) to the repo root.
2. Repo → Settings → Pages → Source: Deploy from branch → `main` / `(root)`. Custom domain: `truedreamsconsultant.com` → Save. Tick "Enforce HTTPS" once available.
3. GoDaddy → My Products → truedreamsconsultant.com → DNS. Delete the existing `@` A record ("Parked") and any `www` record / domain forwarding, then add:

| Type  | Name | Value                         | TTL    |
|-------|------|-------------------------------|--------|
| A     | @    | 185.199.108.153               | 1 hour |
| A     | @    | 185.199.109.153               | 1 hour |
| A     | @    | 185.199.110.153               | 1 hour |
| A     | @    | 185.199.111.153               | 1 hour |
| CNAME | www  | Gawhar143.github.io | 1 hour |

(Optional IPv6: AAAA @ → 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153)

4. Wait 10 min – 24 h. Both truedreamsconsultant.com and www.truedreamsconsultant.com will load the site; HTTPS is free.

## Alternative: Cloudflare Pages
Upload this folder in Cloudflare → Workers & Pages → Pages, add the domain to Cloudflare (free), change GoDaddy nameservers to the two Cloudflare gives you, then add both domains under Custom domains.
