# Author Style Profile — "Backyard Beds" (SYNTHETIC EXAMPLE)

> **This entire document is a worked example built from fabricated demonstration text.**
> "Backyard Beds" is not a real blog, and the three samples in `synthetic-corpus/` were written
> for this skill to illustrate the procedure end to end. All numbers below were computed from
> those three files and are reproducible by re-running the same counts against them.
>
> **Toy-corpus caveat:** three samples is well below the 8–15 this skill recommends for
> production use (see SKILL.md, "Inputs required"). This example keeps the corpus tiny so the
> whole worked profile fits in one file — treat every "pattern" below as illustrative of the
> *method*, not as a statistically solid finding at this sample size.

**Purpose:** demonstrate the author-style-profile-mining procedure on a small, fully synthetic
corpus, showing what measured output looks like at each phase.

**Scope:** style only. Nothing in the three synthetic sample files is real content to protect —
they're intentionally throwaway — but the profile still follows the same content/voice
separation a real profile requires.

**Method.** 3 plain-text samples (`sample-1-soil.txt`, `sample-2-blight.txt`,
`sample-3-watering.txt`), ~250–270 words each, 780 words / 28 sentences total. Sentence
segmentation: naive split on `.`/`!`/`?` followed by whitespace + a capital letter (semicolons
treated as internal punctuation, not sentence boundaries — this is why several sentences below
run well past 50 words). Bracketed synthetic-label header lines were excluded from all counts.

---

## 1. Sentence-Length Distribution and Rhythm (measured)

**Aggregate, all 3 samples, 28 sentences:**

| Statistic | Value |
|---|---|
| Mean | 26.8 words/sentence |
| Median | 17.5 words/sentence |
| Min | 1 |
| Max | 86 |

**Distribution (word-count buckets, n=28):**

| Length | Count | % |
|---|---|---|
| 1–10 | 9 | 32.1% |
| 11–20 | 6 | 21.4% |
| 21–30 | 3 | 10.7% |
| 31–40 | 3 | 10.7% |
| 41–50 | 1 | 3.6% |
| 51+ | 6 | 21.4% |

**Per-sample mean/median:**

| Sample | n sentences | Mean | Median |
|---|---|---|---|
| sample-1-soil | 10 | 24.1 | 15.0 |
| sample-2-blight | 9 | 28.6 | 27.0 |
| sample-3-watering | 9 | 28.0 | 15.0 |

**Reading of the distribution.** Mean sits above median in all three samples and in aggregate —
right-skewed, consistent with a writer whose typical sentence is short-to-medium, punctuated by
a real minority (21.4% here) of much longer sentences. The short end (1–10 words, 32.1%) is
worth reading in context before calling it a "punchy" register: in this toy corpus, all nine of
those short sentences land immediately after one of the long comma-chained sentences ("It
didn't help." after a 58-word sentence in sample-1; "Don't." after a 66-word sentence in
sample-2) — a reset-after-long-clause-stack pattern, not a sustained short-sentence style.
**Mechanism of the long sentences:** comma-linked accumulation of near-independent clauses
("...and the beds mostly survived, which I took as proof the number was right; survival and
health are not the same measurement, though, and I only learned that when a hot week pushed the
schedule..."), not conventional subordinate nesting — a genuine habit to preserve, not a
run-on to silently fix.

---

## 2. Paragraph Construction

- Paragraphs track an argumentative beat, not a fixed length: the closing paragraph of each
  sample runs 1–3 short sentences (a landing/turn), while the opening paragraph runs long and
  dense (the setup-and-reveal).
- **The opening paragraph does two things every time**: (1) states what the author used to
  believe/do, (2) pivots — via the "Turns out" marker, see §3 — to what turned out to be true.
  All three samples follow this shape exactly.
- Sub-headers are short, wry noun phrases, not full-sentence summaries: "Compaction, Not
  Drought," "The Blight Wasn't the Blight," "A Schedule Isn't the Same as Enough."
- Paragraphs never close on a restated thesis; they close on a short declarative landing line
  ("Roots do the rest." / "Don't." / "It just isn't the last one.").

---

## 3. Transition and Connector Habits (measured)

| Marker | Total across 3 samples | Samples with 0 |
|---|---|---|
| "Turns out" | 3 | 0 of 3 |
| Semicolons | 7 | 0 of 3 (range 2–3) |
| Em dashes | 0 | — (none used) |
| "However" / "Furthermore" / "Moreover" / "In conclusion" / "Additionally" (combined) | 0 | 3 of 3 |

- **"Turns out" is the dominant pivot marker** — present in every sample, always marking the
  move from an assumption the author acted on to the corrected finding.
- **Mechanical transition words are entirely absent** across all 780 words — a small corpus, so
  this is a directional signal only, not a statistically load-bearing one at n=3, but it
  matches the shape of the finding a real (8–15-sample) corpus would let you state with
  confidence.
- **Semicolons appear in every sample (2–3 each)**, always yoking two balanced clauses ("Turns
  out the problem was never moisture at all; it was compaction three inches down...") — never as
  a list separator.

---

## 4. Evidence / Quotation Integration Style

Not applicable in a load-bearing way to this corpus — these are first-person observational
pieces with no outside sources quoted. (A real profile should say plainly when a phase doesn't
apply, rather than force an answer.)

---

## 5. Characteristic Syntactic and Rhetorical Moves

- **Openings:** all three samples open by stating what the author *believed and acted on*
  before the correction — never a scene-setting or general-topic opener.
- **Signature structural move:** "I thought it was [wrong cause], turns out it was
  [actual cause]" recurs, verified, in all three samples on three unrelated subjects (soil
  compaction, plant disease, watering method) — a real habit of mind at this tiny sample size,
  and the kind of claim a real profile should only make after checking ≥3 unrelated topics, per
  SKILL.md Phase 6.
- **Person:** first-person singular "I" only, never "we" — 13/8/10 raw instances per sample.
  Consistent across the whole (tiny) corpus, unlike a corpus that mixes "I" and "we" sample to
  sample.
- **Closings:** every sample ends on a forward-looking or plainly stated-limit line, never a
  bullet-style recap ("Next season I'm building a fourth bed..." / "The fruit up top doesn't
  know the bottom third is gone." / "It just isn't the last one.").
- **No rhetorical questions appear anywhere in the corpus** — worth noting as an absence, not
  just skipping the category.

---

## 6. Vocabulary Register and Recurring Signatures

- Plain, concrete, physical-object vocabulary throughout (broadfork, drip line, moisture
  reading) — no elevated or abstract register at pivot points; the "Turns out" pivot itself
  carries the register shift, not a vocabulary shift.
- **AI-marker vocabulary scan:** zero hits for delve/leverage/landscape/tapestry/multifaceted/
  foster/cultivate/facilitate/utilize/comprehensive/holistic/robust-as-filler/synergy/unlock/
  streamline/game-changer/cutting-edge across all 780 words. At this corpus size that's a weak
  signal on its own, but it is exactly the kind of scan a real (larger) corpus would run to
  produce an avoidance rule with real weight behind it.

---

## 7. Hedging Patterns — Genuine Qualification vs. Throat-Clearing

**The author's real hedging pattern — verified instances:**
- Named, specific, reason-tied admissions of the exact limit of a claim, always in a dedicated
  short paragraph, never scattered through the piece: "I haven't run this across every bed in
  the yard, only the three on the east side, so I can't say compaction explains every wilting
  bed anyone will ever have" (sample-1); "I don't know whether this holds for container
  gardens the same way, since containers dry from more directions at once" (sample-3).
- **Scope-narrowing, not confidence-softening**: each hedge narrows *what the claim covers*
  ("only the three on the east side," "for beds in open ground") while stating the core finding
  plainly and without a qualifier.

**What does NOT appear anywhere in the corpus:**
- No "it is worth noting that," "arguably," "to some extent," or vague both-sides gestures.

**Practical rule:** when a future "Backyard Beds" post needs to mark a limit, do it the way
this author does — one dedicated short paragraph, naming exactly what wasn't tested, scope
narrowed rather than confidence softened. Don't sprinkle "might"/"perhaps" through the rest of
the piece; this author's plain declarative claims stay plain.

---

## 8. Genre-Gap Notes

*(Omitted — this worked example has no target document/context to calibrate toward. A real
profile built to calibrate, say, a print-magazine gardening column from this same voice would
fill this section: e.g., the direct "I" address and the first-person confessional hedge
paragraph would need a note on whether a magazine's house style allows first person at all.)*

---

## 9. DO / DON'T List

**DO:**
1. Open by stating what the author believed and acted on, then pivot with "Turns out" to the
   corrected finding — not "however" or "it turns out that," the bare two-word phrase.
2. Let one long, comma-chained sentence carry the setup, then land on a short (≤10-word)
   declarative sentence immediately after it.
3. Use a semicolon to yoke two balanced clauses at least once per piece; never as a list
   separator.
4. Close on a forward-looking line or a plainly stated limit — never a bullet-style recap.
5. When hedging, use one dedicated short paragraph that narrows scope by name ("only the three
   beds on the east side") rather than softening confidence with "might" or "perhaps."

**DON'T:**
1. Don't use "however," "furthermore," or "in conclusion" — this corpus has zero instances of
   any of them.
2. Don't switch to "we" — this author's first person is singular only, consistently, across
   every sample checked.
3. Don't decorate with a rhetorical question — none appear in the corpus.
4. Don't scatter soft qualifiers ("arguably," "to some extent") through ordinary declarative
   sentences — this author's hedges are concentrated, named, and scope-narrowing only.

---

## 10. Representative Passages (voice exemplars only)

*Quoted strictly as voice exemplars from fabricated demonstration text. Per the Guardrail
below, none of this wording may be reused as-is in future "Backyard Beds" writing — a real
profile applies the identical restriction to real corpus text.*

**1. The "Turns out" pivot (DO #1) —** `sample-1-soil.txt`
> "Turns out the problem was never moisture at all; it was compaction three inches down..."

**2. Long-sentence-then-short-reset (DO #2) —** `sample-2-blight.txt`
> "...they behave, spread, and respond to treatment completely differently." / "Don't."

**3. Scope-narrowing hedge (DO #5) —** `sample-3-watering.txt`
> "I don't know whether this holds for container gardens the same way, since containers dry
> from more directions at once, and I haven't run the six-inch test on a single pot yet."

---

## Guardrail

This profile calibrates voice, never content. Nothing in this document — including the
fabricated soil/blight/watering "findings" used as demonstration text — should be read as real
gardening advice or reused as factual content anywhere; it exists only to show what a measured
style profile looks like.
