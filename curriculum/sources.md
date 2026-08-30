# Frontend Mastery — Source Material Map

Reference TOCs from master.dev (Frontend Masters) for the 14 modules in `curriculum.html`.
Total source runtime: **~57.5 hours** across 12 courses → target program: ~55–65 recorded hours in Arabic.

> **Dropped from the plan:** *React Performance, v2* and *Web Performance Fundamentals, v2*. What they covered
> is re-sourced below or moved to the original-material list in section 4 — see the M5 and M10 rows.

Rule of thumb: 1 hour of English source ≈ 45–55 min of our recorded Arabic material, because we cut
their project scaffolding and add interview framing.

---

## 0 · Course links

| Course | URL |
|---|---|
| Advanced Web Development Quiz | https://master.dev/courses/web-dev-quiz/ |
| Front-End System Design | https://master.dev/courses/frontend-system-design/ |
| A Tour of JavaScript & React Patterns | https://master.dev/courses/tour-js-patterns/ |
| TypeScript in the Age of AI | https://master.dev/courses/typescript-ai/ |
| Complete Intro to React, v9 | https://master.dev/courses/complete-react-v9/ |
| Intermediate React, v6 | https://master.dev/courses/intermediate-react-v6/ |
| React and TypeScript, v3 | https://master.dev/courses/react-typescript-v3/ |
| State Management at Scale | https://master.dev/courses/react-nextjs-state/ |
| TanStack Start & TanStack Query | https://master.dev/courses/tanstack/ |
| Next.js Fundamentals, v4 | https://master.dev/courses/next-js-v4/ |
| Intermediate Next.js | https://master.dev/courses/intermediate-next-js/ |
| Testing Fundamentals | https://master.dev/courses/testing/ |

---

## 1 · Module → source mapping

| Our module | Primary source(s) | Sections to lift | Source time |
|---|---|---|---|
| **M1** Foundations — what companies test | `web-dev-quiz` | full quiz as a diagnostic | 2h21m |
| **M2** The Browser as a Runtime | `frontend-system-design` (Core Fundamentals, DOM API), `web-dev-quiz` | box model → reflow → composition layers → rendering; DOM querying & perf | ~1h10m |
| **M3** JavaScript, Deeply | `tour-js-patterns` (JavaScript Patterns), `web-dev-quiz` | module/singleton/proxy/observer/factory/prototype; event loop, GC, generators, promises | ~2h20m |
| **M4** TypeScript for Frontend | `typescript-ai` | everything except the AI-generation lessons | 4h23m |
| **M5** React, Deeply | `complete-react-v9`, `intermediate-react-v6` | hooks → ecosystem → advanced → render modes → RSC; *the render model (Fiber, lanes, re-render anatomy) is now original material* | ~7h30m |
| **M6** React + TypeScript | `react-typescript-v3` | full course | 4h20m |
| **M7** UI Engineering & a11y | `frontend-system-design` (Web APIs, Virtualization), `tour-js-patterns` (React Patterns) | Observer APIs, virtualization from scratch, compound/provider/render-props | ~3h15m |
| **M8** Data, State & Routing | `tanstack`, `react-nextjs-state` | TanStack Query/Router/Start; anti-patterns, normalization, URL state, XState | ~9h |
| **M9** Next.js & rendering | `next-js-v4`, `intermediate-next-js`, `intermediate-react-v6` (RSCs with Next.js) | full both + RSC block | ~11h30m |
| **M10** Performance, Testing & Security | `testing`, `frontend-system-design` (Web Application Performance), `tour-js-patterns` (Performance + Rendering Patterns), `web-dev-quiz` (perf/CSP/CORS Qs) | Vitest → Testing Library → Playwright; bundling & loading, CSS/images/fonts; browser hints; Core Web Vitals overview. *Measurement toolchain and React tuning are original material* | ~5h40m |
| **M11** Frontend System Design | `frontend-system-design` (App State, Network, Perf, News Feed) | the whole back half + the interview walkthrough | ~2h25m |
| **M12** Capstone | `next-js-v4` + `tanstack` project arcs | project structure, deploy, test | reuse |
| **M13** Interview Preparation | `web-dev-quiz`, GreatFrontEnd GFE 75 | quiz drilling + JS utility implementations | — |
| **M14** Mock Interviews & Offer | `frontend-system-design` (News Feed walkthrough) as the model | how a design round is narrated | — |

---

## 2 · Full tables of contents

### TanStack Start & TanStack Query — ~4h19m → M8
- **Introduction** (15m)
- **Setup** (37m): Drizzle Overview · Routing Basics · Loaders · Routing Errors & 404 Handling
- **Server Functions** (1h): Loading Data · Route Caching · Layout Rendering & Refetching · Streaming · Streaming with Suspense
- **TanStack Query** (39m): TanStack Query · Suspense & TanStack Query · Blocking Suspense Rendering · Opt-In String Query Params
- **Middleware** (50m): Middleware · Sending Middleware Context · Server-Side Middleware Function · Real World Middleware · Advanced Middleware
- **Advanced Routing** (28m): Server Functions · Selective Hydration · Static Pre-rendering
- **RSCs** (25m): React Server Components · Fetching Data in RSCs · Client Components in RSCs

> Note: this course is TanStack **Start**-centric. For our M8 we teach TanStack **Router** standalone (type-safe routes, loaders, search-param state) plus Query — skip the Drizzle/Start-server half unless we add a Start bonus lesson.

### Front-End System Design — ~4h33m → M2, M7, M10, M11
- **Introduction** (5m)
- **Core Fundamentals** (38m): Box Model · Browser Formatting Context · Browser Positioning · Reflow · Composition Layers · Browser Rendering
- **DOM API** (28m): DOM & Querying · DOM Performance Best Practices · DOM Templating Exercise
- **Web APIs for Complex UI Patterns** (36m): Observer API · Infinite Scroll with IntersectionObserver · MutationObserver (+ exercise) · ResizeObserver (+ exercise)
- **Virtualization** (58m): Virtualization Technique · Coding Virtualization from Scratch · Loading New Data · Creating a Virtualization Pool · Recycling Elements · Q&A · Handle Top Virtualization
- **Application State & Network Connectivity** (42m): Application State Design · Network Connectivity · Server-Sent Events · Web Sockets · Classic REST & GraphQL
- **Web Application Performance** (26m): Performance Optimization · JavaScript Bundling & Loading · CSS, Images & Rendering — **now the primary web-perf source for M10**
- **System Design Interview: Social Media News Feed** (38m): Requirements & Mock-Up · Application State & API · Optimizing Performance

> This is the closest thing to our M11. Their interview walkthrough is only 38 minutes and covers one question — our module goes wider (RADIO + 6 canonical questions), so this is a template, not a substitute.

### TypeScript in the Age of AI — ~4h23m → M4
- **Introduction** (4m)
- **TypeScript Basics** (48m): Nominal vs Structural Typing · TypeScript Basics · `typeof` Operator · Type-Safe Forms · Exporting Types for Public APIs · Return Types
- **Generics** (48m): Generics · Generics in React Components · Grabbing Arguments · Custom Proxying Layer · Zustand with Generics · Generics Exercise · Generate Generics with AI
- **Unions** (53m): Unions · Type Narrowing · Type Guards · Narrowing to Never · Excess Property Checks
- **Conditional Types** (51m): Conditional Types & Inferring · Generating Conditional Types with AI · Exercise · Unions with Conditional Types · Validating Types Match · Tuple Types · Finding the Longer Subset
- **Advanced Techniques** (54m): Function Overloading · Template Literal Types · Variance · Mapped Types Overview · Using Mapped Types · Mapped Types Exercise · Constraining Keys Exercise

> Drop the two "with AI" lessons — that content belongs to the *AI for Frontend* SKU.

### Complete Intro to React, v9 — Brian Holt · 8h27m · 50 lessons → M5
- Introduction (11m) · Basic React App (21m) · Tooling (43m) · JSX in React (34m) · **React Hooks (2h04m)** · **The React Ecosystem (1h)** · **Advanced React Techniques (1h17m)** · Testing (1h31m) · **React 19 Features (35m)** · Wrapping Up (6m)
- Stack: Vite, ESLint, Prettier, TanStack Router, TanStack Query, Vitest.

### Intermediate React, v6 — Brian Holt · 6h22m · 37 lessons → M5, M9
- Introduction (17m) · **React Render Modes (1h04m)** · **React Server Components (1h30m)** · **RSCs with Next.js (1h23m)** · Performance Optimizations (36m) · Transitions (29m) · Optimistic Values (23m) · Deferred Values (34m)

### Next.js Fundamentals, v4 — ~6h37m → M9
- **Introduction** (6m)
- **Setup** (1h19m): Course Project Setup · Create a Next.js App from Scratch · Project Structure & Config · Static vs Dynamic Routes and Layouts · Pages and Routing Exercise · Styling Marketing & Auth Pages · Static Pages
- **Server Actions** (1h01m): Server Actions · Auth Server Actions · Auth Forms with Server Actions · Creating the Signup Form · Testing Auth Server Actions
- **Authentication & Data Handling** (41m): Data Access Layer · Authenticating Users · Caching with `dynamicIO` & Suspense · Dashboard UI & Layout
- **CRUD with Server Actions** (56m): Creating Issues · Data Loading & Caching Q&A · Editing Issues · Updating with `useTransition` · Q&A
- **Caching & API Routes** (1h07m): Caching · Memoizing · API Routes · Creating API Routes
- **Middleware & Edge Functions** (26m): What is Next.js Middleware? · Authenticating APIs with Middleware · Edge Functions & Runtime
- **Deployment & Testing** (57m): Deploying to Vercel · Updating a Vercel App · Testing with Vitest · Testing the Dashboard Page

### Intermediate Next.js: Server Actions, Route Slots & State — ~3h28m → M9
- **Introduction** (11m): Project & Database Setup
- **Form Authentication Actions** (42m): React Standards in Next.js · Server & Form Actions Overview · Auth Actions · Submit Button · Sign-In Form
- **Routing & Data Fetching** (1h24m): Route Slots · Dashboard Routes · Default Routes · Server-Side Data Fetching · Displaying Attendee Count · Fetching Events & RSVPs · Per-Request Caching · Cache Persistence & Revalidation Tags · Suspense & Errors
- **Active & Protected Routes** (22m): Active Routes · Route Protection · Protecting Routes with Middleware
- **Advanced Server Actions & Revalidation** (41m): Non-Form Server Actions · `useTransition` & Non-Blocking Updates · Q&A · Cache & Revalidation Strategies · Events Page

### React and TypeScript, v3 — ~4h20m → M6
- **Introduction** (12m)
- **useState Type Safety** (54m): Types · Types vs Interfaces · Typing Children Exercise · Typing useState (+ exercise)
- **Event & Form Types** (35m): Typing Events · Typing Form Events Exercise · Button Props · Creating a Button Component Exercise
- **State Management** (47m): Unions & Template Literal Types · Typing Reducer Actions · Discriminated Unions · Refactoring Reducer with Action Type
- **Async Data and Suspense** (37m): Typing Async Data · Schema Validation with Zod · Optional/Nullable/Coercion · Advanced Zod Types · `use()` Hook & Suspense Types
- **Context API & Generics** (1h14m): Context & Selector Types · Generics · Generics with React Components · Helpful Type Utilities · Component Variants · Q&A

> This is the single best-fitting course in the list — M6 can follow it almost 1:1.

### State Management at Scale in React & Next.js — ~4h45m → M8
- **Introduction** (10m)
- **Anti-Patterns** (20m): Deriving State · useState & Redundant State · Exercise
- **State Modeling** (28m): Incidental vs Accidental Complexity · Essential Modeling Diagrams · Application Flow Exercise
- **Optimizing State Management** (40m): Best Practices · Finite States · Combining State Exercise · Type State Implementation
- **FormData & Complex State** (1h13m): `useActionState` · Converting useState to FormData · `useReducer` · State Flow with `use()`, Stores & Effects · Context and State Machine Exercise · Step-Based Approach
- **External Libraries** (29m): Store vs Atomic Libraries · XState Store · Exercise
- **Data Normalization** (33m): Flattening Nested Structures · Exercise · Undo & Redo Events
- **Event-Driven vs Reactive** (12m): Avoiding Cascading Effects · Refactor Exercise
- **Advanced Techniques** (38m): URL Parameters as State · Server State with TanStack Query (+ exercise) · Syncing with External Stores · `useSyncExternalStore` Exercise · Testing Reducers vs Components

### Testing Fundamentals — ~4h26m → M10
- **Introduction** (15m) · Course Overview
- **Testing Basics** (53m): Anatomy of a Test · First Test · Simple Tests Exercise · Testing Guidelines · Invalid Input · Edge Cases Exercise
- **Testing Equality** (39m): Referential Equality · Testing Randomness · Asymmetric Matchers Exercise · Before/After Hooks & Async Code
- **Testing the DOM** (1h01m): DOM Testing Tools · Testing Buttons · Testing Library Utilities · Accident Counter project (+ exercise + solution) · Searching DOM
- **Stubs, Spies, Mocks** (1h09m): Test Doubles · Spies · Mocks · Alert Spy Exercise · Mocking Dependencies · Mocking Time
- **End-To-End Testing** (26m): Playwright · Testing the Counter with Playwright · Mock Service Worker

### A Tour of JavaScript & React Patterns — ~3h27m → M3, M7, M10
- **JavaScript Patterns** (1h21m): Module · Singleton · Proxy · Observer (+ Q&A) · Factory · Prototype — each with a solution lesson
- **React Patterns** (1h06m): Container/Presentation · Higher-Order Component · Render Props · Hooks · Provider · Compound — each with a solution lesson
- **Performance Patterns** (30m): Bundling & Compiling · Static & Dynamic Imports · Browser Hints: Prefetch & Preload — **→ M10**
- **Rendering Patterns** (18m): Core Web Vitals · Client-Side & Static Rendering · Incremental Rerendering & SSR — **→ M10**, the only Core Web Vitals overview left in the set

### Advanced Web Development Quiz — 2h21m · 30 questions → M1 diagnostic + M13 drill bank
`async`/`defer` order · rendering pipeline & compositing · DNS resolution · call stack & event loop · resource hints · object reference & destructuring · `PerformanceNavigationTiming` · cache directives · garbage collection · animation cost · event propagation · CSS specificity · `WeakMap` · Web Vitals · CSP header · referrer policies · generators · promise methods · bfcache · front-end security · font strategies · cookie policy header · CSS pseudo selectors · transport security · render layers · image formats · CORS headers · event loop · HTTP 1/2/3 · invoking object methods & scope

> **Use this twice**: as the M1 "here's what you don't know yet" diagnostic, and as the M13 quiz-round bank. It maps almost one-to-one onto the questions a mid/senior "why" round asks.

---

## 3 · Suggested prep order (before recording)

| # | Course | Hours | Records into |
|---|---|---|---|
| 1 | Advanced Web Development Quiz | 2.4 | M1, M13 — do this first, it sets the bar |
| 2 | Front-End System Design | 4.6 | M2, M7, M11 |
| 3 | A Tour of JS & React Patterns | 3.5 | M3, M7 |
| 4 | TypeScript in the Age of AI | 4.4 | M4 |
| 5 | Complete Intro to React, v9 | 8.5 | M5 |
| 6 | Intermediate React, v6 | 6.4 | M5, M9 |
| 7 | React and TypeScript, v3 | 4.3 | M6 |
| 8 | State Management at Scale | 4.8 | M8 |
| 9 | TanStack Start & Query | 4.3 | M8 |
| 10 | Next.js Fundamentals, v4 | 6.6 | M9 |
| 11 | Intermediate Next.js | 3.5 | M9 |
| 12 | Testing Fundamentals | 4.4 | M10 |

**Total: ~57.5 h.** Two courses that used to sit at #7 and #13 are gone; the hours they freed move
to authoring, because M5's render model and M10's measurement toolchain are now written from scratch.

Two passes per course: watch at 1.5×, then re-watch only the sections in the mapping table while
writing the Arabic lesson outline.

---

## 4 · Coverage gaps — none of these 14 cover it

These modules have **no source course** in the list. Plan original material:

1. **HTML semantics & the accessibility tree** (M2, M7) — nothing here teaches ARIA, focus management, or keyboard interaction. Source: MDN + WAI-ARIA Authoring Practices patterns.
2. **CSS at depth** (M2) — only the box model / formatting contexts from Front-End System Design. Flexbox, Grid, cascade layers, container queries need original lessons.
3. **JS language internals** (M3) — the patterns course teaches *patterns*, not closures/`this`/prototypes/memory. Frontend Masters' "JavaScript: The Hard Parts" is the missing piece if you want a source.
4. **The interview utility library** (M3) — debounce, throttle, deepClone, curry, EventEmitter, `Promise.all`. Source: GreatFrontEnd GFE 75 JS-functions list; write our own solutions.
5. **The component gauntlet** (M7) — modal, dropdown, tabs, autocomplete, toast built from scratch. Only virtualization is covered above. Source: GFE user-interface question list + WAI-ARIA patterns.
6. **React's render model** (M5) — Fiber, lanes, the anatomy of a re-render, and the tuning that follows from it (`useMemo`, `useCallback`, `React.memo`, transitions, deferred values, the compiler). *Intermediate React v6* still covers render modes, performance optimizations, transitions, optimistic and deferred values, so the tuning half has a source — the internals half does not. Source for that: the React docs' "React Compiler" and "You Might Not Need an Effect" pages, `react-reconciler` source reading, and Dan Abramov's writing.
7. **Web-performance measurement** (M10) — Core Web Vitals in depth (LCP, CLS, INP, TTFB, FCP), the Performance API and PerformanceObserver, Lighthouse, the Performance panel, CrUX, WebPageTest, RUM, and the improvement playbooks for each metric. `tour-js-patterns` gives a 18-minute overview and the quiz gives ~6 questions; everything past that is ours. Source: web.dev/vitals, the Chrome DevTools docs, and a measured before/after on our own job board.
8. **Security** (M10) — the quiz has ~4 questions on CSP/CORS/transport; nothing systematic on XSS, CSRF, token storage. Needs original material.
9. **RADIO + system design at senior level** (M11) — Front-End System Design gives one 38-minute walkthrough. The framework, evaluation axes, and 6-question drill set are ours to build.
10. **Behavioral, CV, negotiation, mock interviews** (M13–M14) — zero coverage. This is exactly where Backend Mastery differentiates, and it has to be built from scratch.

---

## 5 · References for M12, M13, M14

No master.dev course covers these three. Use instead:

**M12 — Capstone** (borrow project arcs, not curriculum)
- Next.js Fundamentals v4 — best full arc: setup → server actions → auth → CRUD → caching → deploy & test
- Intermediate Next.js — route slots, revalidation tags, protected routes
- Testing Fundamentals — Playwright + MSW so the capstone ships with E2E in CI
- TanStack Start & Query — loader/query patterns for the data layer
- https://nextjs.org/docs/app — caching/rendering semantics move faster than any course
- https://web.dev/articles/vitals — where the performance budget comes from
- https://github.com/eng-AhmedMahmoud/commerceos-frontend-architecture — my own boundaries + staged versions

**M13 — Interview preparation** (question banks & drills)
- https://www.frontendinterviewhandbook.com/ — free; clearest map of formats and answer structures
- https://www.greatfrontend.com/interviews/gfe75 — the 75-question core list
- https://www.greatfrontend.com/questions/formats/ui-coding — 59 build-a-component questions
- https://www.greatfrontend.com/questions/formats/quiz — 283 "why" questions
- https://bigfrontend.dev/ — JS utility implementations with real test cases
- master.dev Advanced Web Development Quiz — the 30-question set, reused from M1
- https://www.greatfrontend.com/interviews/blind75 — only if we cover DSA at all
- https://roadmap.sh/questions/frontend — free sanity list

**M14 — Mocks & offer** (format, rubric, salary data)
- https://www.greatfrontend.com/behavioral-interview-playbook — question categories & frameworks
- https://www.greatfrontend.com/front-end-interview-playbook/resume — CV lesson structure
- https://interviewing.io/ — recorded real interviews; best reference for pacing and narration
- https://www.tryexponent.com/ — mock structure and scoring rubrics
- https://www.levels.fyi/ — salary bands; pair with local Egypt/Gulf data
- https://www.greatfrontend.com/system-design/evaluation-axes — the six axes become our mock scorecard
- Internal: Backend Mastery M11–13 — Abdullah's mock format and offer module

All of it is reference for me. Every question, rubric and mock we ship gets written fresh in Arabic —
those banks are licensed products, and the point of M13–M14 is that ours are ours.

---

**Read:** roughly 60% of the technical spine has a strong English source to learn from; the
interview layer — the part that makes it *Mastery* and not a tutorial series — is 100% original,
which is also why it can't be copied by a competitor.
