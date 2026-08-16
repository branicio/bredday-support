# BredDay Support

Support website for the BredDay iOS & Android apps — livestock gestation & breeding calculator.

Hosted via GitHub Pages at: https://branicio.github.io/bredday-support/

## Pages

- [Support](https://branicio.github.io/bredday-support/) — landing page (contact + links) (`index.html`)
- [Privacy Policy](https://branicio.github.io/bredday-support/privacy.html) (`privacy.html`)
- [Terms of Use](https://branicio.github.io/bredday-support/terms.html) (`terms.html`)

## Languages

Every page is trilingual — English, Português (Brasil), Español — following the
Pew Pal / Solshield support-site pattern: the three languages are stacked in
`[data-lang]` sections on one page, and `site.js` shows exactly one of them.

- Language picked by, in priority order: URL fragment → stored choice
  (`localStorage["bredday.lang"]`) → `navigator.language` → English.
- Deep-link anchors (what the app links to): `#portugues`, `#espanol`, and
  `#top` (pins English explicitly).
  e.g. https://branicio.github.io/bredday-support/privacy.html#portugues
- Header tabs (EN / PT / ES) switch and remember the language; in-site links
  rewrite themselves so the language survives navigation.
- No JavaScript → all three languages render stacked (never a blank legal
  page). The tabs hide, since the full content is already on screen.

When editing content, keep the three `[data-lang]` sections structural clones
of each other — same elements, same order, only the copy changes. `site.js`
stamps `role="tabpanel"` / `aria-hidden` / ids at runtime; never hand-author
those (the hand-authored ids `top`, `portugues`, `espanol` are the exception).

## Contact

braniapps@gmail.com
