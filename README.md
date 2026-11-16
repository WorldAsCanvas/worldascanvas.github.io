# The World as a Canvas

Website for **The World as a Canvas: Materializing Imagination through Prompting the
Physical World**, a full-day workshop at UIST '26 — November 2, 2026, Detroit Marriott
at the Renaissance Center.

Live site: https://worldascanvas.github.io
Paper: https://doi.org/10.1145/3830397.3842699

## Structure

One page, no build step. Edit, commit, push; GitHub Pages redeploys in about a minute.

```
index.html                                the whole site, CSS and JS inline
the-world-as-a-canvas-uist26-workshop.pdf  linked from the Workshop Proposal button
favicon.ico
images/                                    see the README in that folder
images/organizers/                         portraits, wired by exact filename
images/photos/                             workshop photos shown in the Photos section
```

Sections in order: hero · Workshop Overview · Six Challenges · Organizers · Program ·
Photos · Contact.

The workshop took place on November 2, 2026. The page is now in its after-the-event
state: the registration block and the participant form links are gone, and Photos shows
a gallery from `images/photos/` plus four numbered links to Ruofei Du's 360° photos
(hosted on his viewer, not in this repository).

## Typefaces

Comico (wordmark, step labels, TBD markers) and Author (everything else), both from
Indian Type Foundry under the ITF Free Font License. They are loaded from Fontshare,
ITF's own CDN, and deliberately **not** committed here: the licence forbids making the
font files available through a public repository, while self-hosted serving and the
Fontshare API are each expressly permitted.

## Things that will break if changed carelessly

`index.html` carries comments at each of these; they are worth reading before editing.

- **Six Challenges card titles** are capped at 24px. The longest, *Cross-Media Creation,
  Transformation, and Provenance*, spills to a third line above that at the current card
  width. Break points inside the titles are pinned with non-breaking spaces.
- **The `CANVAS` block** is a background on a pseudo-element, never on the text, so the
  ragged crayon edge cannot eat into the letters.
- **Organizer hover** underlines the name rather than recolouring it. Yellow type on
  white measures 1.68:1 and disappears; yellow works as a fill, not as type.
- **`Workshop Proposal` label** on the peri button needs to stay at 19px/700. Blue on
  peri is 4.23:1, which only clears contrast at large-text sizes.
- **Organizer photos** are referenced by exact filename, including extension.

## Still to fill in

- Photos: the Google Photos album link ("More photos!")
- Research agenda and post-workshop report, once they are ready
