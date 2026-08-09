# Table Card — print one per table
### DDD MUC · 12 Aug 2026 · From North Star to Working App

**Table #: ______**

**Room North Star Metric:** _______________________________________________

**Our actor (claimed at 18:53):** _________________________________________

**Our core bounded context (named by 20:00 — scopes everything after the break):**

_______________________________________________

---

## The timetable

| Time | Station | Done when… |
|---|---|---|
| 18:00 | *Pizza — roles assigned, skills installed, one chat open* | Facilitator / Driver / Scribe named |
| 18:30 | Welcome & framing *(plenary)* | |
| 18:40 | **1** North Star — diverge, critic at 18:49 | 20+ candidates, top 2 survive the critic |
| 18:53 | *Plenary vote + claim your actor* | NSM and actor written above |
| 19:00 | **2** Domain Story ⭐ | 8–12 sentences, **frozen** |
| 19:32 | **3** Bounded Contexts | 3–6 contexts, contested sentences argued, **core named** |
| 20:00 | *Break + gallery walk* | Driver swapped |
| 20:15 | **4** Glossary **of the core context** | Terms + cardinalities, transcription confirmed |
| 20:37 | **5** The Running Prototype ⭐ | Story walks through it. Link sent by 20:50. |
| 20:52 | Demos — 2 min, one screen | |

⭐ = never cut these two. At 20:37, **fire the build before you discuss anything.**

---

> **The AI never gets the last word.** Every artifact gets corrected by a human here
> before it moves on. One chat all evening. Driver rotates at the break.

**Story scope — same for every table. Say it, then hold it:**

> ### One traveller. One trip. One friend. From getting home to the friend seeing it.

**Skills:** `devils-advocate` (S1) · `domain-story-seeder` (S2) ·
`domain-story-context-finder` (S3) · `domain-story-glossary-consistency` (S4) ·
`prototype-from-domain-story-and-glossary` (S5) — `github.com/Grinseteddy/SamplesDddMeetAi`
**Three propose, two challenge. Build on paper first, then invoke a critic.**

---

## Paste-ready prompts

**1a · Diverge — no skill, just generate**
```
You're a participant in our brainstorm, not the facilitator. We're designing a new app
for sharing vacation experiences. We're in the DIVERGENT phase — no judging.
Give us 15 candidate North Star Metrics. Go wide. One line each, no commentary.
```

**1b · Converge at 18:49**
```
Use the devils-advocate skill. We've stopped generating and we're choosing now.

We're shortlisting a North Star Metric for a vacation-sharing app. Our finalists:
<PASTE 4–5 CANDIDATES>

Which of these is gameable, which measures activity rather than value, and which would
still look healthy while the product quietly fails? Bring the objections you banked.
```

**2a · Seed the story**
```
Use the domain-story-seeder skill.

Domain: an app for sharing vacation experiences.
Focus the story on this actor: <YOUR ACTOR>.
Scope, strictly: one traveller, one trip, one friend, from getting home to the friend
seeing it. Nothing before, nothing after.
No Wardley or capability map — work from this description.
One concrete happy-path story, 8–12 numbered sentences. Flag every guess you made.
```

**2b · Challenge the corrected story**
```
Play a respectful devil's advocate on our corrected domain story below. This is an as-is
story for <YOUR ACTOR>, deliberately scoped to one trip and one friend.

Which verbs are UI language rather than domain language? Which actor is collapsed or
missing? Where does the sequence not survive contact with reality?

<PASTE THE NUMBERED STORY>
```
→ then **freeze it**: paste the final numbered story back into the chat.

**3 · Draw your own rings first, then** *(attach photo/export with rings on it)*
```
Use the domain-story-context-finder skill on the frozen story earlier in this chat.
We've drawn our own cut — the rings in the photo. Propose your cut, justify each
boundary from evidence in the story, and tell us where you disagree with ours.
Show the contested sentences and the alternative cuts.
```
→ *"Which side does this sentence belong on, and why?"* → 2 axes → **name the core.**

**4a · Glossary of the core context only** *(attach photo/export)*
```
Read this visual glossary. It covers only the <CORE CONTEXT> bounded context of the
domain story we froze earlier in this chat. Transcribe it, confirm the transcription
with us, then give us the term catalogue and the derived model — entities, value
objects, aggregates, identity.
```

**4b · Cross-check**
```
Use the domain-story-glossary-consistency skill on the frozen story and this glossary.
Scope: the glossary deliberately covers only the <CORE CONTEXT> context, so treat story
terms outside that context as out of scope rather than as gaps.
```

**5a · Fire the build at 20:37 — before discussing anything**
```
Use the prototype-from-domain-story-and-glossary skill.
- Domain story: the frozen numbered story earlier in this chat, scoped to the
  <CORE CONTEXT> bounded context.
- Visual glossary: the one we just interpreted.
- Formatting example: none — go ahead without it and design a plain one.
Build the clickable prototype. Use the glossary's exact term names in all labels.
```
*While it renders: agree the three demo sentences. No screen needed.*

**5b · One fix round after walking the story through**
```
Walking our story through the prototype: at step <n>, <ACTOR> can't <VERB> the
<WORK OBJECT> — there's no way to do it. Fix that screen only.
```

---

## Say these out loud when you need them

- "Stop reading. What's wrong with it?"
- "Is that really how it goes?"
- "What do you call that when you're not looking at a screen?"
- "Who at this table knows that's true?"
- "That's story two — we're still in story one."
- "Where does the language change?"
- "Which side does this sentence belong on?"
- "Does it speak our language, or did it invent words?"

## Demo — 2 minutes, three sentences

1. Our actor is ___ and here's the moment that mattered.
2. The core context turned out to be ___, which surprised us because ___.
3. Here's the one screen worth seeing.

**Link to the host by 20:50.**