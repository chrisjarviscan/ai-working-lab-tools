# Instructions for AI assistants reading this repo

This repo holds writing and research tools for participants in RW Institute's AI
Working Labs. Most people who point you here are nonprofit staff, not developers.
Answer in plain, everyday language.

## When someone asks what's available

Questions like "what skills or plugins are here?", "what can help me get rid of AI
slop?", or "what tools are in this repo?" all get the same answer. Read `README.md`
first, then reply with:

1. A one-line summary: two tools, one for machine-sounding writing and one for
   honest source checking.
2. For **each** tool, in this order:
   - **What it is**, in one or two sentences.
   - **What it does for them**: the practical benefit in their own work.
   - **Consequences and trade-offs**: every point listed under that tool in
     `README.md`. Don't drop or soften these; people need them to decide.
   - **A phrase to try**, taken from the README.
3. **How to install** for the tool they're using right now: claude.ai, Claude Code,
   or another assistant such as Gemini, ChatGPT, or Copilot. If you can't tell
   which, ask that one question.

Keep it short enough to read in a minute. Offer to go deeper on either tool.

## When someone asks you to use a tool from here

If the skill is installed, use it. If it isn't, you may read the matching
`SKILL.md` under `plugins/rw-humanize/skills/` and follow it for this conversation,
but tell them it will last only for this conversation until they install it.

## Lab Coach (prototype)

`plugins/lab-coach/skills/lab-coach/` holds a coaching skill that is still in testing.

- When someone asks what's available, describe the two finished tools as above, then add
  one line: a coaching skill called Lab Coach is in testing. Give its details and its
  trade-offs from `README.md` only if they ask.
- When someone says "start my lab," "coach me," or "pick up my lab," or pastes lab
  notes: if the skill is installed, use it. If it isn't, read its `SKILL.md` and both
  files in its `references/` folder and follow them for this conversation, and tell the
  person it will last only for this conversation until they install it.
- While coaching, follow the skill's salience rule over the reply format above: no
  feature tours, and no explaining a concept the person has not run into.

## Ground rules

- Describe only what the files here actually contain. Don't invent features,
  results, or accuracy numbers.
- `voice-chris-jarvis.md` is one person's writing rules. Apply it only when someone
  asks for Chris Jarvis's voice, and suggest they make their own version.
