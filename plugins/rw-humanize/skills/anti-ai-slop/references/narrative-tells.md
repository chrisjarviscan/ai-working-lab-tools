# Layer 3: Narrative and Structural Tells (Patterns 13-20)

This is the layer most anti-AI writing advice misses, and it is the layer that
matters most as models improve.

## Why this layer exists

Surface tells (delve, tapestry, em dashes, the rule of three) are real, but they
are disappearing. Newer models are trained away from them, and a light editing
pass strips them out. In the StoryScope study (Russell et al., COLM 2026), the
authors took AI stories, used a span-level rewriting system (LAMP) to strip
cliche and purple prose, and then checked whether their detector still caught
them. A narrative-based detector barely budged: it still flagged the edited
stories at 93.9% macro-F1, down from 95.5% on the originals, a 1.6-point drop.
(This robustness test was run on one model's output, Gemini's.) The prose got
cleaner. The writing was still machine-made, and still detectable, because the
tell was never really in the words. A style-based detector is the thing that
would have collapsed under that edit; the narrative one did not, which is the
whole point.

The durable signature appears to live in narrative and structural choices: how
meaning is delivered, how tension is resolved, how the argument is ordered, how
the reader is treated. StoryScope showed these choices separate human from AI
writing at a 93.2% macro-F1 using no stylistic features at all. The authors frame
durability as a hypothesis rather than a settled fact, but their reasoning holds:
humanizing the surface is a find-and-replace job; humanizing the structure
requires rewriting the thing. Most people do the first and skip the second.

The study is about fiction. Chris writes thought leadership, memos, and
client narrative. The patterns below are the fiction findings translated into
nonfiction prose, with the original evidence kept so you can see the reasoning.
Do not apply the fiction literally. Apply the underlying tendency.

## The one-line version of every pattern

AI writing is over-determined, over-tidy, over-performed, and over-resolved. It
explains what it means, answers every question it raises, marches in a straight
line, colors every scene, keeps its moral judgments clean, and writes as if no
reader were present. Human writing trusts inference, leaves real tension open,
digresses, withholds, allows ambivalence, and talks to someone. Every pattern
here is a specific face of that difference.

## How to apply this layer without overcorrecting

These are tendencies to resist, not switches to flip. The failure mode of a
writer who takes this list too literally is as bad as slop: a memo with no
thesis, a buried lead, aimless digressions, a non-ending, and every judgment
hedged into mush. That is not human writing, it is unreadable writing.

Two guardrails hold at all times, and they outrank every pattern below:

- **Clarity and the reader's time win.** For a memo, an executive summary, a
  brief, or anything a busy person reads to make a decision, state your point
  early and plainly. Bottom-line-up-front is correct. Patterns 14, 15, and 16
  (unresolved tension, second threads, withheld disclosure) are about not making
  the whole piece mechanically tidy. They are not a license to hide your thesis
  or wander. When in doubt, be clear.
- **Take a real position.** Holding tension (14) and allowing ambivalence (18)
  mean refusing false certainty and cheap strawmen, not refusing to conclude.
  Thought leadership exists to say something. A piece that commits to nothing has
  overcorrected.

The narrative layer earns its keep most on longer, narrative-led pieces
(essays, long-form thought leadership) and least on short, decision-oriented
documents. Weight it accordingly. The source study measured roughly 5,000-word
stories, so treat the patterns as directional for short forms, not literal.

---

## Pattern 13: Thematic Over-Determination

**What it is.** The writer states the point the reader could have inferred, and
tags every fact, story, or example with the lesson it teaches. The takeaway is
never left to land on its own.

**Evidence.** This is the largest gap among the paper's 1-5 scale features. On
that scale of thematic explicitness and moralizing, AI averaged 3.94 against a
human 3.28, a 0.65 gap. AI narrators explicitly explained the story's theme 77% of the time versus
52% for humans. AI dialogue served philosophical debate 59% versus 34%. The
paper's summary: "AI spells out meaning rather than trusting the reader to infer
it."

**In nonfiction.** Every anecdote ends with "which shows that...". Every section
restates its own thesis. The reader is told what to conclude before they have
had the chance to conclude it.

**How to spot it.** After each concrete passage (a story, a number, a case),
look for a sentence that interprets it. Ask: would the reader have gotten the
point without this sentence? If yes, the interpretation is over-determination.

**Fix.** Give the fact or the story and cut the lesson. Trust the reader to do
the inference; that act of inference is what makes the point stick. Where the
meaning genuinely is not obvious, earn it with a second fact, not with a
label. Connects to surface Family A (significance inflation), Family B
(editorializing participle tails), and craft Pattern 10 (moralizing).

---

## Pattern 14: False Resolution / Over-Tidy Argument

**What it is.** Every tension the piece raises gets resolved. Every question
gets answered. The piece ties a bow. Nothing is left genuinely unsettled, even
when the honest state of the matter is unsettled.

**Evidence.** AI stories run tighter causal chains (4.20 vs 3.92 on continuity)
and resolve through the protagonist's own choices far more often (agency in
resolution: 69% AI vs 46% human). They resolve through internal understanding or
acceptance 47% of the time versus 27% for humans, who are "more comfortable with
ambiguous endings." The paper: "AI tells the same story from first clue to the
grand reveal."

**In nonfiction.** The essay that opens on a hard problem and closes having
solved it. The memo that surfaces a real tradeoff and then dissolves it. The
piece where the writer never admits they do not know.

**How to spot it.** Read the last paragraph of each section and the end of the
piece. Count how many end resolved. If a genuine tension you raised earlier is
now tidily closed, ask whether it is actually closed in reality or just closed
on the page.

**Fix.** Leave the real open question open. End on the unresolved tension when
that is the true state. This is the empirical backing for the Chris Jarvis Voice
rule "hold productive tension rather than resolving it neatly." An honest
non-ending reads more human than a satisfying false one.

---

## Pattern 15: Single-Track Linearity

**What it is.** One clean line from premise to conclusion. No genuine
digression, no competing thread, no complication that fails to resolve back into
the main argument.

**Evidence.** AI favors single-track narratives: 79% of AI stories had no
subplots versus 57% for humans, and humans integrated subplots into the main
theme at twice the rate (42% vs 21%). Human writing is "messier, with time jumps
and disjointed causal chains." The paper found AI draws from a narrower
narrative repertoire overall.

**In nonfiction.** Everything in the piece serves the thesis, tidily, in order.
There is no place where the writer follows a real tangent because it is true,
no counter-thread that complicates the main claim without defeating it.

**How to spot it.** Ask what the piece's second thread is. If there is exactly
one thread and every paragraph advances it in sequence, it is single-track.

**Fix.** Allow a real second thread: a complication, a counter-case, a
digression that earns its place because it is honest rather than because it is
on-message. The subplot should touch the main theme, not just decorate it.

---

## Pattern 16: Front-Loaded Disclosure / No Withholding

**What it is.** The thesis is stated upfront and then dutifully supported.
Nothing is withheld, nothing is revealed late, nothing is reordered for effect.
The reader always knows exactly where they are and where they are going.

**Evidence.** Every human-elevated temporal feature points here: humans use more
chronological discontinuity, more nonlinear framing for delayed disclosure, more
anachrony (flashbacks and flash-forwards), and deeper reinterpretation after a
surprise. AI "favors single-track narratives" told in order. Humans "use
nonlinear structure to delay key revelations."

**In nonfiction.** The classic AI shape: tell them what you'll tell them, tell
them, tell them what you told them. Predictable and inert.

**How to spot it.** Does the piece reveal anything the reader did not see coming
from the first paragraph? Is there a fact held back until it lands hardest? If
the structure is fully predictable by paragraph two, disclosure is front-loaded.

**Fix.** Consider opening in the middle of the tension instead of above it. Hold
one key fact until the moment it does the most work. Let the reader sit inside a
question before you answer it. You do not need a plot twist; you need one place
where the order of telling is a choice rather than a default.

---

## Pattern 17: Embodied and Sensory Over-Performance

**What it is.** Emotion rendered as physical symptom, scenes over-colored with
sensory detail, setting used to mirror inner states. "Show, don't tell" pushed
past the point of honesty into performance.

**Evidence.** The largest single categorical gap in the study: AI conveys
emotion through physical sensation and bodily metaphor 81% of the time versus 38%
for humans. AI uses more smell-based imagery (82% vs 57%), denser sensory
description, and setting-as-psychological-mirror more heavily. Humans name
feelings directly far more often (explicit emotion labels 29% vs 8%). The paper:
"Where a human author might write that a character felt afraid, AI renders fear
as a tightening chest, cold sweat, and dimming lamplight."

**In nonfiction.** Mostly relevant to narrative-led openings, which Chris uses.
The tell is the invented sensory scene: the "picture a Monday morning" opener
thick with coffee smell and fluorescent light, the manager whose frustration is
staged as a clenched jaw. It is atmosphere doing the work that a plain sentence
should do.

**How to spot it.** Look at scene-setting passages. Is the sensory detail
carrying real information, or is it coloring? Is an emotion being acted out with
the body when naming it would be cleaner and truer?

**Fix.** Sometimes just name the feeling. Cut sensory detail you invented rather
than observed. Let a scene be sparse. Anti-fabrication applies: do not
manufacture a vivid moment that did not happen to make a point land.

---

## Pattern 18: Moral Clarity / Flattened Ambivalence

**What it is.** Clean heroes and clean villains. The people the piece critiques
are strawmen; the ones it champions are spotless. Moral positioning is
unambiguous.

**Evidence.** Humans present morally ambivalent protagonists far more often:
moral polarity toward the protagonist was ambivalent or mixed in 59% of human
stories versus 38% for AI. AI frames protagonists' choices as more morally
clear-cut.

**In nonfiction.** The CSR manager who is simply doing it wrong. The
transactional program that has no redeeming logic. The transformative approach
that has no cost. Flattened ambivalence makes the argument weaker, not stronger,
because the reader knows the real world is mixed.

**How to spot it.** For each actor the piece judges, ask: is this person allowed
to be partly right? Is the thing being criticized allowed to have made sense at
the time? If every judgment is one-directional, ambivalence is flattened.

**Fix.** Let the person you critique be sympathetic and partly right. Let your
hero be compromised. This is the empirical backing for the Chris Jarvis Voice
rule "critique framing, timing, or scope, not intent or character," and for
craft Pattern 9 (empathy not sustained). The critique stays sharp; the target
gets their dignity.

---

## Pattern 19: The Absent Reader

**What it is.** The writing proceeds as if no one is reading it. It never
acknowledges the reader's actual situation, never treats them as a person with
stakes in the room.

**Evidence.** Humans break the fourth wall much more (fourth-wall permeability
67% vs 39%) and address the reader directly far more often (28% vs 7%). The
paper: "Human writing acknowledges its audience as a co-participant; AI writes as
though no one is watching."

**Critical nuance.** This does NOT license the metadiscursive directives the
surface layer bans in Pattern 3 ("consider this," "pay attention," "let that
sink in," "sit with this"). Those are the AI tell of commanding the reader's
cognition, and they stay banned. The human move is different: genuine
acknowledgment of the reader's position and stakes, not instructions on how to
think. "If you run a program like this, you already know the 4pm feeling when
the numbers are due and none of them tell you anything" is co-presence. "Consider
the implications of these numbers" is a cognitive command. One treats the reader
as a peer in the room; the other treats them as a student to be directed.

The bright-line rule when the two patterns feel like they are in conflict: if the
sentence tells the reader what to do with their attention or their mind (notice,
consider, sit with, imagine, pay attention), it is banned under Pattern 3,
whatever the framing. If it names the reader's real situation or stakes without
issuing an instruction, it is the co-presence Pattern 19 wants. When unsure,
default to cutting it; a piece can have too much reader address, and silence is
safer than a directive.

**How to spot it.** Ask whether the piece knows who is reading it. Does it ever
name their real situation, their constraint, the thing they are up against? Or
could it have been written into a void?

**Fix.** Acknowledge the reader's actual position. Name what they are dealing
with. Ask a real question you would ask them across a table. Keep it as
co-presence, never as a directive about how to process the text.

---

## Pattern 20: Convergence to Defaults (the meta-tell)

**What it is.** Not any one sentence. The predictability of every choice. At each
fork (how to open, how to order, how to end, which example to reach for, which
metaphor), the writer took the most obvious option. The piece is the statistical
center of what could have been written.

**Evidence.** This is the study's deepest finding. The five AI models cluster in
a tight, shared region of narrative space, well separated from human writing.
Human stories are rarer and more dispersed: their mean rarity percentile was 0.71
versus 0.49 for AI, and humans were overrepresented in the rarest tail (24.7% of
human stories fell in the rarest 10% corpus-wide, versus 7.1% of AI). AI
converges on defaults; humans spread out. Idiosyncrasy is the signature of a
human author.

**In nonfiction.** The piece that could have been generated by anyone from the
same prompt. The expected opening, the expected structure, the expected close,
the example everyone uses.

**How to spot it.** At each major choice, ask: is this the first thing anyone
would have done? If the opening is the obvious opening and the example is the
stock example and the ending is the expected ending, the piece has converged.

**Fix.** At each structural fork, notice the default and consider the second or
third option. Reach for the example that is true and specific to you rather than
the one everyone uses. The goal is not weirdness for its own sake; it is the
particular choice only this writer, with this experience, would make. This is
where Chris's real material (client stories, the science, lived constraints)
beats anything generic.

---

## The Claude Fingerprint Watch

Chris drafts with Claude, so Claude's specific tendencies are the ones most
likely to leak into his work. StoryScope profiled each model. Claude's
fingerprint, from their analysis ("Claude keeps it cool") and Table 17:

- **Flat event escalation.** Claude's stories escalate less than any other
  source; intensity stays even. In an argument, watch for a piece with no real
  spike, no moment that lands harder than the rest.
- **Reverent, not subversive.** Claude honors and extends conventions rather
  than challenging them (62% of Claude stories, versus 39-56% across other sources).
  Watch for writing that never breaks a form, never contradicts the expected
  frame, never surprises.
- **Quiet, tidy endings.** Claude favors calm, consistent, "epilogue" style
  closes and avoids the abrupt or explosive. Watch for the soft wrap-up that
  resolves the emotional temperature down to neutral (overlaps Pattern 14).
- **Uniform voice.** Claude's narrative voice is the most consistent of any
  model. Watch for tonal sameness from open to close, no roughness, no shift in
  register where the material would justify one.

When self-auditing a Claude draft, run this watch on top of Patterns 13-20. The
fix in every case is deliberate variation: let one moment escalate, break one
expected frame, let one ending stay rough, let the register shift where the
content earns it.
