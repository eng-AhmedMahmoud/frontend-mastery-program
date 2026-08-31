# What the LMS expects — read from *AI for Frontend*

Observed from the live course at
`learning.catalystai.llc/learn/courses/ai-for-frontend`, which is the shape Frontend
Mastery has to match. This file records the contract; `lesson-map.md` is Frontend Mastery
filled into it.

## The two units

**Course → Module → Lesson.** Nothing else. There is no "act", no "chapter", no "part".
The three acts in our curriculum deck are a *narrative* device for the sales page — the
platform only knows modules.

| | AI for Frontend | Frontend Mastery, target |
|---|---|---|
| Modules | 10 | 14 |
| Lessons | 56 | 129 (drafted) |
| Lessons per module | 4 – 7 | 6 – 12 |
| Runtime | short-form | 55 – 65 h |

Our modules are heavier because the program is three times longer. What must not change is
the *granularity*: a lesson is one idea, watchable in one sitting, and it is the unit a
student marks complete. Module 1's recording script already works this way — nine lessons,
72 minutes, none over 12 minutes. That is the house rhythm; apply it everywhere.

## A module needs

1. **Title** — a phrase, not a topic list. *"Spec-Driven UI Development"*, not *"Specs"*.
2. **Blurb** — two or three sentences of what the student walks out able to do, ending in an
   explicit aim. The live course does this consistently:
   > *"A practical map of when to use Lovable, Claude/ChatGPT, Cursor… **Aim: tool judgment,
   > not tool addiction.**"*
   The aim sentence is the part that sells the module. Ours currently have topic lists where
   this should be.
3. **Ordered lessons.**

## A lesson page carries

In this order, and every lesson has all of it:

| Block | Shape | Notes |
|---|---|---|
| Breadcrumb | Course › Module › Lesson | automatic |
| Title | a claim or an action | *"Two AI skills: building with AI vs building AI in"* |
| Video | embedded player | keyboard hint sits under it |
| **Lesson summary** | **one sentence** | what this lesson is, in the student's language |
| **What you will learn** | **4 bullets** | concrete, checkable, no "understand X" |
| **Core idea** | **one short paragraph** | the single thing to remember; this is the quotable line |
| **Key takeaways** | **4 short bullets** | ≤ 10 words each, no sentences |
| Mark complete | button + autoplay toggle | automatic |
| Lesson Q&A | one thread per lesson | students post here |

Worked example, verbatim from lesson 2 of module 1:

> **Lesson summary:** Frontend now has two distinct AI skills, and this program is built to
> give you both — using AI to build your UI, and building AI into the product itself.
>
> **What you will learn:** · The two AI skills the course develops · What "building with AI"
> means · What "building AI in" looks like · How every module ahead maps onto one of these
>
> **Core idea:** One skill makes you faster at shipping frontend; the other makes the product
> itself intelligent. Knowing which you're practising keeps you oriented across all 10 modules.
>
> **Key takeaways:** · Frontend now demands two AI skills, not one · "Building with AI" =
> ship the same-quality UI, faster · "Building AI in" = put AI-powered experiences inside the
> product · The whole course is structured around these two skills

Note what the *Core idea* does: it names the distinction **and** tells the student why it
matters for navigating the rest of the course. Every core idea should orient, not summarise.

## Lesson titles are claims, not topics

The live course never ships a lesson called "Specs" or "Design systems". It ships:

- *"Why specs make AI dramatically better than prompts"*
- *"AI is an employee: micromanage vs delegate"*
- *"Design is no longer only Figma-first"*
- *"Agent safety: what not to delegate and how to review diffs"*

Each one is an argument the lesson then makes. Our module 1 script already does this
(*"The Ladder — One Question, Three Levels"*). Modules 2–14 have topic lists instead, and
that is the main writing job in `lesson-map.md`.

## What Frontend Mastery is missing

| Gap | Where it bites |
|---|---|
| ~~No lesson breakdown for modules 2–14~~ | **Drafted** in `lesson-map.md` — 129 lessons. Needs your editorial pass. |
| **No per-lesson LMS blocks** | Every lesson needs summary / learn / core idea / takeaways written. 129 lessons × 4 blocks. |
| **Module blurbs are topic lists** | They read as syllabus, not as an outcome. Each needs rewriting to end in an aim. |
| **No video numbers** | The git convention (`module-3/v10-utils`, tag `m3-v10-end`) has been waiting on exactly this. The lesson map supplies it. |

The last one is the cheap win: the moment a module's lesson map exists, its exercise branch
can take its real name and its deck slides can carry per-lesson chips, the way module 1's
deck already does.

## Two things the live course does that we should copy

1. **Lesson Q&A per lesson, not per course.** A question attaches to the lesson that caused
   it, so the answer is findable by the next student who hits the same wall. Our plan has a
   weekly live Q&A and a community space; per-lesson threads are a different, better thing.
2. **A named capstone thread running through the modules.** *AI for Frontend* says "add one
   AI feature into the capstone" in module 10 and "final capstone review" as the last lesson.
   We have the same shape with the job board — but only the curriculum deck says so. Each
   module's last lesson should name the slice it just added, the way module 10 does.

## One thing we do that it does not

The exercise repo with three branches per stage, verified by CI. *AI for Frontend* has a
capstone repo but no start/guided/solution contract and no machine checking that the starter
still fails. Keep it; it is the sharpest differentiator in the program and it deserves its
own lesson in module 1 — which it has.
