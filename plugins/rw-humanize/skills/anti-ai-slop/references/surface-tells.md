# Layer 1: Surface Tells (Patterns 1-4, Vocabulary, Formatting)

The fast layer. These are string-level and sentence-level habits that mark text
as machine-made. They are the easiest tells to catch and, increasingly, the
easiest for models to shed, so catching them is necessary but never sufficient.
Run this layer first because it is cheap; then run the deeper layers, which is
where durable slop lives.

Numbering note: Patterns 1-4 keep their historical numbers because other RW
tools reference them. Craft patterns are 5-12 (see craft-patterns.md), narrative
patterns are 13-20 (see narrative-tells.md).

## Tier 1: Banned Vocabulary and Stock Phrases

Zero tolerance in figurative or filler use. These are statistically
overrepresented in AI output and now function as tells. Where tooling allows,
grep for them rather than eyeballing.

### Words (figurative/filler use)

| Banned | Use instead |
|---|---|
| delve, delve into | look at, examine, dig into, or just start saying the thing |
| tapestry, rich tapestry | name the actual elements |
| vibrant | specific detail about what makes it lively |
| pivotal | important, decisive, or cut it |
| testament (as in "a testament to") | show the evidence instead of labeling it |
| underscore(s/d/ing) | show why it matters, or "this shows" |
| showcase, showcasing | show, display, or name what is shown |
| foster(s/ing) | build, create, support, or name the mechanism |
| highlighting (as editorial tail) | cut, or state the point as its own sentence |
| emphasizing (as editorial tail) | cut, or state the point as its own sentence |
| leverage (verb) | use |
| robust | specific: tested, redundant, well-staffed, whatever it actually is |
| seamless(ly) | describe the actual handoff |
| landscape (figurative: "the CSR landscape") | field, market, or name the actual actors |
| journey (figurative: "their giving journey") | name the actual sequence of events |
| realm | field, area, or cut |
| boasts (meaning "has") | has |
| nestled | located, sits, or just the location |
| profound | specific about the size or nature of the effect |
| intricate, intricacies | detailed, complicated, or name the parts |
| crucial / vital role ("plays a crucial role in") | say what it actually does |
| ever-evolving, rapidly changing | cut, or name the specific change |
| game-changer, transformative (as hype) | state the specific before/after difference |
| elevate (figurative) | improve, raise, or the specific action |
| embark (figurative) | start, begin |
| navigate (figurative: "navigating challenges") | handle, work through, or name the challenge |

### Stock phrases and transitions

| Banned | Fix |
|---|---|
| "In today's fast-paced world / rapidly changing landscape" | Delete. Start with the subject. |
| "In the heart of" | Give the location plainly. |
| "It's important to note that" | Delete the frame; keep the note. |
| "It's worth mentioning that" | Delete the frame; keep the mention. |
| "Additionally," / "Moreover," / "Furthermore," as paragraph openers | Connect with logic, not a stacking word. Often deletable. |
| "In conclusion," / "In summary," / "Overall," | Delete. End on substance. |
| "At the end of the day" | Delete or state the actual bottom line. |
| "a significant milestone," "marks a pivotal moment" | State what happened; let the reader judge scale. |
| "stands as," "serves as," "functions as," "represents" when the meaning is "is" | Use "is." |

A banned word used literally and correctly ("the surgeon made an intricate
incision," "the app's robust error handling was tested against...") is fine; the
ban targets figurative filler. When in doubt, replace.

## Tier 2: The Four Core Syntax Patterns

Zero tolerance.

### Pattern 1: Presentative Construction with Evaluative Assertion

Announcing that something is important instead of letting content demonstrate it.
Opens with "Here is," "This is," "There is," a copula, a definite noun phrase,
and an evaluative clause telling the reader how to feel.

Do not produce: "Here is the part that should matter to anyone running a
corporate social impact program." / "This is the finding that should keep
program directors up at night."

Fix: delete the announcer clause; start with the substance. "Here is the part
that should matter to program directors" becomes "Program directors have a
design problem on their hands."

### Pattern 2: Anaphoric Fragment Stacking

A run of sentence fragments each opening with the same word, separated by
periods. Oratory borrowed into prose, where it reads as performance.

Do not produce: "For logistics. For participation counts. For photo ops." /
"Not the exception. Not the outlier. The norm."

Fix: fold into one sentence with commas, semicolons, or subordination.

### Pattern 3: Metadiscursive Directives

Instructing the reader on how to process the content: pay attention, sit with
it, notice, consider, let it sink in. Patronizing in written prose.

Do not produce: "Sit with those numbers for a moment." / "Consider the
implications." / "Let that sink in."

Fix: delete the directive. If emphasis is needed, restructure so the point lands
in a strong position (end of paragraph, short sentence after a long one). Trust
the reader. (Note: this is distinct from genuine reader co-presence, which
narrative Pattern 19 actively wants. The line is command versus acknowledgment.)

### Pattern 4: Staccato Parallel Fragments

A burst of very short sentences with identical structure fired in sequence.
Mechanical and rhythmically flat.

Do not produce: "Same information. Same beneficiary. Same story." / "No face. No
voice. No reciprocity."

Fix: combine into one sentence with connective tissue, and vary structure so no
two consecutive sentences share a skeleton.

## Tier 4: Formatting and Artifact Tells

### Punctuation and emphasis

- **Em dashes:** zero in Chris Jarvis, RW, or RWI voiced output (standing voice
  rule). In voice-agnostic prose, at most one per ~500 words; chains are a tell.
  Replace with commas, periods, colons, or parentheses.
- **Boldface for emphasis:** bold is for structure (defined terms at first use,
  reference labels), not for stressing words mid-sentence.
- **Quotation marks:** keep straight or curly consistent; a mid-document switch
  signals pasted-in generated text.

### Lists and headings

- **Bold-header bullet syndrome:** stacks of "**Label:** explanation" bullets.
  One in a reference doc is fine; prose deliverables that keep collapsing into
  these were generated, not written. Convert to connected prose.
- **List inflation:** bullets where the content is an argument with logical
  connections ("because," "despite," "which led to"). Write sentences.
- **Heading case mismatches** and **heading-level skips** (H2 then H4), plus
  decorative horizontal rules before headings: match convention, fix hierarchy,
  drop rules.
- **Emoji as bullets or section markers** (the decorative kind): remove unless
  house style calls for them.

### Chatbot and pipeline artifacts

Zero tolerance; direct evidence of unedited AI output. Search for:

- Conversational residue: "I hope this helps," "Certainly!", "Great question,"
  "Would you like me to," "Let me know if"
- Self-reference: "As an AI," "As a language model," knowledge-cutoff disclaimers
- Refusal fragments: "I can't create content that..."
- Placeholder text: "[Insert name]," "[Company]," unresolved template variables
- Citation-pipeline debris: turn0search0, oaicite, contentReference, [cite: 1]
- Tracking parameters in pasted links: utm_source=, utm_medium= (strip them)
- Abrupt mid-sentence cut-offs at the end of a section

## Structural pattern families (paragraph-level, from the original base skill)

These sit between surface and craft. Scan per paragraph.

- **Family A: Significance inflation.** Generic claims of importance or legacy
  with no evidence ("marks a significant shift," "left an indelible mark"). State
  the concrete fact; show evidence if significance is real, else cut.
- **Family B: Editorializing participle tails.** A fact with an interpreting
  participle bolted on ("..., underscoring the need for reform," "..., fostering
  a culture of trust"). Cut the tail; if the interpretation matters, give it its
  own sentence with an owner.
- **Family C: Negative parallelism.** "Not X, but Y" and variants. Max one per
  piece, never as the final line. (Piece-level count agrees with craft Pattern
  12.)
- **Family D: Rule-of-three saturation.** Triads everywhere. Max two per ~500
  words, never consecutive.
- **Family E: Vague attribution.** "Experts argue," "studies show," with nothing
  named. Name the source, own the claim, or cut it.
- **Family F: Copula avoidance and elegant variation.** "Serves as," "stands as"
  where the meaning is "is"; and cycling synonyms for one thing. Use "is"; repeat
  the right word.
- **Family G: Formulaic wrap-ups.** Challenges-then-optimism endings, section
  recaps, universal-significance closes. End on the strongest concrete point.

## Thresholds

| Item | Threshold |
|---|---|
| Tier 1 vocabulary and stock phrases | 0 (figurative/filler use) |
| Patterns 1-4 | 0 |
| Family A significance inflation | 0 without attached evidence |
| Family B participle tails | 0 |
| Family C negative parallelism | max 1 per piece, never final line |
| Family D rule of three | max 2 per ~500 words, never consecutive |
| Family E vague attribution | 0 |
| Family F copula avoidance | 0 for dodges |
| Family G formulaic wrap-ups | 0 |
| Em dashes | 0 in CJ/RW/RWI voice; max 1 per ~500 words elsewhere |
| Bold-for-emphasis, emoji bullets, artifacts | 0 |
