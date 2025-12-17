# Trillo

Trillo is a responsive, visually polished landing website that demonstrates a modular UI built with semantic HTML, SASS (SCSS) and lightweight vanilla JavaScript. The project showcases a clean layout, reusable components and a design system powered by SASS variables and mixins so you can quickly iterate on themes, spacing and responsive behavior.

---

## What you'll see

- A multi-section landing page with hero, overview, gallery, details and reviews sections.
- Responsive grid and layout utilities that adapt across mobile, tablet and desktop.
- Polished UI interactions implemented in `public/js/app.js` (no heavy frameworks).
- A curated set of imagery and SVG icons in `public/img/` and `public/img/SVG/`.

---

## SASS-first architecture

This project uses SASS to organize styles into a small, maintainable design system:

- `sass/abstracts/` — variables (`_variables.scss`) and reusable mixins/functions (`_mixins.scss`). Change colors, fonts, and breakpoints here to update the whole site.
- `sass/base/` — global base styles and typography.
- `sass/components/` — self-contained UI components (buttons, gallery, reviews, calls-to-action).
- `sass/layout/` — grid and structural styles (header, navigation, layout utilities).
- `sass/main.scss` — the entry file that imports the partials and produces the compiled stylesheet.

Benefits you get out of the box:

- Centralized theme control via variables (colors, spacing, font-sizes, breakpoints).
- Encapsulated component styles so components can be reused or extracted easily.
- Utility mixins for responsive rules, clearfixes and vendor prefixes.

---

## Where files live

- `public/index.html` — the HTML markup served to browsers.
- `public/css/style.css` — compiled stylesheet generated from `sass/main.scss`.
- `public/js/app.js` — lightweight client-side behaviors.
- `public/img/` and `public/img/SVG/` — images and SVG icon assets.
- `sass/` — SASS source files and partials.
- `firebase.json` — hosting configuration (if you deploy to Firebase).

---

## Quick commands

Compile SASS once (produces `public/css/style.css`):

```
npx sass sass/main.scss:public/css/style.css
```

Watch SASS and rebuild on change (development):

```
npx sass --watch sass/main.scss:public/css/style.css
```

Preview the site locally (serve `public/`):

```
npx http-server public -p 8080
```

Or:

```
npx serve public -l 8080
```

Deploy to Firebase Hosting:

```
firebase login
firebase deploy --only hosting
```

(If not configured, run `firebase init hosting` first.)

---

## How to customize the look

1. Start by editing `sass/abstracts/_variables.scss` to set brand colors, base font sizes and breakpoints.
2. Use or add mixins in `sass/abstracts/_mixins.scss` for responsive helpers and shared patterns.
3. Add or modify component files in `sass/components/` and import them into `sass/main.scss`.
4. Rebuild the compiled CSS and refresh the browser to see changes.

Tip: keep small, focused partials for each component so styles remain easy to maintain and reuse.

---

## Contributing

Contributions are welcome. For style or layout changes, update SASS partials and the compiled CSS, test across viewports, then open a pull request describing the visual and structural changes.

---

## License

Add a `LICENSE` file to this repository and indicate the chosen license there.

---

Author: mostafaEkbal
