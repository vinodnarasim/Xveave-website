# Xveave.com

Static marketing site for Xveave Technologies. Plain HTML/CSS — no build step, no dependencies.

## Structure

- `index.html` — home
- `what-we-build.html`, `technology.html`, `industries.html`, `about.html`, `contact.html`
- `innovations/` — index + one page per innovation
- `assets/style.css` — all styling (design tokens at the top)
- `sitemap.xml`, `robots.txt`, `CNAME`, `404.html`

## Deploy to GitHub Pages

1. Create a repo (e.g. `xveave-site`), push these files to the `main` branch root.
2. Repo → Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. In the Custom domain field enter `xveave.com` (the CNAME file here keeps it set).
4. At your domain registrar, add DNS records:
   - **A records** for the apex `xveave.com`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - **CNAME record** for `www` → `<your-github-username>.github.io`
5. Back in Pages settings, tick "Enforce HTTPS" once the certificate is issued (can take up to an hour after DNS propagates).

## Contact form

The form posts to Formspree. Create a free form at formspree.io, then replace `YOUR_FORM_ID` in `contact.html` with your form ID. Until then the form will not submit.

## Before launch checklist

- [ ] Replace `YOUR_FORM_ID` in contact.html
- [ ] Add the LinkedIn company URL (footer + contact page, currently `#`)
- [ ] Set up info@xveave.com (Zoho Mail free tier or Google Workspace) and its MX records
- [ ] Add real product screenshots to the Implementation Accelerator page
- [ ] Review Selective Distribution Management copy against actual POC scope

## Editing

Pages share their header/footer markup by duplication — if you change navigation, change it in every file (a find-and-replace across *.html does it). Design tokens (colors, fonts, spacing) live at the top of `assets/style.css`.
