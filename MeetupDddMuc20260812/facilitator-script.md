# Table Facilitator Script
## DDD MUC — "From North Star to Working App"
**Wed 12 Aug 2026 · codecentric AG, August-Everding-Str. 20, München**

---

## The timetable

| Time | What | Length |
|---|---|---|
| 18:00 | Pizza, arrival — **assign roles, install skills, open the one chat** | 30 min |
| 18:30 | Welcome & framing *(plenary)* | 10 min |
| 18:40 | **1 · North Star Metric** — diverge → `devils-advocate` → plenary vote **+ tables claim an actor** | 20 min |
| 19:00 | **2 · Domain Story** ⭐ | 32 min |
| 19:32 | **3 · Bounded Contexts** — name the core | 28 min |
| 20:00 | **Break + gallery walk** — driver swaps | 15 min |
| 20:15 | **4 · Visual Glossary of the core context** | 22 min |
| 20:37 | **5 · The Running Prototype** ⭐ | 15 min |
| 20:52 | Demos — 2 min per table, one screen | 8 min |
| 21:00 | End | |

⭐ = never cut these two.

**Five stations, five skills, one chat.** Each station's output is the next one's input:

```
North Star ─► Domain Story ─┬─► Bounded Contexts ─► (core context scopes everything below)
                            └─► Glossary of the core ─┐
                                                      └─► Prototype
```

---

## 0. Read this first (5 minutes, over pizza)

### The shape of the evening

The whole room converges on **one** North Star Metric and each table claims a **different
actor**. From there every table carries its actor end-to-end to its own running prototype.
At 20:52 the tables demo — together they form one app, seen from several angles.

Say this at your table early: **you are not building the same thing as the next table.**
It removes the "are we allowed to be different?" question that otherwise eats ten minutes.

### The cardinal rule — say it out loud

> **The AI never gets the last word.** Every artifact it produces gets corrected by a
> human at this table before it moves to the next station.

If your table goes quiet and stares at a screen, you have lost the session. Your single
most important intervention all evening is:

> "Stop reading. What's wrong with it?"

### The skills each table needs — install before 18:30

All from **Grinseteddy/SamplesDddMeetAi**. Installed on both laptops *before* the pizza
runs out; a table installing skills at 18:35 has already lost Station 1.

| Station | Skill | Link |
|---|---|---|
| 1 · North Star | `devils-advocate` | [Chapter04/Skills/BrainstormingSkill](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter04/Skills/BrainstormingSkill) |
| 2 · Domain Story | `domain-story-seeder` | [Chapter06/Skills/DomainStorySeederSkill](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter06/Skills/DomainStorySeederSkill) |
| 3 · Bounded Contexts | `domain-story-context-finder` | [Chapter06/Skills/ProposeBoundedContextsForADomainStory](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter06/Skills/ProposeBoundedContextsForADomainStory) |
| 4 · Glossary | `domain-story-glossary-consistency` | [Chapter07/CheckConsistencyBetweenGlossaryAndStory](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter07/CheckConsistencyBetweenGlossaryAndStory) |
| 5 · Prototype | `prototype-from-domain-story-and-glossary` | [Chapter07/Skills/ProtypeSkillWithVisualGlossary](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter07/Skills/ProtypeSkillWithVisualGlossary) |

**Three propose, two challenge.** The seeder, the context finder and the prototype skill
*make* something; the devil's advocate and the consistency check *argue with* what your
table already made. Know which kind you're firing: **build on paper first, then invoke a
critic.** A critic pointed at an empty board gives you a lecture instead of a critique.

**`devils-advocate` waits for convergence — by design.** It holds its fire while a group is
still generating. So at Station 1 you diverge *without* it and invoke it only when the
table starts choosing.

**The prompts below use these exact names.** If an installed `SKILL.md` has a different
`name:` field, correct the prompt — otherwise it silently falls back to a generic answer,
and you won't notice, because generic answers look plausible. They're just thinner.

### One chat per table

Open **one** Claude conversation at 18:30 and keep it all evening. Context carries forward
and later stations get much sharper. Don't start a fresh chat per station.

### Roles — assign during pizza, not at 18:30

| Role | Who | Job |
|---|---|---|
| **Facilitator** | you | Timebox, airtime, phase discipline. You don't decide content. |
| **Driver** | one volunteer with a laptop | Types prompts, reads output aloud. **Rotates at the break.** |
| **Scribe** | one volunteer | Stickies and marker. Takes the photos. |
| **Everyone else** | 3–5 people | Domain experts. They have all been on holiday. That's the expertise. |

Ideal table size **5–7**. At 8+, split. At 3, merge.

### Photo hygiene (three of the five skills read pictures)

Straight-on, whole board in frame, no shadow, flash off, room light on. A bad photo
produces a confident misreading and you'll spend five minutes undoing it.

### Materials per table

Stickies (3 colours), thick markers, A1 paper or a wall slot, 1–2 laptops with the five
skills already installed, a phone for photos, this script, the table card.

---

## Plenary — 18:30 to 19:00 *(host leads; you sit with your table)*

**18:30 Welcome & framing (10 min).** Host explains the arc and the cardinal rule.

**18:40 Station 1 — North Star Metric (20 min).** *The first half is yours.*

Say:

> "Before we design anything: what value should a vacation-sharing app actually create?
> We're diverging — quantity, no judging, no 'yes but'. Claude is in this with us as a
> participant, not as the answer."

Driver pastes (no skill here — divergence needs no scaffolding):

```
You're a participant in our brainstorm, not the facilitator. We're designing a new app
for sharing vacation experiences. We're in the DIVERGENT phase — no judging.

Give us 15 candidate North Star Metrics for it. Go wide: some obvious, some wild. One
line each, no commentary.
```

Table generates **on stickies at the same time** — nobody waits for the output. Then read
Claude's 15 aloud and steal, combine, hitchhike. Target 20+ on the table.

**At 18:49 — shortlist 4–5, then bring in the critic:**

```
Use the devils-advocate skill. We've stopped generating and we're choosing now.

We're shortlisting a North Star Metric for a vacation-sharing app. Our finalists:
<PASTE 4–5 CANDIDATES>

Which of these is gameable, which measures activity rather than value, and which would
still look healthy while the product quietly fails? Bring the objections you banked.
```

Pick your **top 2**, write them big, one person carries them to the plenary wall.

**18:53 Plenary (7 min).** Host runs dot-voting to **one** room-wide NSM, then reads out a
list of actors and **each table claims one** — no two tables the same. Write both the NSM
and your actor on the table card. Everything downstream hangs off them.

---

## Station 2 — Domain Story · 19:00–19:32 (32 min) ⭐

**Goal:** discover how "sharing a vacation" really works for your actor.
**Output:** a corrected, numbered domain story. **Everything after this reads it. Protect
this timebox.**

### Scope it before you start — this is the whole trick

Write this on the board and say it out loud:

> **One traveller. One trip. One friend. From getting home to the friend seeing it.**

Same boundary for every table. Domain stories only sprawl when nobody says where they end.
**Eight to twelve sentences.** If the table is at sentence 15, you've drifted outside the
boundary — go back and cut, don't keep going.

**Minute 0–4 — teach the grammar.**

```
<n>  <Actor>  <activity verb>  <work object>
```

> "One concrete scenario. Present tense. No if-then, no 'usually'. If you need a
> conditional, you've got two stories — pick one."

**Minute 4–9 — seed a strawman.** Name the focus explicitly, or the skill will stop and ask:

```
Use the domain-story-seeder skill.

Domain: an app for sharing vacation experiences.
Focus the story on this actor: <YOUR ACTOR>.
Scope, strictly: one traveller, one trip, one friend, from getting home to the friend
seeing it. Nothing before, nothing after.
No Wardley or capability map — work from this description.
One concrete happy-path story, 8–12 numbered sentences. Flag every guess you made.
```

**Minute 9–24 — the room corrects it.** *This is the actual work, and now it has room to
breathe.* Read the seeded story aloud one sentence at a time. After each:

> "Is that really how it goes? Who actually does that? What's it called here?"

The scribe rewrites corrected sentences on stickies. **Expect to throw away half — that's
the design, not a failure.** A wrong strawman is what makes people talk.

Three smells worth interrupting for:
- **CRUD or UI verbs** — "creates", "manages", "clicks", "uploads". Ask: "what do you call
  that when you're not looking at a screen?"
- **A missing external system** — the phone's photo library, the map service, the friend's
  messaging app. They're actors too.
- **Drift past the boundary** — anyone who says "and then later..." is starting story two.

**Minute 24–29 — challenge it.**

```
Play a respectful devil's advocate on our corrected domain story below. This is an as-is
story for <YOUR ACTOR>, deliberately scoped to one trip and one friend.

Which verbs are UI language rather than domain language? Which actor is collapsed or
missing? Where does the sequence not survive contact with reality?

<PASTE THE NUMBERED STORY>
```

**Minute 29–32 — fix and freeze.** Apply what you accept. Then **paste the final numbered
story into the chat as plain text** and say "this is our frozen domain story." You will
reuse it three times.

---

## Station 3 — Bounded Contexts & Core Domain · 19:32–20:00 (28 min)

**Goal:** cut the story into bounded contexts and name the one worth investing in.
**Output:** 3–6 named contexts, contested sentences argued, a core named.
**Everything after the break happens inside the core context you name here.**

> "We're not inventing anything new. Everything we need is the story on the wall —
> we're just standing further back from it."

**Minute 0–7 — the table cuts first.** Draw rings around groups of sentences in the frozen
story. Where would *you* put the seams? Name each in **domain language** (`Trip Curation`,
not `Content Service`).

Two questions do most of the work:
- **Where does the language change?** When the same word starts meaning something
  different, you've found a boundary.
- **Which cut could a competitor buy off the shelf?** That one isn't your core.

Don't skip this. The skill's proposal is only interesting *against* a cut of your own.

**Minute 7–13 — the skill proposes.**

```
[attach photo/export of your story with your rings drawn on it]

Use the domain-story-context-finder skill on the frozen story earlier in this chat.
We've drawn our own cut — the rings in the photo. Propose your cut, justify each
boundary from evidence in the story, and tell us where you disagree with ours.
Show the contested sentences and the alternative cuts.
```

**Minute 13–22 — argue the contested sentences.** *This is the station.* Take the sentences
the skill flags and put them to the table one at a time:

> "Which side does this sentence belong on, and why?"

A sentence both contexts want is usually a missing concept, a hidden handoff, or a
published-language boundary. Say that out loud when you see it — it's the densest DDD in
the evening, and you now have nine minutes for it instead of five.

**Minute 22–28 — name the core.** Draw two axes: **business differentiation** (left→right)
× **model complexity** (bottom→top). Place each context, then:

> "Which one is core, and who disagrees?"

Take the dissent, don't resolve it, write both names down. **Write the core context on your
table card before the break** — the whole second half is scoped to it.

**If you're behind:** skip the axes. Ask "which of these is core?", take one dissent, move on.

---

## Break · 20:00–20:15 (15 min) — a working break

Drinks, and a **gallery walk**: every table leaves its story and context cut visible, one
person stays to answer questions, everyone else walks. Two minutes per table.

**Rotate the driver.** Whoever typed in the first half doesn't type in the second.

Honest checkpoint: if your story isn't frozen or you haven't named a core context, spend
the first five minutes of the break finishing that rather than walking. Everything after
20:15 depends on both.

---

## Station 4 — Visual Glossary of the Core Context · 20:15–20:37 (22 min)

**Goal:** pin down what the things in *the core context* are called and what shape they are.
**Output:** a glossary the prototype will speak.

> "Not the whole app. Just the context we said was worth investing in."

Scoping to one context is what makes 22 minutes enough to go deep instead of wide.

**Minute 0–10 — build it from the core context's nouns.** Take only the story sentences
inside your core ring. Underline every work object. One sticky per term, **exact business
spelling**. Draw labelled lines between them, put a multiplicity on at least one end:
`1`, `0..1`, `1..*`, `0..25`.

Force the argument that matters: **is this a thing of its own, or a field on something
else?** Is a `Moment` its own entity, or an attribute of a `Trip`? Does a `Photo` exist
without a `Trip`? That argument is the whole point of the station.

**Minute 10–16 — read it back.**

```
[attach photo/export of the glossary]

Read this visual glossary. It covers only the <CORE CONTEXT> bounded context of the
domain story we froze earlier in this chat. Transcribe it, confirm the transcription
with us, then give us the term catalogue and the derived model — entities, value
objects, aggregates, identity.
```

**Confirm the transcription before you let it move on.** One misread edge poisons the
prototype, and the failure is silent.

**Minute 16–22 — cross-check against the story.**

```
Use the domain-story-glossary-consistency skill on the frozen story and this glossary.
Scope: the glossary deliberately covers only the <CORE CONTEXT> context, so treat story
terms outside that context as out of scope rather than as gaps.
```

Read the findings aloud. Contradictions between story and glossary are **real findings
about the domain**, not clerical errors. Fix whichever artifact is wrong.

**If you're behind:** skip the cross-check. Never skip the transcription confirmation.

---

## Station 5 — The Running Prototype · 20:37–20:52 (15 min) ⭐

**Goal:** something that opens on a phone — the core context's app, not a generic one.

**Minute 0 — fire the build immediately. Don't discuss it first.**

```
Use the prototype-from-domain-story-and-glossary skill.

- Domain story: the frozen numbered story earlier in this chat, scoped to the
  <CORE CONTEXT> bounded context.
- Visual glossary: the one we just interpreted.
- Formatting example: none — go ahead without it and design a plain one.

Build the clickable prototype. Use the glossary's exact term names in all labels.
```

**Minute 0–4, while it renders — prep the demo.** No screen needed. Agree three sentences:

1. *"Our actor is ___ and here's the moment that mattered."*
2. *"The core context turned out to be ___, which surprised us because ___."*
3. *"Here's the one screen worth seeing."*

**Minute 4–11 — walk the story through the UI.** Read the frozen story aloud, sentence by
sentence, and do each one in the prototype. When a sentence has no screen that supports it,
that's your finding — a gap between model and app, not a bug.

Then **one** round of fixes, no more:

```
Walking our story through the prototype: at step <n>, <ACTOR> can't <VERB> the
<WORK OBJECT> — there's no way to do it. Fix that screen only.
```

**Minute 11–15 — the vocabulary check.** Glossary open next to the app:

> "Does it speak our language, or did it invent words?"

Every label should be a glossary term. Where it isn't, decide as a table: glossary gap, or
AI drift? Telling those two apart is a good last thing to do together.

**Send the link to the host by 20:50.**

---

## Plenary — 20:52–21:00 · Demos & Reflection

Two minutes per table, hard stop, host times it. One screen, three sentences, no full
click-through. Then the closing question:

> "What was the distance between the metric and the screen — and where did it get lost?"

Ask your table to name **one thing the AI got wrong that a human at the table caught.**
Those are the best stories of the night.

---

## Rescue kit — what will actually go wrong

| Symptom | What to do |
|---|---|
| **Table goes silent, reading output** | "Stop reading. What's wrong with it?" Turn the laptop away for 60 seconds. |
| **The story is at sentence 15 and climbing** | You're outside the boundary. One traveller, one trip, one friend. Cut back. |
| **One person owns the keyboard all evening** | Driver rotates at the break. Enforce it. |
| **The AI invents a domain fact and nobody notices** | "Who at this table knows that's true?" Silence = it's a guess, mark it red. |
| **The artifact is beautiful and wrong** | Beauty is not agreement. Walk the story through it out loud. |
| **You reach the break without a frozen story or a named core** | Finish it in the first 5 min of the break. Skip the gallery walk. |
| **You're behind after the break** | Cut the glossary cross-check. Never cut the transcription confirmation or the story walk-through. |
| **A skill stalls asking clarifying questions** | Answer in one line and add "go ahead with what you have." Don't let it negotiate. |

## The four things you must not lose

1. **The frozen domain story** (Station 2) — everything downstream reads it.
2. **The core context name** (Station 3) — it scopes the whole second half.
3. **The glossary** (Station 4) — the vocabulary the prototype speaks.
4. **The prototype link** (Station 5) — to the host by 20:50 for the demo.

Everything else is disposable scaffolding. Say that when your table starts polishing a
sticky note.

---

## Host prep option: pre-seed the stories

If you'd rather buy Station 2 another ten minutes, run `domain-story-seeder` yourself
beforehand — once per actor, printed, one per table. Tables then open Station 2 with a
wrong strawman already in hand and spend the full 32 minutes correcting it.

**Trade-off:** you lose the moment where the room watches a story get generated, which is
part of what people came to see. You gain a calmer station and a better story. If your
facilitators are volunteers recruited on the night, pre-seed. If they're experienced,
generate live.