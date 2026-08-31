# Frontend Mastery — program material

Fourteen modules. Everything a module needs lives in one folder, so module 9 can be built
without opening module 2.

```
frontend-mastery-program/
  program/
    program-page.html       the public program page
    internal-plan.html      pricing, margins, sprint plan — internal only
  curriculum/
    curriculum-deck.html    the 24-slide curriculum proposal
    sources.md              the 12 reference courses, mapped module by module
    lms-structure.md        what the LMS expects per module and per lesson
    lesson-map.md           all 14 modules broken into 129 lessons (draft)
  modules/
    01-foundations/
      deck.html             28 slides, chipped per lesson
      script.html           the recording script — lesson map, figures, spoken text
    02-browser-runtime/
      deck.html
    …                       one folder per module, added as it is written
  repo/
    jobboard-deck.html      the exercise repo, explained
  assets/                   screenshots and recordings, shared by every deck
```

## Adding a module

Start from `curriculum/lesson-map.md` — it already names the module's lessons and which one
carries the exercise stage. `curriculum/lms-structure.md` is the content contract every
lesson has to satisfy before it can be uploaded.

1. `mkdir modules/<NN>-<slug>` — two-digit number so the folder list sorts into program
   order, then a slug that says what the module is about, not what number it is.
2. Write `script.html` first. The deck is built from it, not the other way round: the
   lesson map, the runtime budget and the figures all start there.
3. Write `deck.html`. Lift the figures out of the script rather than redrawing them —
   module 1's six figures moved across as inline SVG, recoloured by a five-line map.
4. Register the deck in `brand/apply_brand.py` with its chip, then run
   `python3 brand/apply_brand.py` from the repo root.

Two files per module is the rule. A module that needs a third — a workbook, a diagram
source — puts it in the same folder, never in a shared `misc/`.

## Assets

`assets/` is shared on purpose: the job board screenshots appear in the module 1 deck, the
module 2 deck and the repo deck, and there should be exactly one copy of each. Decks
reference them by relative path — `../../assets/…` from a module, `../assets/…` from
`repo/` — so a deck only works while it sits next to this folder.

Module-specific artwork that nothing else will ever use belongs in that module's folder.

## Chips

`apply_brand.py` gives every slide a `MODULE X · VIDEO Y` chip. The registry sets a deck's
default; a slide overrides it with `data-chip="MODULE 01 · VIDEO 4"`. Module 1's deck uses
the override on every slide, because it is the only module with a lesson map so far — the
chip tracks which of its nine lessons the slide belongs to.

## Preview

From the repo root:

```sh
portless catalyst-slides -- sh -c 'python3 -m http.server "$PORT"'
```

Then open `/frontend-mastery-program/modules/01-foundations/deck.html`.
