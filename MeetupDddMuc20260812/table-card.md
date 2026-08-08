# Table Facilitator Script
## DDD MUC — "From North Star to Working App"
**Wed 12 Aug 2026 · codecentric AG, August-Everding-Str. 20, München**
**18:00 pizza & arrival · 18:30 session starts · 20:00 break · 21:00 end**

---

## 0. Read this first (5 minutes, over pizza)

### The shape of the evening

The whole room converges on **one** North Star Metric. After that, **each table takes a
different actor/impact from the shared impact map and carries it end-to-end** to its own
running prototype. At 20:50 the tables demo — together they form one app, seen from
several angles.

This matters for you: **you are not building the same thing as the next table.** Say so
at your table, early. It removes the "are we allowed to be different?" question that
otherwise eats ten minutes.

### The cardinal rule — say it out loud at your table

> **The AI never gets the last word.** Every artifact it produces gets corrected by a
> human at this table before it moves to the next station.

The skills are built as *participants* — a brainstorm partner, a devil's advocate, a
critic. They are not the modeller. If your table goes quiet and stares at a screen,
you have lost the session. Your single most important intervention all evening is:

> "Stop reading. What's wrong with it?"

### The skills each table needs — install before 18:30

All from **Grinseteddy/SamplesDddMeetAi**. Have them installed on both laptops *before*
the pizza runs out; a table installing skills at 18:35 has already lost Station 1.

| Station | Skill | Link |
|---|---|---|
| 1 · NSM convergence | `devils-advocate` | [Chapter04/Skills/BrainstormingSkill](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter04/Skills/BrainstormingSkill) |
| 2 · Impact Map | `impact-mapping-critic` | [Chapter04/Skills/ImpactMappingSkill](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter04/Skills/ImpactMappingSkill) |
| 3 · Domain Story | `domain-story-seeder` | [Chapter06/Skills/DomainStorySeederSkill](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter06/Skills/DomainStorySeederSkill) |
| 4 · Bounded Contexts | `domain-story-context-finder` | [Chapter06/Skills/ProposeBoundedContextsForADomainStory](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter06/Skills/ProposeBoundedContextsForADomainStory) |
| 5 · Visual Glossary | `domain-story-glossary-consistency` | [Chapter07/CheckConsistencyBetweenGlossaryAndStory](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter07/CheckConsistencyBetweenGlossaryAndStory) |
| 6 · Prototype | `prototype-from-domain-story-and-glossary` | [Chapter07/Skills/ProtypeSkillWithVisualGlossary](https://github.com/Grinseteddy/SamplesDddMeetAi/tree/main/Chapter07/Skills/ProtypeSkillWithVisualGlossary) |

**Three propose, three challenge.** The seeder, the context finder and the prototype skill
*make* something; the devil's advocate, the impact-mapping critic and the consistency check
*argue with* what your table already made. Know which kind you're firing: **build on paper
first, then invoke a critic.** A critic pointed at an empty board gives you a lecture
instead of a critique.

**`devils-advocate` waits for convergence — by design.** It holds its fire while a group is
still generating and brings its objections when the group starts choosing. So at Station 1
you diverge *without* it, and invoke it in the last three minutes when the table picks its
top two. Firing it at minute one would suppress exactly the half-formed ideas you want.

**The prompts use these exact names.** If an installed `SKILL.md` has a different `name:`
field, correct the prompt — otherwise it silently falls back to a generic answer, and you
won't notice, because generic answers look plausible. They're just thinner.

**Six stations, six skills, one chat.** Every station has a skill behind it now. The chat
carries the story and glossary forward, so from Station 4 onward you mostly point the
skills at material that's already in the conversation.

### One chat per table

Open **one** Claude conversation at 18:30 and keep it for the entire evening. Context
carries forward and later stations get much sharper. Don't start a fresh chat per station.

### Roles — assign during pizza, not at 18:30

| Role | Who | Job |
|---|---|---|
| **Facilitator** | you | Timebox, airtime, phase discipline. You don't decide content. |
| **Driver** | one volunteer with a laptop | Types prompts, reads output aloud. **Rotates at the break.** |
| **Scribe** | one volunteer | Stickies and marker. Takes the photos. |
| **Everyone else** | 3–5 people | Domain experts. They have all been on holiday. That's the expertise. |

Ideal table size is **5–7**. At 8+, split. At 3, merge.

### The long stretch

There are **four stations between 18:30 and the break at 20:00** with no pause. That's a
long time to hold a room's attention. Around 19:18, when Station 3 starts, tell people to
stand up for 60 seconds and refill a glass. It buys you the last half hour.

### Photo hygiene (half the skills read photos)

Straight-on, whole board in frame, no shadow across it, phone flash off, room light on.
A bad photo produces a confident misreading and you'll spend five minutes undoing it.

### Materials per table

Stickies (3 colours minimum), thick markers, A1 paper or a wall slot, 1–2 laptops with
Claude and **the five skills already installed**, a phone for photos, this script, the
table card.

---

## Plenary — 18:30 to 19:00 *(host leads; you sit with your table)*

**18:30 Welcome & framing (10 min).** Host explains the arc and the cardinal rule.

**18:40 Station 1 — NSM divergence, at tables (12 min).** *This one is yours.*

Say:

> "Before we design anything: what value should a vacation-sharing app actually create?
> We're diverging — quantity, no judging, no 'yes but'. Ten minutes. Claude is in this
> with us as a brainstorm partner, not as the answer."

Driver pastes:

```
You're a participant in our brainstorm, not the facilitator. We're designing a new app
for sharing vacation experiences. We're in the DIVERGENT phase — no judging.

Give us 15 candidate North Star Metrics for it. Go wide: some obvious, some wild. One
line each, no commentary.
```

Table generates **on stickies at the same time** — do not let people wait for the output.
Then read Claude's 15 aloud and steal, combine, hitchhike. Target: 20+ on the table.

**Last 3 minutes — converge, and now bring in the critic.** Shortlist 4–5 candidates, then:

```
Use the devils-advocate skill. We've stopped generating and we're choosing now.

We're shortlisting a North Star Metric for a vacation-sharing app. Our finalists:
<PASTE 4–5 CANDIDATES>

Which of these is gameable, which measures activity rather than value, and which would
still look healthy while the product quietly fails? Bring the objections you banked.
```

Pick your **top 2**, write them big, and one person carries them to the plenary wall.

**18:52 Plenary convergence (8 min).** Host runs dot-voting to **one** room-wide NSM.
Write the winning NSM on your table card. Everything downstream hangs off it.

---

## Station 2 — Impact Map · 19:00–19:18 (18 min)

**Goal:** the shared NSM → the actors we must reach and the behaviours we must change.
**Output:** a four-level impact map on paper + a critique the table has answered.

**Minute 0–2 — frame it.**

> "Four levels. WHY is fixed — it's the room's North Star. WHO can reach it. HOW must
> their behaviour change. WHAT could we build to cause that. The WHATs are *options*,
> not promises."

**Minute 2–11 — the table draws it.** Paper and stickies only. Laptop closed.
Push for **at least 4 actors**, and insist on at least one who isn't the obvious traveller
(the friend who receives it, the person in the photo who didn't consent, the platform,
the person who wasn't invited on the trip).

Watch for the two classic failures and name them when you see them:
- **A solution posing as a goal** ("increase feed engagement" is not a why).
- **A feature posing as an impact** ("gets push notifications" is not a behaviour change).

**Minute 11–15 — the critic.** Scribe photographs the map. Driver pastes:

```
[attach photo of the impact map]

Use the impact-mapping-critic skill. Play devil's advocate on our impact map.
Our North Star Metric is: "<PASTE THE ROOM'S NSM>".
There's no Business Model Canvas — critique on internal logic and tell us what you
can't read from the photo.
```

**Minute 15–18 — answer it, don't obey it.** Round-robin: everyone picks **one** finding
they think is wrong, and one they think is fatal. Change the paper map accordingly. It is
completely fine to reject findings — say so at the table, loudly, so people learn the
posture.

**Carry forward:** your table's **chosen actor** and **one impact** for that actor. Announce
it to the host so no two tables pick the same actor.

**If you're behind:** cut the critic to 3 minutes and only ask "which of our impacts is
actually a feature in disguise?"

---

## Station 3 — Domain Story · 19:18–19:42 (24 min)

*Start with a 60-second stand-up-and-stretch. Then go.*

**Goal:** discover how "sharing a vacation" really works for your actor.
**Output:** a corrected, numbered domain story. **This is the most valuable artifact of the
evening — it is the required input for the prototype at Station 7. Protect this timebox.**

**Minute 0–3 — teach the grammar.** Write it on the board:

```
<n>  <Actor>  <activity verb>  <work object>
```

> "One concrete scenario. Present tense. No if-then, no 'usually'. If you need a
> conditional, you've got two stories — pick one."

**Minute 3–8 — seed a strawman.** Driver pastes (name the focus explicitly, or the skill
will stop and ask you to pick one — you don't have time for that round-trip):

```
Use the domain-story-seeder skill.

Domain: an app for sharing vacation experiences.
Focus the story on this actor and behaviour: <ACTOR> — <IMPACT FROM STATION 2>.
No Wardley or capability map — work from this description.
Give us one concrete happy-path story, 8–12 numbered sentences, and flag your guesses.
```

**Minute 8–17 — the room corrects it.** *This is the actual work of the station.* Read the
seeded story aloud, one sentence at a time. After each, ask:

> "Is that really how it goes? Who actually does that? What's it called here?"

The scribe rewrites corrected sentences on stickies. **Expect to throw away half of it —
that's the design, not a failure.** A wrong strawman is what makes people talk.

Two smells you should interrupt for:
- **CRUD or UI verbs** — "creates", "manages", "clicks", "uploads". Ask: "what do you call
  that when you're not looking at a screen?"
- **A missing external system** — the phone's photo library, the map service, the friend's
  messaging app. They're actors too.

**Minute 17–22 — the critic.** Photo of the sticky story, or paste the corrected text:

```
Play a respectful devil's advocate on our corrected domain story below. This is an as-is story for the actor <ACTOR>.

<PASTE THE NUMBERED STORY>
```

**Minute 22–24 — fix and freeze.** Apply what you accept. Then **paste the final numbered
story into the chat as plain text** and say "this is our frozen domain story." You will
reuse it twice.

---

## Station 4 — Bounded Contexts & Core Domain · 19:42–20:00 (18 min)

**Goal:** cut the story into bounded contexts and name the one worth investing in.
**Output:** 3–6 named contexts, the contested sentences argued, and a core.
**Everything after the break happens inside the core context you name here.**

> "We're not inventing anything new. Everything we need is the story on the wall —
> we're just standing further back from it."

**Minute 0–5 — the table cuts first.** Go to the frozen story and draw rings around groups
of sentences. Where would *you* put the seams? Name each in **domain language**
(`Trip Curation`, not `Content Service`).

Two questions do most of the work:
- **Where does the language change?** When the same word starts meaning something
  different, you've found a boundary.
- **Which cut could a competitor buy off the shelf?** That one isn't your core.

Don't skip this. The skill's proposal is only interesting *against* a cut of your own.

**Minute 5–10 — the skill proposes.**

```
[attach photo/export of your story with your rings drawn on it]

Use the domain-story-context-finder skill on the frozen story earlier in this chat.
We've drawn our own cut — the rings in the photo. Propose your cut, justify each
boundary from evidence in the story, and tell us where you disagree with ours.
Show the contested sentences and the alternative cuts.
```

**Minute 10–15 — argue the contested sentences.** *This is the station.* Take the sentences
the skill flags and put them to the table one at a time:

> "Which side does this sentence belong on, and why?"

A sentence both contexts want is usually a missing concept, a hidden handoff, or a
published-language boundary. Say that out loud when you see it.

**Minute 15–18 — name the core.** Draw two quick axes: **business differentiation**
(left→right) × **model complexity** (bottom→top). Place each context, then:

> "Which one is core, and who disagrees?"

Take the dissent, don't resolve it, write both names down. **Write the core context on
your table card before you go to the break** — the whole second half is scoped to it.

**If you're behind:** skip the axes. Ask "which of these is core?", take one dissent, move on.

---

## Break · 20:00–20:15 (15 min) — and it's a working break

Drinks, and a **gallery walk**: every table leaves its impact map, domain story and context
cut visible. One person stays to answer questions, everyone else walks. Two minutes per table.

**Rotate the driver before you restart.** Whoever typed in the first half doesn't type in
the second.

This is also your honest checkpoint. If your domain story isn't frozen, or you haven't
named a core context, spend the first five minutes of the break finishing that rather than
walking. Everything after 20:15 depends on both.

---

## Station 5 — Visual Glossary of the Core Context · 20:15–20:33 (18 min)

**Goal:** pin down what the things in *the core context* are called and what shape they are.
**Output:** a glossary the prototype will speak.

> "Not the whole app. Just the context we said was worth investing in."

Scoping this to one context is what makes 18 minutes enough to go deep instead of wide.

**Minute 0–8 — build it from the core context's nouns.** Take only the story sentences
inside your core ring. Underline every work object. One sticky per term, **exact business
spelling**. Draw labelled lines between them, and put a multiplicity on at least one end:
`1`, `0..1`, `1..*`, `0..25`.

Force the argument that matters: **is this a thing of its own, or a field on something
else?** Is a `Moment` its own entity, or an attribute of a `Trip`? Does a `Photo` exist
without a `Trip`? That five-minute argument is the whole point of the station.

**Minute 8–13 — read it back.**

```
[attach photo/export of the glossary]

Read this visual glossary. It covers only the <CORE CONTEXT> bounded context of the
domain story we froze earlier in this chat. Transcribe it, confirm the transcription
with us, then give us the term catalogue and the derived model — entities, value
objects, aggregates, identity.
```

**Confirm the transcription before you let it move on.** One misread edge poisons the
prototype, and the failure is silent.

**Minute 13–18 — cross-check against the story.**

```
Use the domain-story-glossary-consistency skill on the frozen story and this glossary.
Scope: the glossary deliberately covers only the <CORE CONTEXT> context, so treat story
terms outside that context as out of scope rather than as gaps.
```

Read the findings aloud. Contradictions between story and glossary are **real findings
about the domain**, not clerical errors. Fix whichever artifact is wrong.

**If you're behind:** skip the cross-check. Never skip the transcription confirmation.

---

## Station 6 — The Running Prototype · 20:33–20:50 (17 min)

**Goal:** something that opens on a phone — and it's the core context's app, not a generic one.

**Minute 0 — fire the build immediately.** Don't discuss it first:

```
Use the prototype-from-domain-story-and-glossary skill.

- Domain story: the frozen numbered story earlier in this chat, scoped to the
  <CORE CONTEXT> bounded context.
- Visual glossary: the one we just interpreted.
- Formatting example: none — go ahead without it and design a plain one.

Build the clickable prototype. Use the glossary's exact term names in all labels.
```

**Minute 0–5, while it renders — prep the demo.** No screen needed for this. Agree the
three sentences as a table:

1. *"Our actor is ___ and the behaviour we wanted to change is ___."*
2. *"The core context turned out to be ___, which surprised us because ___."*
3. *"Here's the one screen worth seeing."*

**Minute 5–13 — walk the story through the UI.** Read the frozen story aloud, sentence by
sentence, and do each one in the prototype. When a sentence has no screen that supports it,
that's your finding — a gap between the model and the app, not a bug.

Then **one** round of fixes, no more:

```
Walking our story through the prototype: at step <n>, <ACTOR> can't <VERB> the
<WORK OBJECT> — there's no way to do it. Fix that screen only.
```

**Minute 13–17 — the vocabulary check.** Glossary open next to the app:

> "Does it speak our language, or did it invent words?"

Every label should be a glossary term. Where it isn't, decide as a table: glossary gap, or
AI drift? Telling those two apart is a good last thing to do together.

**Send the link to the host by 20:48.** Two minutes, one screen, three sentences.

---

## Plenary — 20:50–21:00 · Demos & Reflection

Two minutes per table, hard stop, host times it. Then the closing question:

> "What was the distance between the metric and the screen — and where did it get lost?"

Ask your table to name **one thing the AI got wrong that a human at the table caught.**
Those are the best stories of the night, and they're the answer to the question the
meetup description asks.

---

## Rescue kit — the six things that will actually go wrong

| Symptom | What to do |
|---|---|
| **Table goes silent, reading output** | "Stop reading. What's wrong with it?" Turn the laptop away from the table for 60 seconds. |
| **One person owns the keyboard all evening** | Driver rotates at the break. Enforce it. |
| **The AI invents a domain fact and nobody notices** | Ask "who at this table knows that's true?" Silence = it's a guess, mark it. |
| **The artifact is beautiful and wrong** | Beauty is not agreement. Walk the story through it out loud. |
| **You reach the break without a frozen story or a named core context** | Finish it in the first 5 min of the break. Skip the gallery walk. |
| **You're behind after the break** | Cut the glossary cross-check. Never cut the transcription confirmation or the story walk-through. |
| **A skill stalls asking clarifying questions** | Answer in one line and add "go ahead with what you have." Don't let it negotiate. |

## The three artifacts you must not lose

1. **The frozen domain story** (Station 3) — everything downstream reads it.
2. **The core context name** (Station 4) — it scopes the whole second half.
3. **The glossary** (Station 5) — the vocabulary the prototype speaks.
4. **The prototype link** (Station 6) — send it to the host by 20:48 for the demo.

Everything else is disposable scaffolding. Say that to your table when they start
polishing a sticky note.