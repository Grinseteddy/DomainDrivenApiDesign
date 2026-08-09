# Miro Annex
## DDD MUC · 12 Aug 2026 · "From North Star to Working App"
*Read alongside the facilitator script. Nothing in the main script changes — this only
tells you where the board replaces the wall, and where it doesn't.*

---

## The rule of thumb

**Miro is the record and the input pipeline. Paper is the workspace.**

Use the board where the artifact needs to be *read by a skill* or *survive the evening*.
Use paper where the artifact needs six people arguing over it at once.

### Opt-in, not mandatory

Tables choose at 18:00. Mixed tables in one room is fine and actually interesting — the
comparison is worth a line in the closing reflection.

**A table may only choose Miro if it has two devices.** Board device and prompt device
must be different. One laptop = paper table, no exceptions. The failure this prevents is
the whole table leaning over one screen while one person drives, which is the exact
opposite of what the evening is for.

---

## Per-station call

| # | Station | Board or paper | Why |
|---|---|---|---|
| 1 | North Star | **Either** | Board is fine — parallel typing works here, and quantity is the goal |
| 2 | Domain Story | **Paper** ⚠️ *(or egon.io)* | The station where a mouse pointer becomes an accidental talking stick |
| 3 | Bounded Contexts | **Board** | Rings get redrawn constantly, and contested sentences are easier to drag than to rewrite |
| 4 | Visual Glossary (core context) | **Board** ✅ | Biggest win: cardinalities read perfectly, no photo misreads |
| 5 | Prototype | n/a | Paste the prototype link into the board's last frame |

**Station 2 (Domain Story) is the one to defend.** If a table wants a digital story, point them at
**egon.io** — it's purpose-built for Domain Storytelling, and its export is read directly
by the `domain-story-interpreter` skill, so you skip the photo step entirely. If they use
egon.io, they still read each sentence aloud and correct it as a group. The medium changes;
the ritual doesn't.

---

## Board template — build this before the event

One Miro board **per table** (not one shared board — tables carry different actors and
will collide). Seven frames, left to right, each pre-labelled:

1. **Table info** — table number, room NSM and actor (blank, filled at 18:53), core context (blank, filled at 20:00)
2. **S1 · North Star candidates** — empty canvas
3. **S2 · Domain Story** — *photo drop zone* (or egon.io link) — deliberately not a workspace
4. **S3 · Bounded Contexts** — space to ring the story, plus two axes: business differentiation (x) × model complexity (y)
5. **S4 · Visual Glossary (core context only)** — empty canvas + a legend note: `1 · 0..1 · 1..* · 0..25`
6. **S5 · Prototype** — link + screenshot
7. **Parking lot** — hotspots, disagreements, "we made this up" flags

Colour convention, written on frame 1 so nobody has to ask:
**yellow = actor · blue = activity · green = work object · pink = external system ·
red = hotspot, guess or contested sentence.**

### Sharing settings — test this in a private window

Set the board to **anyone with the link can edit**. Then open the link in an incognito
window and confirm you can actually place a sticky *without signing in*. Miro's guest-edit
behaviour varies by plan tier, and discovering it at 18:32 costs you Station 1.

Have the links ready as **QR codes on the table cards**, one per table. Typing a Miro URL
from a projector is a five-minute tax.

---

## Feeding the board to the skills

The skills read images. From Miro, **select the frame → Export → Image (PNG), 2x**. That
beats a screenshot, and it beats a phone photo by a mile.

Three things that make exports go wrong, all avoidable:

- **Export the frame, not the viewport.** A screenshot of a zoomed-out board loses the
  cardinality labels, which is exactly the information Station 4 exists to produce.
- **Zoom to fit before exporting** so no stickies are cropped at the edge.
- **Don't export the sticky-note toolbar or cursors** — other people's name badges sitting
  on top of a term get read as part of the term.

The prompts in the table card are unchanged; just attach the PNG export instead of a photo.
One addition worth making at Station 4, since the board makes it worth asking:

```
[attach frame export]

Use the visual-glossary-interpreter skill. This glossary accompanies the domain story
we froze earlier in this chat. Transcribe it and confirm the transcription with us before
deriving anything — this is a Miro export, so tell us if any edge label or cardinality
is ambiguous.
```

**The transcription confirmation still matters.** A clean export makes misreads rarer,
not impossible, and the failure is silent.

---

## What the facilitator has to watch for that paper tables don't have

| Symptom | Intervention |
|---|---|
| **One cursor moving, five people watching** | "Everyone place a sticky in the next 30 seconds." If it doesn't fix it, close the board and go to paper for that station. |
| **The table is tidying the board** | Alignment is not modelling. "Is it wrong, or is it just ugly?" |
| **People typing tiny stickies nobody can read** | Enforce a minimum font. If it needs zoom to read, it's not shared. |
| **Silence because everyone's reading the screen** | Same rule as the AI: *"Stop reading. What's wrong with it?"* |
| **Someone's device won't load the board** | Don't debug it. They pair with a neighbour. Move on. |
| **The board becomes the conversation** | Turn the screen off for two minutes and ask the table to say the domain story out loud. |

The pattern in all six: a screen makes a room quieter, and quiet is the thing you're
fighting all evening. Digital tables need **more** facilitator interruption than paper
tables, not less.

---

## Break and demos

**Gallery walk (20:00).** Miro tables put their board on the venue screen if there is one,
or turn a laptop outward at the table. Paper tables do it as before. Both work; don't make
the digital tables move.

**Demos (20:52).** Board tables have an advantage — they can screen-share a frame instantly.
Hold them to the same rule anyway: **two minutes, one screen, three sentences.** A Miro
board is not a demo.

---

## Afterwards

This is where the board earns its keep. Collect all table board links plus prototype links
and put them in the follow-up LinkedIn post and the Meetup event page. A monthly group that
can show what came out of the room recruits better than one that can't.

**Set the boards to view-only after the event** before sharing publicly, so the record
doesn't get edited into confusion.

---

## If you'd rather not

Nothing here is required. A room full of paper, markers and one laptop per table runs this
session fine — that's what the main script assumes. Miro buys you cleaner skill inputs and
a permanent record; it costs you a little energy and one more screen competing for
attention in a session that already has one. Decide per table, and let people switch back
mid-evening if it isn't working.