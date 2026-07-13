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

All signature images live in `assets/` and are served by this repo's GitHub Pages site — signatures reference them by absolute URL, so they load for email recipients too:

- `midwestcards_horizontal_color.png` — logo (from the brand library, high-res)
- `insider_banner.png` — "Become a Midwest Insider" banner
- `icons/` — five social icons (Facebook, X, YouTube, LinkedIn, Instagram) and five contact icons (mobile, phone, email, address, website), gold, from the original team signature
- `headshots/` — team headshots (e.g. `kate.jpg`); add new ones here so everyone has a permanent photo URL

The address line links to Google Maps, and the signature ends with the full confidentiality disclaimer. To swap an image, replace the file **keeping the same filename** and push — Pages redeploys automatically.

⚠️ Don't rename or delete files in `assets/` — every signature already in use points at those URLs.
