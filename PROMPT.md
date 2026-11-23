# Author style profile (paste into ChatGPT, Claude.ai, Gemini or a local model)

You will build an author style profile: a measured account of how one writer (or one consistent voice) writes, ending in a DO/DON'T checklist for imitating or avoiding that style.

## Guardrails
- Profile voice, never content. Do not reuse sentences, arguments, examples or facts from the samples in any draft. Reuse of an idea needs separate sourcing.
- Call a habit a "signature" only if it recurs across several samples on unrelated topics. A pattern from one sample or one topic is a topic artifact; say so.
- Every claim needs a count or a short quoted instance. Anything else is a "qualitative read" and must be labeled that way.
- Fewer than 5 samples means a low-confidence profile. Skip claims about consistency across the corpus.

## Procedure (do in order, one numbered section each)
1. Corpus and method: number of samples, how text was extracted, what was trimmed (references, signatures, boilerplate), how sentences were split, known caveats.
2. Sentence length: mean, median, standard deviation, min, max, and the share of short (under 10 words) and long (over 30 words) sentences. Describe the rhythm.
3. Paragraphs: typical length, how they open and close, one-sentence paragraphs.
4. Transitions: count connectors per 1,000 words (however, but, so, turns out, then...). Name the default pivot word.
5. Quotation and evidence: how sources and quotes are brought in.
6. Syntactic and rhetorical moves: questions, fragments, lists of three, semicolons, dashes, parentheses, with rates.
7. Vocabulary: register, recurring signature words, first-person and second-person use, contractions.
8. Hedging versus throat-clearing: separate deliberate, scope-narrowing hedges (tied to a specific claim) from generic filler ("it is worth noting that", "arguably", "to some extent"). Protect the first kind in any edit.
9. Genre gap (only if I give a target document): where the target needs the voice to bend.
10. DO/DON'T checklist: 8-15 imperative rules, each citing the count or quote behind it.
11. Optional appendix: up to three short passages as voice exemplars only.
12. Restate the guardrail: the profile describes voice, not content.

## Output
Return one document with the sections above. Put the guardrail at the top and the bottom. Keep the checklist specific ("use X as the default pivot, not 'however'"), never vague ("sound formal").

## Start
Ask me for the writing samples (and the target document, if any). Then run the procedure.
