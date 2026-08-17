---
name: author-style-profile-mining
description: Mines a multi-sample writing corpus for an author's measurable, recurring stylistic habits (sentence rhythm, paragraph shape, transition words, syntactic moves, vocabulary register, hedging patterns) and converts the findings into a DO/DON'T checklist that future drafts can imitate or avoid. Invoke when a user wants to calibrate new writing to someone's demonstrated voice, build a style guide from sample documents, or separate an author's authentic quirks from generic/AI-sounding filler before an editing pass.
---

# Author Style Profile Mining

## What this produces

A single evidence-quoted document — an **author style profile** — that answers one question
only: *how does this person actually write, measurably, and how should that translate into
DO/DON'T rules for a future draft?* It never answers *what did they say* and never supplies
content, arguments, or facts for reuse. Style in, style rules out.

The output is useful for three distinct jobs, all served by the same procedure:

1. Calibrating an AI- or ghost-drafted document to sound like a specific person before it is
   published under their name.
2. Building a house style guide from a team's best existing writing.
3. Running a hedging/filler audit that removes AI-sounding padding *without* deleting a
   writer's genuine, deliberate uncertainty-marking along with it (see Phase 8 — this is a
   common failure mode of naive "de-AI-ify" passes and worth doing carefully).

## Non-negotiable guardrail — read this before starting

**This procedure calibrates voice, never content.** No sentence, argument, distinctive
example, or extended phrase from the source corpus may ever be transplanted — verbatim or
lightly paraphrased — into a future draft. The only text that may leave this procedure intact
is the small "representative passages" appendix (Phase 11), and even those exist solely as
voice exemplars, never as source material. If a drafting agent later wants to use an *idea* or
*fact* from a corpus sample, that is a separate sourcing/citation decision governed by
whatever citation rules apply in that context — never smuggled in through the style profile.
Restate this guardrail at the top and bottom of every profile you produce.

A second guardrail: do not report a finding as a "signature habit" unless it recurs across
**multiple, topically unrelated samples**. A pattern that shows up once, or only within one
topic/subject, is a topic artifact, not a style tic — say so explicitly rather than promoting
it.

## Inputs required

- A corpus of writing samples from a single author/voice — plain text, or a format you can
  reliably extract to plain text (PDF, DOCX, HTML, markdown, email export, chat log, etc.).
- **Minimum viable size:** at least 5 samples; 8–15 is comfortably enough for the frequency
  counts in Phases 4 and 8 to mean something. A profile built from 1–2 samples should be
  labeled low-confidence and should skip any claim about "consistent across the corpus."
- Optional: a description of the *target* document/context the profile will calibrate writing
  toward (audience, format, length constraints, house style rules already in force). This
  unlocks Phase 9 (genre-gap analysis) — skip that phase if there is no target context yet and
  the profile is purely descriptive.

## Procedure

Work through the phases in order. Each phase should produce a numbered section in the final
document with **measured evidence** (counts, ratios, short quoted fragments), not impressions.
Anything you assert without a count or a specific quoted instance to back it should be
flagged as a qualitative read, not presented as a measured finding.

### Phase 1 — Assemble and normalize the corpus

1. Convert every sample to plain text, preserving paragraph breaks. Note the extraction method
   used (so results are reproducible) and any known artifacts it introduces — PDF extraction in
   particular can bleed running headers/footers into body text, distort line-wrapped
   hyphenation, or mis-join lines across a page break.
2. Trim non-authorial boilerplate before counting anything: bibliographies/reference lists,
   email signatures and disclaimers, navigation chrome, license footers, page numbers. These
   sections are not the author's voice and will pollute every frequency count downstream.
3. Record, in a short **Method** note at the top of the profile: how many samples, how they
   were extracted, what sentence-segmentation approach was used (Phase 2), and any caveats
   discovered along the way (e.g., "the single longest measured sentence is partly a
   header-bleed artifact, not a real 400-word sentence"). State plainly that the profile is
   reproducible against these named inputs — this is what makes a finding checkable rather than
   asserted.

### Phase 2 — Sentence-length distribution and rhythm

1. Run a consistent sentence segmenter across the whole corpus (a regex-based splitter that
   protects common abbreviations/initials is adequate; a corpus-linguistics-grade parser is not
   required, but note the limitation).
2. Compute aggregate statistics: mean, median, standard deviation, min, max word-count per
   sentence, and total sentence count.
3. Bucket the distribution (e.g., 1–10, 11–20, 21–30, 31–40, 41–50, 51+ words) and report the
   percentage of sentences in each bucket.
4. Compute **per-sample** mean and median too, not just the aggregate — this is what lets you
   tell a corpus-wide habit apart from one outlier sample dragging the average.
5. **Read the distribution, don't just report it.** Specifically:
   - Is the mean well above the median in most/all samples? That is a right-skew fingerprint:
     a writer whose *default* sentence is one length, punctuated by a real minority of much
     longer cumulative sentences that carry the piece's real argumentative or narrative weight.
   - What do the short sentences (bottom bucket) actually *do*? Read a sample of them in
     context. Are they a sustained short-punchy register, or almost always a single declarative
     reset placed right after a long clause-stack? These read very differently and the profile
     should say which.
   - **Diagnose the mechanism of the long sentences, not just their length.** Long sentences
     built by chaining independent or near-independent clauses with commas (comma-splice
     accumulation) read as, and should be described as, a different habit than long sentences
     built by conventional subordinate-clause nesting. If the corpus shows the former, say so
     explicitly and flag it as a real stylistic habit to preserve, not a proofreading error to
     silently "fix" in a future draft.

### Phase 3 — Paragraph construction

Answer these with evidence (quoted paragraph openers/closers, rough word-count ranges), not
generic impressions:

- Do paragraphs track a fixed length, or an argumentative/narrative *unit* — ending when one
  sub-point/beat is fully done rather than at a word-count target? If length varies a lot by
  function (dense analytical paragraphs vs. short transitional ones), report the range for
  each function separately rather than one blended average.
- What does the **opening paragraph** of a section/chapter/piece typically do? Common patterns
  worth checking for: does it state a local question, preview the coming structure, and stake
  a position, all before any evidence appears? Does it do all three, every time, or only
  sometimes?
- Are sub-headers (if the form uses them) short noun phrases, or full sentences/summaries?
- How do paragraphs typically **close** — on a restated thesis, on the most specific piece of
  evidence just discussed, on a bridge to the next paragraph, or something else? Pull 2–3
  verified closing-sentence examples.

### Phase 4 — Transition and connector habits (measured)

1. Build a small marker table. Include both markers you notice the author leaning on and the
   generic "connective tissue" set that shows up by default in unedited or AI-assisted prose:
   "however," "furthermore," "moreover," "in conclusion," "additionally," "on the other hand,"
   plus whatever pivot word(s) you notice the author actually favoring.
2. For each marker, count total occurrences across the corpus **and** how many samples contain
   zero instances of it. The zero-count column matters as much as the total: a marker present
   in every sample is a real habit; a marker with a high total driven entirely by one outlier
   sample is not.
3. Do the same count-and-tabulate pass for punctuation devices that carry stylistic signal:
   semicolons, em dashes, colons introducing lists, parentheticals, ellipses.
4. **Report variance honestly.** If semicolon use ranges from 1 to 26 per sample, that range
   *is* part of the real signature — don't collapse it into one "average rate" and don't tell a
   future drafter to hit a fixed target number per page. Report what the device is *used for*
   (e.g., always yoking two balanced independent clauses, never as a list-separator) separately
   from how often it's used.
5. Explicitly call out any marker set that is a strong **negative** signal — present zero or
   near-zero times across the whole corpus. A near-total absence, measured across enough total
   words to rule out coincidence, is exactly as reportable a finding as a strong presence, and
   it is often the more useful one for an avoidance rule.

### Phase 5 — Evidence/quotation integration style

Applies to any corpus where outside material enters the prose: cited sources, quoted dialogue,
data points, examples, testimonials.

- How does outside material get introduced — named first and then quoted/cited, or
  paraphrased first and attributed after the fact?
- Is quoted material folded into the grammar of the author's own sentence by default, or
  block-set/colon-introduced by default? At what length (rough line/word count) does the
  author switch from folding-in to block-setting?
- What is the mechanical attribution convention — inline parenthetical, footnote/endnote, no
  attribution at all? Is it consistent across the corpus?
- Does the citation apparatus (if any, e.g. footnotes) double as a second, more informal
  authorial channel — asides, uncertainty admissions, acknowledgments — distinct from the main
  argument's voice? This matters a great deal for Phase 9 if the target document's citation
  format has no equivalent channel.

### Phase 6 — Characteristic syntactic and rhetorical moves

- **Openings.** How do pieces typically start, and how many sentences elapse before the
  author's own stance/thesis is directly stated? Pull 2–3 verified opening sequences.
- **Signature structural move.** Does one particular argumentative or narrative shape recur
  across multiple, topically unrelated samples — e.g., always carving a third position between
  two named poles, always a concede-then-pivot structure, always a problem-then-twist reveal?
  Verify it independently in at least three samples on genuinely different subject matter
  before calling it a real habit of mind rather than a topic artifact. Name the poles/beats
  generically when describing the pattern — do not restate the actual examples as reusable
  content.
- **How disagreement/counterargument is handled.** Is an opposing view or objection always
  named specifically and answered in the same paragraph/scene, or does the author sometimes
  gesture at it vaguely without engaging it? This is a binary worth measuring directly (count
  instances of each).
- **Person and address.** If first-person or direct address is used, count singular vs. plural
  (or first- vs. third-person) instances **per sample**, not just in aggregate — the
  interesting finding is often *whether a single rule holds across the whole corpus* or whether
  it's picked per-piece (or even switches mid-piece). Report the raw pattern; don't force a
  single rule onto it if the corpus doesn't have one.
- **Closings.** How do pieces end — a recap, a forward-looking gesture, a stated limitation, an
  aside, a cliffhanger? Is a bullet-style summary ever used, or avoided?
- **Rhetorical questions or direct-address devices.** If present, are they always resolved (the
  author answers their own question in the same or next sentence/beat), or sometimes left
  hanging as a flourish? This is directly measurable — check every instance.

### Phase 7 — Vocabulary register and recurring signatures

- What register of vocabulary shows up at **argumentative/emotional pivot points** specifically
  (the moments the author stakes something or turns a point), versus the plainer register used
  for ordinary connective/expository passages? Note the contrast, not just a word list.
- Is there a recurring **coin → gloss → abbreviate** pattern: a term or label is introduced,
  explained once, then reused in short form for the rest of the piece without re-explanation?
  If so, name it as a repeatable structural habit, not just a vocabulary note.
- Are technical, foreign-language, or jargon terms kept in their original form and glossed
  inline, or silently translated/simplified away? This is a real stylistic choice worth
  measuring.
- **Run an explicit AI-marker vocabulary scan.** Search the whole corpus for a standard filler
  set — words like *delve, leverage, landscape, tapestry, multifaceted, foster, cultivate,
  facilitate, utilize, comprehensive, holistic, robust (as filler), synergy, unlock, streamline,
  game-changer, cutting-edge* — and report presence or absence as a structural signal, not a
  curiosity. A handful of surface hits used in an ordinary, non-filler sense (e.g. "robust" as
  a literal adjective describing a physical object) do not count as a tic; say so if that's
  what you find, and don't let raw hit-count alone drive the conclusion. A genuine near-zero
  result across the full corpus is itself a strong, reportable finding: it means a future
  drafting pass should *not* introduce this vocabulary under the mistaken belief that it sounds
  more polished or more "professional" — for this author, it is specifically what their real
  writing avoids.

### Phase 8 — Hedging vs. throat-clearing

This phase deserves care because a blunt "remove all hedging" editing pass will strip out a
writer's authentic, deliberate uncertainty-marking along with generic AI-sounding padding —
the two need to be told apart, not conflated.

1. Find every instance in the corpus where the author marks uncertainty, narrows a claim, or
   states a limitation.
2. Classify each instance into one of two buckets:
   - **Genuine, author-specific hedging**: named and specific, tied to a stated reason,
     appearing at a real decision point (an unverifiable fact, a deliberately narrowed scope, a
     translation/interpretation choice). Often this *narrows what the claim covers* rather than
     *softening how confidently it's held* — e.g., swapping a strong universal claim for an
     explicitly weaker, bounded one, stated once and plainly.
   - **Generic throat-clearing / AI-pattern hedging**: phrases that could be inserted in front
     of almost any sentence without losing anything specific — "it is worth noting that," "it
     should be noted that," "one might argue that," "arguably," "to some extent," "in many
     ways," "somewhat," or vague both-sides gestures ("there are many perspectives on this").
3. Report **marker density** (roughly how many genuine-hedge instances per sample) and confirm
   whether they cluster at real decision points or scatter as a reflexive tic attached to
   ordinary declarative sentences. Report separately whether the generic throat-clearing bucket
   has *any* instances at all in the corpus — often it has none, which is itself the finding.
4. Turn this into a **practical rule**, not just a classification: when a future draft needs to
   mark a genuine limit, do it the way this author does — plainly, once, tied to a specific
   named reason, preferring scope-narrowing over confidence-softening. Do not pad ordinary
   declarative sentences with reflexive qualifiers just because "hedging" sounds appropriately
   cautious — if that register doesn't exist anywhere in the author's own writing, it isn't part
   of their voice and shouldn't be added in their name.

### Phase 9 — Genre-gap / transfer analysis (skip if there is no target document yet)

Every finding above was measured against the corpus's own genre, audience, length, and format.
Before turning findings into rules for a *different* target document, sort each finding into
one of three buckets and say why:

- **Transfers cleanly** — the feature doesn't depend on the corpus's original context in any
  way that the target lacks.
- **Transfers with modification** — state the modification precisely. (Common case: the
  corpus's citation/footnote apparatus carries a second authorial voice — asides, hedges,
  acknowledgments — that the target format has no equivalent channel for; state where that
  content should go instead, e.g. folded into the main prose or a different designated section.)
- **Does not transfer** — state why (audience breadth, length ceiling, single-vs-recurring
  authorship, format constraints) and what the target document should do *instead*. A common
  case: the corpus's extreme upper-quantile sentence length or heaviest device-density is
  sustainable for a narrow specialist audience reading closely, but would hurt readability for
  a broader or skimming audience — the rule for the target becomes "aim at the corpus's own
  *median* register, not its long tail."

This phase is what makes a profile usable instead of merely descriptive — it prevents a
future drafter from over-applying a feature outside the context that actually supports it.

### Phase 10 — Convert findings into a DO / DON'T checklist

Write two numbered lists. Every single line must trace back to a specific measured finding
from Phases 2–9 — reject any line that is really just a speculative impression ("the author
probably likes X") with no count or quoted instance behind it.

- **DO** lines must be specific and mechanically actionable — name the actual word, device, or
  structural move and when to use it. "Sound authoritative" is not a usable rule; "use word X
  as the default pivot when moving from a rejected position to your own — not word Y or word Z"
  is.
- **DON'T** lines must name the anti-pattern precisely enough that someone could grep for it
  (specific banned phrases, specific constructions) and should carry a one-clause reason so the
  rule isn't applied dogmatically out of context (e.g., don't strip *all* qualification in the
  name of de-hedging — only the throat-clearing kind identified in Phase 8).
- If Phase 9 was run, fold its transfer/no-transfer/modify verdicts directly into the relevant
  DO/DON'T lines rather than leaving them in a separate section a drafter might skip.

### Phase 11 — Representative passages appendix (optional, recommended)

Select 4–6 short passages — a single sentence or a short excerpt, each roughly under 40 words —
that each cleanly exemplify one specific rule from the DO/DON'T list. Label each with which
rule it illustrates and which sample it came from. State plainly, right above the list: **these
are voice exemplars only; see the guardrail** — none of this wording, or any argument/example
it carries, may be reused in future writing. If the corpus contains sensitive, private, or
identity-revealing material, either omit this appendix or paraphrase the *shape* of the passage
without quoting it directly.

### Phase 12 — Restate the guardrail

Close the document by restating the Phase-0 guardrail in the profile's own words: this document
calibrates voice, never content; nothing in it may be quoted, paraphrased-into, or otherwise
transplanted into future writing as material; any idea or fact from the corpus that a future
draft genuinely wants to use is a separate sourcing decision, never a silent pull from this
profile.

## Output structure

Use `references/output-template.md` in this skill as the section skeleton — its **Method** note
captures Phase 1, its ten numbered sections map to Phases 2–11 in order, and its closing
**Guardrail** restates Phase 12, all as ready-to-fill markdown headers. Keep every count and
every quoted fragment traceable to a specific sample so the profile stays
falsifiable/reproducible rather than asserted.

## Common failure modes to avoid

- **Reporting a single-sample quirk as a corpus-wide habit.** Always check the per-sample
  breakdown, not just the aggregate total, before calling something a "signature."
- **Turning a real variance into a fake fixed target.** If a device's usage rate genuinely
  ranges 1–26 across samples, don't average it into "use roughly 13 per document" — report the
  range and what drives it.
- **Treating length/register as free-floating "quality"** rather than something in service of
  a specific corpus's audience and format — always run Phase 9 before handing rules to a
  drafting context that differs from the corpus's own.
- **Conflating de-hedging with de-authenticating.** Removing every qualifier in the name of
  sounding less "AI" will also erase a writer's genuine, deliberate hedging — Phase 8 exists
  specifically to prevent this.
- **Smuggling content through the style profile.** The single most important discipline in this
  whole procedure: every excerpt you quote is there to show *how something is built*, never
  *what it says*. If you catch yourself wanting to reuse an example's actual claim or fact in
  future writing, stop — that requires separate sourcing, not a style-profile shortcut.
