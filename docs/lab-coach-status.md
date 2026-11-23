# Lab Coach prototype: status

## Current status (2026-11-23)

- **Goal:** for the 2027 AI Working Labs with nonprofit staff, each participant's own
  assistant acts as the instructor. People build first, on a real task from their job,
  and meet each concept only when it becomes relevant to that work. Group sessions are
  for sharing and problem solving, not breakout exercises.
- **Owner:** Chris Jarvis, RW Institute.
- **Done:** first draft of the skill (`plugins/lab-coach/skills/lab-coach/SKILL.md`),
  the concept map and build plan in its `references/` folder, a zip for claude.ai, a
  Claude Code plugin entry, and notes in `README.md`, `CLAUDE.md`, and `AGENTS.md`.
- **Not done:** nobody has run a coaching session with it yet. It is unverified.
- **Next action:** Chris tries it as a participant with a real task and notes where it
  lectures, where it takes over the work, and which concept triggers fire too early or
  never.

## Decisions

- Nothing is taught without salience. A concept is explained only when something in the
  person's own work gives them a reason to care, or when they ask.
- No Anthropic course content is copied here. The four-part build plan adapts the pilot
  plan described on the public outline page of the Claude Forward Deployed Engineer
  path. The reflection questions follow the ideas of the AI Fluency Framework. Wording
  and examples are RW Institute's own, with links to the free courses for going further.
- Developer topics from that path (the API, model choice, agent loops) are left out.

## Open questions

- Which Claude plans will participants be on, and can they connect GitHub or upload
  skills? This decides whether "sync the repo" works for everyone or some people need
  the zip.
- Do participants' organizations restrict connectors or what staff may paste into AI
  tools?
- How do lab notes travel between sessions: saved in a project, or pasted by hand?
- What does a participant bring to each group session, and how do facilitators see who
  is progressing?
- Does the coach hold back enough? It needs testing against a participant who says
  "just do it" every time, and one who wants everything explained up front.
- The lessons inside the Forward Deployed Engineer path have not been read, only the
  outline page. The Delivery Methodology course may hold more worth adapting.
