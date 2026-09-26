# FBLA Chapter Website Template

A website template for a Future Business Leaders of America chapter, built in plain HTML, CSS, and a little vanilla JS. There's no build step: open `index.html` in a browser and it works. It can be hosted anywhere, including GitHub Pages.

The layout is modeled on [fbla.org](https://www.fbla.org/). The colors, typography, and logos follow the official [FBLA Brand Center](https://www.fbla.org/brand-center/) guidelines.

## Pages

| File | Page |
|---|---|
| `index.html` | Home: hero, mission callout, quick links, "four ways to grow" cards, Save the Date, Get Involved |
| `about.html` | About: chapter story, the official FBLA mission, officers, and adviser |
| `events.html` | Events & Competitions: upcoming events list and competitive event categories |
| `join.html` | Join: why join, three steps to membership, and an FAQ |

## Make it yours

1. **Chapter details.** Search all four HTML files for text in square brackets, such as `[Chapter Name]`, `[School Name]`, `[State]` and `[Location]`, and replace it.
2. **Email addresses.** Replace `adviser@school.edu` and the officer addresses.
3. **Photos.** Each gray placeholder is a `<div class="photo">`. Replace its inner content with an image, for example `<div class="photo"><img src="assets/photos/team.jpg" alt="Our chapter at SLC"></div>`. The image fills the box automatically.
4. **Events.** Edit the list in `events.html`. Each event is one `<li class="event">`. The sample dates are placeholders, apart from the 2026 National Fall Leadership Conference.
5. **Social links.** The footer points to FBLA National's accounts. Swap in your chapter's.
6. **Membership form.** Point the "Membership form" link in `join.html` at your form.

The navbar and footer are copied into every page. When you edit one, edit it in all four files.

## Brand rules (from the FBLA Brand Guidebook)

The full guidebook is in `assets/brand/FBLA_Brand_Guidelines.pdf`.

**Colors.** Use only the official palette. The tokens are at the top of `css/styles.css`.

| Name | Hex | Use |
|---|---|---|
| Navy | `#0a2e7f` | headings, dark sections |
| Blue | `#1d52bc` | links, icons, subheads |
| Gold | `#f4ab19` | accents, primary buttons (with navy text) |
| Cobalt | `#226add` | accents on navy |
| White | `#ffffff` | backgrounds |
| Black | `#2d2b2b` | body text |

Gold isn't used for text on white backgrounds, because it doesn't have enough contrast to be readable.

**Typography.** The site uses Apercu Pro, the primary brand typeface, self-hosted in `assets/fonts/apercu-pro/`. Arial is the approved fallback.
- Bold is used for headlines.
- Medium in uppercase is used for subheads.
- Regular is used for body text.
- Medium is used for body text on dark backgrounds.

Gelasio, the serif option, is included for print materials only.

**Logo.**
- Never alter, recolor, stretch, or add effects to the logo.
- Never use the delta symbol on its own.
- Keep clear space equal to one sixth of the logo's width on all sides.
- On navy backgrounds, use the `color-Reverse` version.
- On blue backgrounds, use the all-white version.
- The favicon uses the FBLA Emblem, which the guide approves as a web and social icon.

**Your chapter logo.** The header shows the primary FBLA logo with a separate chapter label beside it, outside the clear space. For an official State + Chapter lockup, follow `assets/brand/FBLA_Logo_Customization_Guide_2023.pdf` or download a template from the Brand Center. Then replace `assets/logos/web/fbla-horizontal-color.png` in the header and remove the `.brand__chapter` label. Don't build your own lockup with CSS or text.

## Assets

```
assets/
├── brand/                 FBLA Brand Guidelines + Logo Customization Guide (PDF)
├── fonts/
│   ├── apercu-pro/otf/    Original Apercu Pro files (all weights)
│   ├── apercu-pro/woff2/  Web versions used by the site
│   └── gelasio/           Serif option (print), with its Open Font License
└── logos/
    ├── horizontal/            Official hi-res PNGs: color, color-Reverse, navy, white, black
    ├── horizontal-full-name/  Same five variations, with "Future Business Leaders of America"
    ├── vertical/              Same five variations, stacked
    ├── emblem/                FBLA Emblem (crest)
    └── web/                   Trimmed, web-sized copies used by the pages + favicons
```

The official logo files come from the FBLA Brand Center and keep their original file names. The `web/` folder holds trimmed, resized copies so pages load fast; they are not altered in any other way.

## Code structure

```
css/styles.css   All styles: fonts, brand tokens, components, responsive rules
js/main.js       Mobile menu, header shadow on scroll, footer year
```
