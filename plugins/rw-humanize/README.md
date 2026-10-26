# rw-humanize

Plugin name: `rw-humanize`. Main skill: `anti-ai-slop` (shown in your skills list
as `rw-humanize:anti-ai-slop`).

A three-layer defense against AI slop in writing, plus a team of adversarial
audit agents. Consolidates three older RW skills (AI Syntax Avoidance, its craft
extension, and Chris Jarvis Voice) into one skill, and adds the durable
narrative-structure layer that older tools were missing.

## Install

In Claude Code:

```
/plugin install rw-humanize --marketplace chrisjarviscan/ai-working-lab-tools
```

## Why three layers

AI writing gives itself away at three depths:

1. **Surface** (vocabulary, syntax, formatting) is easy to catch and increasingly
   easy for models to shed. Necessary but not sufficient.
2. **Craft** (transitions, paragraph weight, tone, rhythm) is whether the piece
   works as writing.
3. **Narrative and structure** (how meaning is delivered, how tension is
   resolved, how the argument is ordered, how the reader is treated) is the
   durable signature. It survives a humanizing edit almost untouched.

The narrative layer is grounded in the StoryScope study (Russell et al., COLM
2026), which showed that narrative choices alone separate human from AI writing at
a 93.2% macro-F1 and barely move after stylistic editing. Most anti-AI advice only
reaches the surface. This plugin reaches all three, and weights the deepest one.

## What's in it

- **Skill: `anti-ai-slop`.** The consolidated super-skill. Two modes: drafting
  (shape human, slop-free writing) and auditing (adversarial review of an existing
  draft). Routes to four reference files and orchestrates the agent team.
- **References** (loaded on demand):
  - `surface-tells.md` (Layer 1: Patterns 1-4, vocabulary, formatting, Families A-G)
  - `craft-patterns.md` (Layer 2: Patterns 5-12)
  - `narrative-tells.md` (Layer 3: Patterns 13-20 plus the Claude fingerprint watch)
  - `voice-chris-jarvis.md` (the Chris Jarvis Voice contract)
- **Agents** (adversarial audit, run in fresh context):
  - `surface-tell-auditor`, `narrative-structure-auditor`, `voice-fidelity-auditor`
    run in parallel, one per layer.
  - `slop-audit-synthesizer` merges, dedupes, and ranks their findings into one
    prioritized report.

- **Skill: `source-accountability`.** Before the assistant says it "checked everywhere,"
  it has to list each source, mark it CHECKED or NOT CHECKED, and name how it checked.
  Gaps go in the finding itself, not a footnote.

## How to use it

- **Drafting or rewriting:** the skill triggers on writing, editing, humanizing,
  "sounds like AI," "make it more human," "Chris Jarvis voice," and similar. It
  shapes the writing toward the human signature, not just away from the tells.
- **Auditing a draft:** ask "does this read as AI?" or "audit this draft." The
  skill spawns the three auditors in parallel, then the synthesizer, and returns
  one ranked report.

## Pattern numbering

Patterns keep continuous numbers across the three layers so other RW tools can
reference them: surface 1-4, craft 5-12, narrative 13-20. Paragraph-level Families
A-G live in the surface layer.

## Replaces

This plugin is designed to replace the separate use of `ai-syntax-avoidance`,
`ai-syntax-avoidance-extended`, and `chris-jarvis-voice-v3`. It carries their full
content forward and adds the narrative layer they lacked.
