# Frontend Mastery — lesson map

**Draft for your edit.** Modules 2–14 are derived from the topic lists already written in
`curriculum-deck.html` and the source mapping in `sources.md`, rewritten into the lesson
shape the LMS expects (see `lms-structure.md`). Module 1 is not a draft — it is the real
map from `modules/01-foundations/script.html`.

Nothing here is uploaded until you have been through it. Two things depend on it, so it is
worth an editing pass early:

- **Branch names.** `module-3/v10-utils` needs the `v10`. The `Stage` column below supplies it.
- **Deck chips.** `MODULE 02 · VIDEO 7` on a slide needs the lesson number.

**129 lessons across 14 modules**, averaging 9 per module and ~4.3 hours of recorded video
per module — which lands the program at 60 hours, inside the 55–65 target.

Lesson titles are claims, not topics. If a title could be a folder name, it is not finished.

---

## Module 01 · Foundations — What Companies Actually Test
*Nine lessons · 72 min · free-preview candidate*

**Aim:** the student can name the five interview formats, place their own answers on the
junior/mid/senior ladder, and knows which module their score sends them to first.

| # | Lesson | Stage |
|---|---|---|
| 1 | Cold Open — Two Minutes Decide It | |
| 2 | The Hiring Map — Who Hires Frontend, and For What | |
| 3 | The Five Formats | |
| 4 | The Ladder — One Question, Three Levels | |
| 5 | Diagnostic, Part 1 — The Browser and the Language | |
| 6 | Diagnostic, Part 2 — Types, React, Architecture | |
| 7 | Your Score, and the Map of the Program | |
| 8 | How to Study This Program | clone the repo, one failing test |
| 9 | The Contract | |

---

## Module 02 · The Browser as a Runtime
*Ten lessons*

**Aim:** the student can explain what happens between an HTML tag and a lit pixel, and can
name which of their own CSS changes costs a layout. **This is the module that makes every
React module afterwards make sense.**

| # | Lesson | Stage |
|---|---|---|
| 1 | From HTML to pixels: the five stages of a frame | ✅ deck built |
| 2 | The DOM API is a shovel — querying without thrashing layout | |
| 3 | Semantic HTML is an API, and the accessibility tree is its output | |
| 4 | The box model decides your maths — content-box vs border-box | |
| 5 | Formatting contexts: why flex and grid are not magic | |
| 6 | Stacking and containing blocks — why `z-index: 9999` did nothing | |
| 7 | Reflow costs the CPU; compositing does not | |
| 8 | Composition layers: what the GPU holds, and what it costs in VRAM | |
| 9 | The event loop: tasks, microtasks, and the frame you just missed | |
| 10 | Instrument a slow page and prove the fix | `module-2/v10-browser-lab` |

---

## Module 03 · JavaScript, Deeply
*Ten lessons*

**Aim:** the student can implement the utilities an interviewer asks for from an empty file,
and can explain why each one is written the way it is — fluency under a shared editor, not
recall.

| # | Lesson | Stage |
|---|---|---|
| 1 | Execution contexts and the scope chain, drawn | |
| 2 | Closures are not a trick question — they are how callbacks remember | |
| 3 | `this` is decided at the call site, not the definition | |
| 4 | Prototypes, and what `class` is hiding | |
| 5 | Modules, bundling, and what `import` actually does at runtime | |
| 6 | Callbacks → promises → async/await, and the states in between | |
| 7 | Error handling across async boundaries | |
| 8 | Memory, references and the leak your SPA has right now | |
| 9 | Building the interview toolbelt, part 1: debounce and throttle | |
| 10 | Building the interview toolbelt, part 2: deepClone, EventEmitter, promiseAll | `module-3/v10-utils` |

> **Naming note:** the exercise stage currently on the remote is `module-3/utils`. Renaming
> it to `module-3/v10-utils` and tagging `m3-v10-end` is one command per branch once you
> confirm lesson 10 is where the library lands.

---

## Module 04 · TypeScript for Frontend Engineers
*Nine lessons*

**Aim:** the student models a domain with types that make the wrong state unrepresentable,
and knows the point where more types stop paying for themselves.

| # | Lesson | Stage |
|---|---|---|
| 1 | Structural typing: TypeScript does not care what you named it | |
| 2 | Generics are parameters for types, nothing more | |
| 3 | Narrowing, and the difference between `unknown` and `any` | |
| 4 | Discriminated unions kill the five-boolean component | |
| 5 | Utility and mapped types you will actually reach for | |
| 6 | Typing async data, and where the lies get in | |
| 7 | Schema validation at the boundary, types on the inside | |
| 8 | `tsconfig` strictness, flag by flag, and what each one catches | |
| 9 | Model the job board's domain end to end | `module-4/v9-domain-types` |

---

## Module 05 · React, Deeply
*Eleven lessons*

**Aim:** the student can explain a re-render they did not expect, and fix it without
reaching for `memo` first. **The render model is the spine of this module — and it is
written from scratch, not sourced.**

| # | Lesson | Stage |
|---|---|---|
| 1 | The render model: what React does between your state and the DOM | |
| 2 | Fiber, lanes, and why rendering can be interrupted | |
| 3 | Anatomy of a re-render — the four reasons a component runs again | |
| 4 | Keys, reconciliation, and state landing on the wrong row | |
| 5 | Hooks: state, effects, refs, and the closure trap | |
| 6 | You might not need an effect — deriving instead of synchronising | |
| 7 | Context, and why it re-rendered everything | |
| 8 | Composition patterns that beat prop drilling | |
| 9 | Error boundaries and portals | |
| 10 | Suspense and concurrent rendering, plainly | |
| 11 | Build the listings feed, then profile it | `module-5/v11-feed-ui` |

---

## Module 06 · React + TypeScript in Production
*Eight lessons*

**Aim:** the student writes components a reviewer can read — typed props, typed events, and
state machines instead of boolean soup.

| # | Lesson | Stage |
|---|---|---|
| 1 | Typing props, children and refs without fighting the compiler | |
| 2 | Typing events, forms and the handlers between them | |
| 3 | Generic components: one `Select`, every option type | |
| 4 | Polymorphic components and the `as` prop | |
| 5 | Typed hooks and typed reducers | |
| 6 | Discriminated state machines instead of five booleans | |
| 7 | A typed API layer the UI can trust | |
| 8 | Build the typed primitives the whole app will use | `module-6/v8-typed-components` |

---

## Module 07 · UI Engineering — Components & Accessibility
*Eleven lessons*

**Aim:** the student builds the components an interviewer asks for live — keyboard-driven,
ARIA-correct, no library. **This is the highest-ROI module for the live-coding round.**

| # | Lesson | Stage |
|---|---|---|
| 1 | Component API design: data, event, config, style and slot props | |
| 2 | Controlled, uncontrolled, and the one you actually want | |
| 3 | Design tokens and a design system small enough to finish | |
| 4 | The accessibility tree, focus, and the keyboard path | |
| 5 | Build the search autocomplete — debounce and race conditions | `module-7/v5-autocomplete` |
| 6 | The ARIA combobox contract, attribute by attribute | |
| 7 | Build the overlays — modal, dropdown, tabs, toast | `module-7/v7-overlays` |
| 8 | Focus traps, portals and live regions | |
| 9 | Forms and validation without a form library | |
| 10 | Virtualization from scratch: windowing, pooling, recycling | `module-7/v10-virtual-list` |
| 11 | Responsive behaviour that is not just breakpoints | |

---

## Module 08 · Data, State & Routing
*Ten lessons*

**Aim:** the student can say which state is the server's and which is theirs — the
distinction that decides mid versus senior — and can defend where each piece lives.

| # | Lesson | Stage |
|---|---|---|
| 1 | Server state vs client state: the question most candidates fail | |
| 2 | TanStack Query: the cache, and what invalidation really means | |
| 3 | Optimistic updates, and the rollback everybody forgets | |
| 4 | Race conditions in data fetching, and the two fixes | |
| 5 | Type-safe routing and loaders | |
| 6 | Search params are state — make the URL shareable | |
| 7 | Normalization, and when a flat store earns its keep | |
| 8 | Zustand, Redux Toolkit, and when each is the wrong choice | |
| 9 | Real-time: polling, SSE and websockets compared | |
| 10 | Rebuild the data layer on Query and Router | `module-8/v10-data-layer` |

---

## Module 09 · Next.js & Rendering Architecture
*Ten lessons*

**Aim:** the student picks a rendering strategy per route and defends it out loud, including
the routes where Next.js is the wrong answer.

| # | Lesson | Stage |
|---|---|---|
| 1 | The App Router mental model | |
| 2 | Server Components vs Client Components — where the boundary goes | |
| 3 | CSR, SSR, SSG, ISR and streaming, chosen per route | |
| 4 | Data fetching and the caching layers, in order | |
| 5 | Server actions and mutations | |
| 6 | Route handlers, middleware and the edge | |
| 7 | Auth and session patterns that survive a refresh | |
| 8 | SEO, metadata, and the dashboard that must not be indexed | |
| 9 | When NOT to reach for Next.js | |
| 10 | Port the job board: public pages vs authed dashboard | `module-9/v10-next-rendering` |

---

## Module 10 · Performance, Testing & Security
*Eleven lessons*

**Aim:** the student sets a performance budget, proves a before and after with numbers, and
ships it with tests in CI. **The measurement toolchain here is original material — no source
course covers it.**

| # | Lesson | Stage |
|---|---|---|
| 1 | Core Web Vitals: LCP, INP, CLS, and which one users feel | |
| 2 | Measuring properly: the Performance panel, lab vs field | |
| 3 | Lighthouse, CrUX, RUM — what each one can and cannot tell you | |
| 4 | Bundles: analysis, code splitting, and the import that cost 300 KB | |
| 5 | Images, fonts and the layout shift they cause | |
| 6 | Memoization that actually helps, and the profiler that proves it | |
| 7 | The testing pyramid: what to unit test, what to E2E | |
| 8 | Testing behaviour with Testing Library, not implementation | |
| 9 | Playwright and MSW: the tests that catch real regressions | |
| 10 | XSS, CSRF, CSP and where to put a token | |
| 11 | Baseline → budget → fix, with CI green | `module-10/v11-perf-and-tests` |

---

## Module 11 · Frontend System Design
*Nine lessons*

**Aim:** the student runs a 45-minute design round with a script — RADIO — and can defend
the trade-offs of a codebase that has to scale past one team. **This is the differentiator;
record it early.**

| # | Lesson | Stage |
|---|---|---|
| 1 | What a design round is actually scoring | |
| 2 | RADIO: Requirements, Architecture, Data, Interface, Optimizations | |
| 3 | Requirements: the questions that buy you the next twenty minutes | |
| 4 | Component and data-flow architecture on a whiteboard | |
| 5 | API and contract design from the client's side | |
| 6 | Scaling the codebase 1 — the modular monolith | *arch repo* |
| 7 | Scaling the codebase 2 — monorepos and what they actually fix | *arch repo* |
| 8 | Scaling the codebase 3 — micro-frontends and their real cost | *arch repo* |
| 9 | Six questions, walked: feed, autocomplete, chat, e-commerce, dashboard, editor | |

> Lessons 6–8 are the existing 49-slide architecture deck, split into three videos. Their
> end states are the branches in `frontend-architecture-monolith`, `-monorepo` and
> `-micro-frontends` — tag them `m11-v6-end`, `m11-v7-end`, `m11-v8-end` with
> `architecture-course/tag-videos.sh`.

---

## Module 12 · The Capstone
*Six lessons*

**Aim:** the student ships one deployed job board they can defend line by line — and
discovers that most of it already exists on branches they wrote themselves.

| # | Lesson | Stage |
|---|---|---|
| 1 | Assembly week, not build week — what you already have | |
| 2 | Wiring auth and protected routes end to end | |
| 3 | The architecture story: writing down why, not what | |
| 4 | Deploy, and the CI gate that keeps it green | |
| 5 | The accessibility and performance pass you can defend | |
| 6 | Capstone review against the senior checklist | `module-12/v6-capstone` |

---

## Module 13 · Interview Preparation
*Eight lessons*

**Aim:** the student has drilled every format under time, and can think out loud without
going quiet.

| # | Lesson |
|---|---|
| 1 | Thinking out loud: the skill nobody practises |
| 2 | The quiz round: 200 "why" questions, and how to answer in thirty seconds |
| 3 | The utilities round under time pressure |
| 4 | The UI round: clarify, scaffold, build, then polish |
| 5 | The design round, timed, with the RADIO script |
| 6 | Behavioural answers with STAR and a real trade-off |
| 7 | Take-home strategy: scope, README, and knowing when to stop |
| 8 | Building your own drill schedule from your module 1 score |

---

## Module 14 · Mock Interviews & Getting the Offer
*Seven lessons*

**Aim:** the student sits a recorded mock, reads their scorecard on six axes, and negotiates
with real numbers.

| # | Lesson |
|---|---|
| 1 | The mock format and the six scoring axes |
| 2 | Recorded mock 1: live coding, with feedback |
| 3 | Recorded mock 2: system design, with feedback |
| 4 | Reading your scorecard, and the retest plan |
| 5 | The CV and LinkedIn a frontend recruiter actually reads |
| 6 | Portfolio review: what to show and what to cut |
| 7 | Salary bands and negotiation: Egypt → Gulf → remote |

---

## What to do with this

1. **Edit the titles.** They are claims; make them yours. Retitle freely — the numbers are
   what the rest of the system depends on, not the words.
2. **Confirm the stage lessons** (the `Stage` column). Those numbers become branch names
   and end tags.
3. **Then, per lesson, write the four LMS blocks** — summary, what you will learn, core idea,
   key takeaways. The template and a worked example are in `lms-structure.md`.

Blocks are the bulk of the writing: 129 lessons × 4 blocks. Worth doing a module at a time,
in the sprint that records it, not all at once up front.
