# Midwest Cards — Email Signature Generator

A single-page tool for creating a consistent, branded Midwest Cards email signature. New team members fill in their details, hit **Copy signature**, and paste it into Gmail or Outlook.

**Live generator:** https://midwestcards.github.io/mwc-email-signature/

## For new team members

1. Open the [live generator](https://midwestcards.github.io/mwc-email-signature/) (or open `index.html` in a browser).
2. Fill in your name, title, phone, email, and pick your office location.
3. Optionally paste a public https link to your headshot.
4. Click **Copy signature**, then paste into your email client:
   - **Gmail:** Settings (gear) → See all settings → General → Signature → Create new → paste → Save changes.
   - **Outlook (web / new):** Settings → Mail → Compose and reply → paste → Save.
   - **Outlook (Windows desktop):** Use **Show HTML → Copy code**, or paste the rendered signature into File → Options → Mail → Signatures.

## For maintainers

Everything lives in `index.html` — no build step, no dependencies.

Team-wide defaults (company links, social URLs, office locations, disclaimer, brand colors, and image assets) live in the **CONFIG** block at the top of the `<script>` in `index.html`. Edit those once, commit, and everyone gets the update.

### Brand assets

The stacked Midwest Cards logo lives in `assets/` and is served by this repo's GitHub Pages site — signatures reference it by absolute URL, so it loads for email recipients too. Social links render as text in brand Secondary Blue (`#1E3E6B`), and the address links to Google Maps.

To add the Insider banner (330px wide): drop a PNG into `assets/`, set its URL in `CONFIG.assets.bannerUrl`, and push. Use PNG only — SVG won't render in Gmail/Outlook.

⚠️ Don't rename or delete files in `assets/` — every signature already in use points at those URLs.
