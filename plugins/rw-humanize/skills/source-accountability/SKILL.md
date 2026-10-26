---
name: source-accountability
description: >
  Enforce rigorous source verification when reporting findings across multiple locations
  or services. Use this skill for multi-source research tasks, cross-platform audits, file-finding
  missions that span more than one service, or any task where the user names specific places to look
  and expects confirmation that each was actually checked. Trigger phrases include "check everywhere
  for," "search across my Drive and Outlook," "audit all our folders," "is there anything in
  [multiple locations]," "verify across," "cross-check," "look through all my [services]," or any
  request that implies comprehensive coverage across platforms (Google Drive, Outlook, SharePoint,
  Slack, Dropbox, etc.). Do NOT trigger for single-source lookups like "find that file in Drive" or
  "search my email for X" -- those are routine tool use, not multi-source verification tasks. The
  purpose of this skill is to prevent the assistant from claiming to have checked sources it did not
  actually access.
---

# Source Accountability

## Why This Skill Exists

Trust breaks when someone says "I checked everywhere" but actually only checked two out
of three places. It doesn't matter whether the missing source would have changed the
conclusion. The problem is the false claim of verification. Once that happens, every
future "I checked" becomes suspect.

This skill exists because the assistant is prone to a specific failure mode: when summarizing
findings, it rolls unchecked sources into "all clear" statements because the conclusion
feels tidier. This isn't confusion about what tools are available -- it's a writing
discipline problem where the assistant prioritizes narrative flow over accuracy. The fix is
structural: force an explicit audit trail before any conclusion is delivered.

## Core Rules

### 1. The Access Ledger

Before delivering any finding, conclusion, or "I checked" statement, produce an explicit
access ledger. This is not optional. The ledger has three columns:

| Source | Status | Method |
|--------|--------|--------|
| iCloud (mounted folder) | CHECKED | File system browse via `ls` and `find` |
| Google Drive | CHECKED | API connector search for "[query]" |
| Dropbox | NOT CHECKED | No connector available, not mounted |
| Outlook email | NOT CHECKED | Not searched this session |

**Status values are binary:** CHECKED or NOT CHECKED. There is no "partially checked"
or "likely fine." You either accessed it with a tool in this session, or you didn't.

**Method must name the actual tool or action used.** "File system browse via `ls`,"
"Google Drive API search for [query]," "Grep for [pattern] in /path." Not "reviewed" or
"verified" — those are conclusions, not methods.

### 2. The Claim Boundary Rule

Never include a source in a verified/checked/confirmed statement unless the access ledger
shows it as CHECKED with a specific method. This applies to:

- "I didn't find any X" — only valid for sources you actually searched
- "Your files are organized correctly" — only valid for locations you actually inspected
- "There's nothing in [location]" — only valid if you accessed that location this session
- "Everything looks good" — only valid if you checked everything in scope

If the user mentioned a source (e.g., "check Dropbox too") and you couldn't access it,
the conclusion MUST be marked incomplete. Not in a footnote. Not as an afterthought.
In the finding itself.

### 3. The Gap Declaration

When a source was mentioned or implied but not checked, say so in the body of the finding,
not buried at the end. The pattern:

"I checked [X] and [Y]. I was NOT able to check [Z] because [reason].
My conclusion covers only [X] and [Y]."

This feels clunky. That's the point. The discomfort of writing it is what prevents the
lazy summary that rolls everything together.

### 4. Scope Before Search

Before starting any multi-source research or audit task, state the scope explicitly:

- What sources are in scope based on what the user asked?
- Which ones can you actually access right now?
- Which ones can't you access, and what would be needed?

This prevents the problem at the start rather than catching it at the end. The user can
then decide whether to proceed with limited access or fix the gap first.

### 5. No Inherited Verification

Results from a previous session or conversation do not count as "checked" in the current
task. Each session starts fresh. If the user says "you already looked at my Google Drive
last time," the honest answer is that you'd need to search again to make current claims.

## When This Skill Fires

Any task where the assistant is reporting on what it found (or didn't find) across one or more
sources. Common triggers include: "Can you check if..." / "Look through my..." /
"Search for..." / "Is there anything in..." / "Do I have any..." plus file audits,
organization assessments, research across multiple services, competitive research, and
any task where the user names specific places to look.

## Applying the Ledger

For quick single-source tasks, the ledger can be inline: "I searched your Google Drive
for [query] and found nothing. Note: this only covers Google Drive — I don't have access
to your Dropbox or local files this session."

For multi-source tasks, use the full table format.

For ongoing work within a session, maintain a running ledger and update it as new sources
are accessed. When delivering a final summary, include the complete ledger.

## Recovery

If you catch yourself about to write a summary that includes an unchecked source — stop.
Rewrite with the gap declared. Better to deliver an honest incomplete finding than a
confident false one.

If the user catches this error, own it plainly: state what you actually checked, what you
didn't, and correct the record. Don't explain why you made the mistake. Just fix it.

---


## Make It Yours: Your Source Map

The ledger works best when the assistant knows which places count as "everywhere" for
your organization. Replace the example rows below with your own and keep the table here.

| Source | Access Method | What It Contains |
|--------|--------------|-----------------|
| Shared drive (e.g. Google Drive, SharePoint, Dropbox) | Connector or mounted folder | Program documents, grant files, reports |
| Email | Email connector | Partner and funder correspondence |
| Calendar | Calendar connector | Meetings and past events |
| Meeting notes or transcripts | Notes tool or connector | Decisions and action items |
| Downloads folder | File system | Recent, unsorted files |

**When claiming "checked everywhere":** the access ledger must show CHECKED for every row
in your table. If a source isn't reachable this session, say so in the conclusion itself.
