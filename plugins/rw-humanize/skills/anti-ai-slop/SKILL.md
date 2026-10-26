---
name: anti-ai-slop
description: >
  Remove AI slop from writing across three layers: surface tells (vocabulary,
  syntax, formatting), craft flaws (structure, transitions, moralizing), and the
  durable narrative-structure signatures that survive stylistic editing
  (over-explaining, false resolution, single-track linearity, flattened
  ambivalence, the absent reader). Optionally enforces Chris Jarvis voice. Use
  this skill whenever writing, drafting, rewriting, editing, humanizing, or
  auditing any prose: thought leadership, blog posts, articles, LinkedIn posts,
  emails, memos, reports, client narrative, presentations, or social copy. Also
  trigger on "sounds like AI," "AI slop," "too robotic," "make it more human,"
  "humanize this," "de-slop," "AI tells," "write like a human," "fix the
  cadence," "does this read as AI," "audit this draft," "Chris Jarvis voice,"
  "CJ voice," "delve," or "em dashes." This is the primary anti-slop skill and
  should be preferred over ad hoc editing whenever slop, voice, or humanness is
  in question.
---

# Anti-AI-Slop

## What this skill does

AI writing gives itself away at three depths, and most editing only reaches the
shallowest one.

1. **Surface** (Patterns 1-4, vocabulary, formatting): the words and punctuation.
   Easy to catch, and increasingly easy for models to shed. Necessary, never
   sufficient.
2. **Craft** (Patterns 5-12): whether the piece works as writing. Transitions,
   paragraph weight, protagonist, tone, rhythm.
3. **Narrative and structure** (Patterns 13-20): how meaning is delivered, how
   tension is resolved, how the argument is ordered, how the reader is treated.
   This is the durable signature. It survives a humanizing edit almost untouched,
   which is exactly why it is the layer that separates human from AI writing as
   models improve.

The three layers are grounded in RW's original AI Syntax Avoidance work, its
craft extension, and the StoryScope study (Russell et al., COLM 2026), which
showed that narrative choices alone separate human from AI writing at 93% and
barely move after stylistic editing. A separate voice layer enforces Chris Jarvis
voice when the author is Chris.

This skill has two modes. Read the mode you are in.

## Mode A: Drafting or rewriting (shape the writing)

Use when producing new prose or rewriting a draft into human, slop-free writing.

1. **Load the layers you need.** Always read `references/narrative-tells.md`: it
   is the layer most easily forgotten and the one that matters most. Read
   `references/surface-tells.md` for the vocabulary and formatting rules. If the
   piece is Chris's own voice, read `references/voice-chris-jarvis.md` and let it
   govern tone; it takes precedence over general style preferences.
2. **Write toward the human signature, not just away from the tells.** Removing
   banned words is table stakes. The real work is structural: leave a genuine
   tension unresolved (Pattern 14), allow a real digression (Pattern 15), hold
   back one fact for effect (Pattern 16), let the people you critique be partly
   right (Pattern 18), acknowledge the actual reader (Pattern 19), and at each
   structural fork take a choice that is specifically yours rather than the
   obvious default (Pattern 20).
3. **Watch the Claude fingerprint.** Because these drafts are written with Claude,
   they drift toward flat escalation, reverent framing, tidy quiet endings, and
   uniform voice. The fingerprint watch at the end of `narrative-tells.md` is the
   antidote: let one moment escalate, break one expected frame, let one ending
   stay rough.
4. **Self-audit before delivering.** Run the validation checklist below. Rewrite
   anything over threshold, then re-scan changed passages, since a rewrite can
   introduce new tells.

You do not need to spawn agents for routine drafting. The agent team is for
adversarial audit of an existing draft, especially one you did not write, or when
the user explicitly wants a thorough review.

## Mode B: Auditing an existing draft (adversarial review)

Use when the user hands you a draft and asks whether it reads as AI, wants it
de-slopped, or wants a thorough review. Adversarial audit works best in fresh
context, so this mode spawns a team of specialist agents rather than scanning in
the main thread.

Run the three auditors in parallel, in a single turn, each pointed at the draft
and its layer's reference file:

- **surface-tell-auditor** (Layer 1): reads `references/surface-tells.md`, reports
  vocabulary, syntax (Patterns 1-4), formatting, and Family A-G hits with quoted
  strings.
- **narrative-structure-auditor** (Layer 3): reads `references/narrative-tells.md`,
  reports Patterns 13-20 and the Claude fingerprint with named locations. This is
  the layer that catches durable slop; weight it accordingly.
- **voice-fidelity-auditor** (Layer 2 + voice): reads `references/craft-patterns.md`
  and, when the author is Chris, `references/voice-chris-jarvis.md`; reports
  craft Patterns 5-12, anti-fabrication risks, and voice breaks.

Then pass all three reports to the **slop-audit-synthesizer** agent (or synthesize
inline if the user wants speed over a clean handoff). The synthesizer dedupes
overlapping findings, resolves the deliberate tension between Pattern 3 (ban
metadiscursive directives) and Pattern 19 (want genuine reader co-presence),
ranks findings by durability and severity, and returns one prioritized report.

Deliver the synthesized report. If the user wants a rewrite too, do the rewrite
in the main thread using Mode A, then re-audit the changed passages.

Agent files live in the plugin's `agents/` directory. In environments without
subagents, fall back to running each layer's reference file yourself in sequence
(narrative first, since it is the deepest), then synthesize.

## Which layer for which situation

- Fast pre-send check on a short email: surface layer only.
- "Does this read as AI?": all three layers, Mode B, weight narrative.
- "Make this sound like me": voice layer governs, all layers enforce, Mode A.
- Long-form thought leadership: all layers, and expect the real problems to be in
  the narrative layer, not the vocabulary.

## The underlying principle

Almost every tell in every layer is one root failure: the writer performs
emphasis, significance, resolution, or analysis instead of earning it. The
surface layer performs it with words. The craft layer performs it with structure.
The narrative layer performs it with the shape of the whole argument: tying every
bow, answering every question, marching in a straight line, keeping every moral
clean. The fix is always the same, and it is the same fix at every depth: trust
the content, trust the reader, name your sources, hold real tension, and make the
particular choice only you would make.

## Output validation checklist

Surface: no banned vocabulary or stock phrases in filler use; no Pattern 1-4
constructions; Family A-G within thresholds; em dashes zero in CJ/RW/RWI voice;
no formatting or chatbot artifacts.

Craft: every paragraph seam has a bridge (5); load-bearing ideas have room (6);
claims have a "what it looks like in practice" beat (7); one protagonist, held
(8); empathy sustained (9); consequence not obligation (10); at most one closing
thump (11) and one contrastive negation (12).

Narrative: nothing over-explained that the reader could infer (13); at least one
genuine tension left honestly open (14); not a single clean track if the subject
is actually complex (15); some real choice in what is disclosed when (16); no
invented sensory or emotional performance (17); the people critiqued are allowed
to be partly right (18); the reader is acknowledged as present, without cognitive
commands (19); the structural choices are specifically the author's, not the
defaults (20); Claude fingerprint checked if drafted with Claude.

Voice (when Chris is the author): no fabrication; no em dashes; lived-in not
optimized; holds tension; does not instruct the reader; science clarifies not
decorates; constraints named.

If any check fails, rewrite before output. When auditing rather than producing,
report each failure with the quoted text and its pattern number.
