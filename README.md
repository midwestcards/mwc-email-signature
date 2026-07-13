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

### One-time branding setup

The signature currently uses a text **MIDWEST CARDS** wordmark and text social links, so it's already usable. For the full branded look, host these images at permanent public URLs and paste them into `CONFIG.assets`:

- Logo (124px wide, PNG)
- Insider banner (330px wide, PNG)
- Optional: four social icons (16px) and four contact icons (12px)

Use PNG only — SVG won't render in Gmail/Outlook.
