# PG Customs — site redesign

Wherever Studios redesign of [pgcustommade.com](https://www.pgcustommade.com/) (PG Customs, Phil Gielow, Gardnerville NV).
A single self-contained `index.html` with no build step; photos live in `media/`.

## Run it

```bash
node serve.mjs 4326
```

Live preview: https://whereverstudios.github.io/pg-customs/ (GitHub Pages from `main`, root). When the real domain moves here, update the `og:image` URL in `index.html` to pgcustommade.com.

Then open http://localhost:4326/. Any static host works (GitHub Pages, Netlify, Squarespace replacement, etc.): upload `index.html` and `media/`.

## What changed from the Squarespace site

- One long, image-led page instead of Home / About / Contact. Everything the old site said is still here, reorganised:
  hero → facts strip → selected work → what we build → process + film → Phil → client quotes → start a project.
- Copy rewritten in a plainer voice around the true story: three generations on the Gielow ranch, Tahoe-sourced lumber, hand-assembled, Phil does it all himself.
- All photos are Phil's own stills from the existing site and film, re-exported for the web. The horseshoe mark is the existing white PNG (inverted with CSS on light backgrounds).
- Hero: the old site's own Squarespace background loop ("PG Customs - Website Loop.mp4", 35 s) pulled from its HLS stream and re-encoded muted: `media/hero-loop.mp4` (1440w, ~5 MB) for desktop, `media/hero-loop-small.mp4` (960w, ~2 MB) under 760px, `media/hero-poster.jpg` as the first frame. Pauses itself under prefers-reduced-motion or when autoplay is blocked; visitors get a Pause/Play control. The 1080p source sits in `media/src/` (gitignored).
- Film: click-to-play YouTube embed (`XnMLmF_CteQ`), poster first so nothing loads until asked.
- Contact form composes an email to phil@pgcustommade.com in the visitor's mail app. Swap the submit handler for Formspree / Netlify Forms if Phil wants submissions without a mail client.
- Structured data (LocalBusiness), Open Graph image, SVG favicon.

## Positioning

Contractor first: decks, pergolas and outdoor living, then remodels, built-ins and additions, with custom furniture as the third service. Calls to action are "Get a quote" / "Request a site visit" and the form is a quote request. Schema type is HomeAndConstructionBusiness.

## To confirm with Phil before launch

- **Nevada contractor license.** If Phil holds an NSCB license, add the number near the footer and the quote form; it is the single biggest trust signal for a contractor site. If he does not, keep the copy as is (it never claims "licensed").
- **Deck and remodel photos.** The only outdoor project photo on hand is the South Lake pergola; there are no deck, remodel or built-in photos at all, so the project grid currently leans on furniture and shop shots. Before/after deck rebuilds would transform the page.
- Process copy (site visit, written quote and timeline, final walk-through) describes a standard contractor flow; confirm it matches how Phil works.

- Project locations in captions are inferred from the testimonials (bed frame → Gardnerville, dining table → Stateline, pergola → South Lake Tahoe). Correct any that are wrong.
- The four process steps are drafted from how the old site describes the work. Phil should check they match how he actually quotes and delivers.
- Testimonial quotes are short excerpts from the old site; full originals are worth pulling from his records if he wants longer ones.
- Service area copy says Carson Valley, Lake Tahoe and Northern Nevada. Add Reno or California towns if he works there.
- The old site had a cart link with nothing behind it; it was dropped. Reinstate only if he actually sells stock pieces.
- `media/src/` holds the original downloads (gitignored). Better photography of finished pieces is the single biggest upgrade available to this page.
