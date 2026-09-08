# Frontend Mastery — program material

Thirteen modules. Everything a module needs lives in one folder, so module 9 can be built
without opening module 2.

```
frontend-mastery-program/          tracked — everything here is safe to hand out
  program/
    program-page.html       the public program page
  curriculum/
    curriculum-page.html    the student-facing curriculum — all 123 lessons, no sourcing
  modules/
    01-foundations/
      deck.html             28 slides, chipped per lesson
      diagnostic-deck.html  50 slides — the twelve questions, answered and animated
    02-browser-runtime/
      deck.html
    …                       one folder per module, added as it is written
  repo/
    jobboard-deck.html      the exercise repo, explained
  assets/                   screenshots and recordings, shared by every deck

_internal/                         gitignored — never leaves this machine
  MAP.html                  the workspace index
  program/internal-plan.html      pricing, margins, sprint plan
  curriculum/
    curriculum-deck.html    the 24-slide curriculum proposal
    sources.md              the reference courses, mapped module by module
    lms-structure.md        what the LMS expects per module and per lesson
    lesson-map.md           all 13 modules broken into 123 lessons (draft)
  modules/01-foundations/
    script.html             the recording script — lesson map, figures, spoken text
    deck-ar.html            how to explain module 1, slide by slide, in Egyptian Arabic
```

Paths below are written from whichever tree the file lives in. A deck in
`frontend-mastery-program/` never links into `_internal/`; the internal files link out
across the boundary, not the other way round.

## Sourcing stays internal

Nothing a student can open ever names or links where the material came from — no source
course, no platform, no author, no URL to one. That means `modules/*/deck.html`,
`program/program-page.html`, `curriculum/curriculum-page.html`, `repo/jobboard-deck.html`,
every workbook, and every LMS lesson block.

- **Internal only:** everything under `_internal/`, which is gitignored. The source map
  lives there and nowhere else.
- **Student-facing references,** when a lesson needs one, point at primary material only —
  MDN, web.dev, the spec, framework docs, our own repo. Never at a course.
- Before shipping a module, run the check below; it must print nothing.

```sh
grep -rniE "master\.dev|frontend ?masters|greatfrontend|bigfrontend|epic ?react|frontendexpert|https?://" \
  modules/*/deck.html program/program-page.html \
  curriculum/curriculum-page.html repo/*.html
```

## Adding a module

Start from `_internal/curriculum/lesson-map.md` — it already names the module's lessons and
which one carries the exercise stage. `_internal/curriculum/lms-structure.md` is the content
contract every lesson has to satisfy before it can be uploaded.

1. `mkdir modules/<NN>-<slug>` — two-digit number so the folder list sorts into program
   order, then a slug that says what the module is about, not what number it is.
2. Write `_internal/modules/<NN>-<slug>/script.html` first. The deck is built from it, not
   the other way round: the lesson map, the runtime budget and the figures all start there.
   Scripts are internal — they carry sourcing, timings and the words said off camera.
3. Write `deck.html`. Lift the figures out of the script rather than redrawing them —
   module 1's six figures moved across as inline SVG, recoloured by a five-line map.
4. Register the deck with its chip in the brand generator and run it from the repo root.
   The generator lives in `brand/`, which is local tooling and is not committed — decks are
   committed already branded.

Two files per module is the rule. A module that needs a third — a workbook, a diagram
source — puts it in the same folder, never in a shared `misc/`.

## Assets

`assets/` is shared on purpose: the job board screenshots appear in the module 1 deck, the
module 2 deck and the repo deck, and there should be exactly one copy of each. Decks
reference them by relative path — `../../assets/…` from a module, `../assets/…` from
`repo/` — so a deck only works while it sits next to this folder.

Module-specific artwork that nothing else will ever use belongs in that module's folder.

## Chips

The brand generator gives every slide a `MODULE X · VIDEO Y` chip. Its registry sets a
deck's default; a slide overrides it with `data-chip="MODULE 01 · VIDEO 4"`. Module 1's deck uses
the override on every slide, because it is the only module with a confirmed lesson map — the
chip tracks which of its seven lessons the slide belongs to.

## Preview

From the repo root:

```sh
portless catalyst-slides -- sh -c 'python3 -m http.server "$PORT"'
```

Then open `/frontend-mastery-program/modules/01-foundations/deck.html`.
