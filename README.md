# emmellconsulting.com

Static one-page site for Emmell Consulting. No build step.

Files
- index.html — the whole site (HTML + CSS inline)
- images/ — the two photos, already compressed and greyscale
- CNAME — tells GitHub Pages the custom domain

Deploy on GitHub Pages
1. Create a repo in the organisation (e.g. `emmellconsulting/website`), upload these files to the root of `main`.
2. Repo → Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)`.
3. Settings → Pages → Custom domain: `emmellconsulting.com` → Save, then tick "Enforce HTTPS" once the certificate is issued (can take up to an hour).
4. Org → Settings → Pages → Verified domains → add `emmellconsulting.com` and add the TXT record it gives you.

DNS records to add in Microsoft 365 (Settings → Domains → emmellconsulting.com → DNS records). Do not change any existing record.
- A    @    185.199.108.153
- A    @    185.199.109.153
- A    @    185.199.110.153
- A    @    185.199.111.153
- CNAME www  <org-name>.github.io
- TXT  _github-pages-challenge-<org-name>  <value from step 4>

Editing text later: everything is plain HTML in index.html. Search for the sentence you want to change.
