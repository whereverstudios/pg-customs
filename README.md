# PG Customs — site redesign

Wherever Studios redesign of [pgcustommade.com](https://www.pgcustommade.com/) (PG Customs, Phil Gielow, Gardnerville NV).
A single self-contained `index.html` with no build step; photos live in `media/`.

## Run it

```bash
node serve.mjs 4326
```

Then open http://localhost:4326/. Any static host works (GitHub Pages, Netlify, Squarespace replacement, etc.): upload `index.html` and `media/`.

## What changed from the Squarespace site

- One long, image-led page instead of Home / About / Contact. Everything the old site said is still here, reorganised:
  hero → facts strip → selected work → what we build → process + film → Phil → client quotes → start a project.
- Copy rewritten in a plainer voice around the true story: three generations on the Gielow ranch, Tahoe-sourced lumber, hand-assembled, Phil does it all himself.
- All photos are Phil's own stills from the existing site and film, re-exported for the web. The horseshoe mark is the existing white PNG (inverted with CSS on light backgrounds).
- Film: click-to-play YouTube embed (`XnMLmF_CteQ`), poster first so nothing loads until asked.
- Contact form composes an email to phil@pgcustommade.com in the visitor's mail app. Swap the submit handler for Formspree / Netlify Forms if Phil wants submissions without a mail client.
- Structured data (LocalBusiness), Open Graph image, SVG favicon.

## To confirm with Phil before launch

- Project locations in captions are inferred from the testimonials (bed frame → Gardnerville, dining table → Stateline, pergola → South Lake Tahoe). Correct any that are wrong.
- The four process steps are drafted from how the old site describes the work. Phil should check they match how he actually quotes and delivers.
- Testimonial quotes are short excerpts from the old site; full originals are worth pulling from his records if he wants longer ones.
- Service area copy says Carson Valley, Lake Tahoe and Northern Nevada. Add Reno or California towns if he works there.
- The old site had a cart link with nothing behind it; it was dropped. Reinstate only if he actually sells stock pieces.
- `media/src/` holds the original downloads (gitignored). Better photography of finished pieces is the single biggest upgrade available to this page.
