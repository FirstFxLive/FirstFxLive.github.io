# fx2live.com

Marketing website for **fx2live** — *First Experience to Live* — AI-powered daycare
& childcare management software. Static HTML/CSS/JS, no build step required.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Homepage — hero, feature overview, AI section, testimonials, pricing teaser |
| `features.html` | Full feature tour (attendance, billing, communication, reports, staff, enrollment, health, analytics) |
| `ai.html` | FX2 Copilot — AI features & responsible-AI commitments |
| `pricing.html` | Plans (Sprout / Bloom / Thrive) + pricing FAQ |
| `about.html` | Company story & principles |
| `contact.html` | Contact info + demo request form (opens a pre-filled email) |
| `terms.html` | Terms of Service |
| `privacy.html` | Privacy Policy |
| `404.html` | Custom not-found page (served automatically by GitHub Pages) |

Shared assets live in `css/styles.css` and `js/main.js`.

## Deploying to GitHub Pages

1. Create a GitHub repository (e.g. `fx2live-site`) and push this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial fx2live.com website"
   git branch -M main
   git remote add origin https://github.com/<your-user>/fx2live-site.git
   git push -u origin main
   ```
2. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / root**.
3. The included `CNAME` file already points to `fx2live.com`. At your DNS provider:
   - `A` records for the apex `fx2live.com` → GitHub Pages IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `<your-user>.github.io`
4. Back in **Settings → Pages**, enter `fx2live.com` as the custom domain and
   enable **Enforce HTTPS** once the certificate is issued (can take up to an hour).

## Before launch checklist

- [ ] Replace the placeholder testimonials on `index.html` with real customer quotes.
- [ ] Have an attorney review `terms.html` and `privacy.html` — they are solid
      starting drafts, not legal advice.
- [ ] Wire the contact form to a form service (e.g. Formspree) if you want
      submissions captured server-side instead of the current mailto flow —
      see the inline note in `contact.html`.
- [ ] Confirm pricing numbers on `pricing.html` / `index.html`.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python -m http.server 8000
# → http://localhost:8000
```
