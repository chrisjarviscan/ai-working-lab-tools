# AI Working Lab Tools

Participants in RW Institute's AI Working Labs can use these tools to keep their AI
work honest. There are two of them. One catches writing that reads as machine-made.
The other stops the assistant from claiming it checked sources it never opened.

**Ask your AI about this repo.** If your Claude (or another assistant) is connected
to GitHub, point it here and ask things like:

- "What skills or plugins are available in this repo?"
- "What tools here can help me get rid of AI slop?"
- "What does each one do, and what's the catch?"

It will read this page and walk you through the list below.

---

## The tools

### 1. Anti-AI-Slop (skill: `anti-ai-slop`)

**What it is.** A writing checker that looks for the signs that a machine wrote
something, at three depths:

1. **Surface:** the giveaway words ("delve," "tapestry," "it's worth noting"),
   stock phrases, heavy formatting, and patterns like "It's not X, it's Y."
2. **Craft:** whether the piece works as writing. That means cold transitions,
   preachy endings, empathy that shows up once and vanishes, and a rhythm that
   reads choppy.
3. **Story and structure:** the deeper habits that survive a quick "make it sound
   human" edit, such as every tension resolving too neatly, the whole point being
   given away in the first paragraph, or no real reader in mind.

**What it does for you.** Two modes. When **drafting**, it shapes the writing
toward how people actually write instead of only stripping out bad words. When
**auditing**, it reviews a draft you already have and gives you a ranked list of
what to fix first, with the exact sentence quoted for each problem.

**Try saying:** "Audit this draft for AI slop." / "Does this read as AI?" /
"Rewrite this so it sounds like a person wrote it."

**Consequences and trade-offs**

- **It uses more of your AI allowance in Claude Code.** There, a full audit
  runs four reviewers: one for each layer, plus one that merges their findings.
  It's slower and uses more of your plan than a single pass. For a short email,
  ask for a quick check instead.
- **It can over-correct.** Pushed too hard, it can sand away phrasing that was
  actually yours. Read the suggested changes and decide for yourself; don't just
  accept the rewrite.
- **It does not check facts.** It tells you whether writing sounds machine-made,
  not whether it's true. A clean audit on a draft with a made-up statistic is
  still a draft with a made-up statistic.
- **Its strictest rules are one person's.** One file
  (`voice-chris-jarvis.md`) is Chris Jarvis's personal writing rules, including
  "no em dashes." It only switches on when you ask for his voice. Copy it, rename
  it, and rewrite it to describe how *you* write.
- **Passing is not a guarantee.** No checker can promise a reader or a detection
  tool won't flag your writing. This one makes the writing better; it doesn't
  certify it.

### 2. Source Accountability (skill: `source-accountability`)

**What it is.** A rule set that makes the assistant prove where it looked. Before
it reports findings, it has to show a short table: every source in scope, whether
it actually opened that source in this session (CHECKED or NOT CHECKED), and how.

**What it does for you.** It stops the most common quiet failure in AI research,
where the assistant says "I checked everywhere and found nothing" when it only
searched two of the three places you named. Any gap goes in the answer itself, not
a footnote. It also won't count a search from a previous conversation as current.

**Try saying:** "Check my Drive, email, and calendar for anything about the
spring gala." / "Cross-check this partner's details everywhere we keep them."

**Consequences and trade-offs**

- **Answers get longer and clunkier.** You'll see a table and statements like "I
  was not able to check X." That's the point: honest beats tidy.
- **It can't give the assistant access it doesn't have.** If your email isn't
  connected, the tool won't search it. It will tell you it couldn't. To get real
  coverage, connect the sources (Settings, then Connectors) first.
- **Set it up for your organization.** The skill ends with a "Make it yours"
  table. Replace the example rows with the places your organization actually keeps
  things, so "everywhere" means something specific.
- **It's for multi-source questions.** For a single quick lookup ("find that file
  in Drive") it stays out of the way.

---

## In testing: Lab Coach (prototype)

**This one is not finished.** It is a first draft for the 2027 labs and has not been
tried with participants yet.

**What it is.** A coaching skill that turns your assistant into the lab instructor. It
starts by asking what is on your plate this week, helps you build one small, useful
piece of it right away, and then looks at the result with you.

**What it does for you.** You learn by doing your own work. It explains an idea (a
skill, a connector, a project) only at the moment you run into a reason to want one, in
a sentence or two, and then gets back to the task.

**Try saying:** "Start my lab." / "Coach me." / "Pick up my lab" (then paste your lab
notes).

**Consequences and trade-offs**

- **It is untested.** Expect rough edges. Tell us what it got wrong.
- **It is slower than just asking for the work.** It hands decisions and judgment back
  to you on purpose. If you are out of time, say "just do it" and it will.
- **It may not remember your last session.** It gives you short lab notes at the end.
  Save them and paste them in next time.
- **Every person's assistant will coach a little differently.** The group sessions are
  where we compare notes and even that out.
- **It can't see what your organization allows.** Questions about connectors, plans, and
  what information you may share go to the group session.

**To try it on claude.ai:** download [`downloads/lab-coach.zip`](downloads/lab-coach.zip)
and upload it the same way as the two tools above. **In Claude Code:**
`/plugin install lab-coach@ai-working-lab-tools`.

---

## How to install

### Claude on the web or the desktop app (claude.ai)

1. Download [`downloads/anti-ai-slop.zip`](downloads/anti-ai-slop.zip) and
   [`downloads/source-accountability.zip`](downloads/source-accountability.zip).
2. In Claude, open Settings, then Capabilities (on some plans it's Customize,
   then Skills), and upload each zip. Leave them zipped.
3. Switch both on. Claude uses them when your request fits, or you can name one:
   "Use the anti-ai-slop skill on this."

### Claude Code

Run these two commands in Claude Code:

```
/plugin marketplace add chrisjarviscan/ai-working-lab-tools
/plugin install rw-humanize@ai-working-lab-tools
```

This gives you both skills plus the four reviewer agents that run the full
three-layer audit.

### Gemini, ChatGPT, or Copilot

The skills are plain text. Open `SKILL.md` in
[`plugins/rw-humanize/skills/anti-ai-slop/`](plugins/rw-humanize/skills/anti-ai-slop/)
or [`plugins/rw-humanize/skills/source-accountability/`](plugins/rw-humanize/skills/source-accountability/),
copy it, and paste it into a Gemini Gem, a ChatGPT Project's instructions, or a
Copilot agent's instructions. For Anti-AI-Slop, also add the four files in its
`references/` folder as knowledge files. The reviewer agents only run in Claude
Code.

---

## What's in this repo

| Path | What it is |
|------|------------|
| `plugins/rw-humanize/skills/anti-ai-slop/` | The writing checker and its four reference guides |
| `plugins/rw-humanize/skills/source-accountability/` | The source-checking rules |
| `plugins/rw-humanize/agents/` | Four reviewer agents for the full audit (Claude Code only) |
| `plugins/lab-coach/` | Prototype coaching skill, with its concept map and build plan |
| `docs/lab-coach-status.md` | Where the Lab Coach prototype stands and what is still open |
| `downloads/` | Ready-to-upload zips for claude.ai |
| `.claude-plugin/marketplace.json` | Lets Claude Code install the plugin from this repo |
| `CLAUDE.md`, `AGENTS.md` | Instructions an AI reads when you ask it about this repo |

Built by RW Institute for the AI Working Labs.
