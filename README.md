# CreatorLedger

**Know your real profit. Never get wrecked at tax time.**

CreatorLedger is a financial back-office built for content creators. Income from YouTube, Twitch, Patreon, TikTok, and brand deals lands in one messy pile — no withholding, no clear picture of what's actually yours. CreatorLedger turns that pile into three numbers every creator needs: your **real take-home profit**, exactly how much to **set aside for taxes**, and your **quarterly estimated payment**.

This repository contains the landing page and the free **Creator Tax + True-Profit Calculator** — a zero-signup tool that gives creators an instant estimate right in the browser.

👉 **[Live demo](#)** _(add your deployed URL here)_

---

## What it does

### The free calculator
Enter what you expect to earn this year across each platform, plus your business expenses, filing status, and state. Instantly see:

- **Tax set-aside %** — the share of your income to hold back so April is never a surprise
- **Full breakdown** — self-employment tax (15.3%), federal income tax, and estimated state tax
- **Quarterly payment** — what to send the IRS each quarter to avoid underpayment penalties
- **Real take-home profit** — what's genuinely yours after expenses and taxes

Everything runs **client-side** — your income numbers never leave your browser.

### The tax model
- 2025 federal tax brackets (single / married-joint / head-of-household)
- Standard deduction per filing status
- Self-employment tax (12.4% Social Security up to the wage base + 2.9% Medicare on 92.35% of net earnings)
- The one-half self-employment-tax deduction
- A simplified, adjustable state income-tax estimate

> **Not tax advice.** The calculator is a planning estimate. It does not account for the QBI deduction, tax credits, exact state/local rules, or other income. Always confirm with a tax professional before filing.

---

## Roadmap

The calculator is a free preview of the full product. Planned:

- **Connect your platforms** — automatic income sync across YouTube/AdSense, Twitch, Patreon, TikTok, Stripe, Gumroad, and more
- **Real profit, always current** — one dashboard across every income source
- **Auto tax set-aside** — a running quarterly number that updates as you earn
- **Creator-specific deductions** — catch the write-offs generic tools miss
- **No QuickBooks required** — built for creators, not accountants

Join the waitlist from the site to get early access.

---

## Tech

- Single static `index.html` — no build step, no dependencies, no backend
- Vanilla HTML/CSS/JS with a glassmorphism dark theme (IBM Plex Sans)
- Accessible (labeled inputs, visible focus states, `prefers-reduced-motion`) and responsive down to 375px

## Run locally

Any static server works:

```bash
python3 -m http.server 5321
# then open http://localhost:5321
```

## Deploy

It's a single static file — drop it on **Netlify**, **Vercel**, **Cloudflare Pages**, or **GitHub Pages**.

To enable **GitHub Pages**: repo **Settings → Pages → Source: `main` / root**, then open the published URL.

## Collecting waitlist emails

The waitlist form works out of the box (it stores signups locally in the browser as a fallback). To capture real emails:

1. Create a free form at [Formspree](https://formspree.io).
2. In `index.html`, set the `FORMSPREE_ID` constant near the bottom of the `<script>` to your form ID.

That's it — submissions will then POST to your Formspree inbox.

---

## License

[MIT](LICENSE)
