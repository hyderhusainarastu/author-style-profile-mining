# author-style-profile-mining

Mine a writing corpus for an author's recurring stylistic habits — sentence rhythm, paragraph
shape, transition words, syntactic moves, vocabulary register, hedging patterns — and turn the
findings into a concrete DO/DON'T checklist that future drafts can imitate or avoid.

## What it does, in plain language

Give this skill a handful of writing samples from one person (or one consistent voice — a
brand, a publication, a character), and it walks through a measured, evidence-first procedure
to answer one question: *how does this writing actually sound, specifically, and how would you
reproduce that on purpose?*

It doesn't guess at vibes ("sounds formal," "sounds casual"). It counts things — sentence
lengths, transition-word frequency, semicolon rates, hedging phrases, first-person pronoun
use — cross-checks the counts against close reading, and only then converts what it finds into
imperative rules a writer or drafting agent can actually apply: *use word X as your default
pivot, not "however"; never close a section on a bullet recap; scope-narrow your hedges instead
of softening them.*

It also includes a specific, useful sub-technique: telling genuine, deliberate hedging apart
from generic AI-sounding throat-clearing ("it is worth noting that," "arguably," "to some
extent"), so an editing pass aimed at removing AI-texture doesn't accidentally erase a writer's
real voice along with it.

**One hard rule the whole method is built around:** the output profiles *voice*, never
*content*. It never extracts arguments, facts, or reusable material from the source corpus —
only the shape of how that corpus is written. Any future draft that wants to reuse an idea from
the corpus needs separate sourcing; the style profile is not a shortcut for that.

## Works with

| Surface | How | Status |
|---|---|---|
| Claude Code | native skill (`./install.sh --claude`) | not tested |
| Codex | native skill via `.agents/skills` (`./install.sh --agents --project .`) | not tested |
| Gemini CLI | native skill via `.agents/skills`, or pointer block (`--gemini`) | not tested |
| Cursor | native skill via `.agents/skills`; reads `AGENTS.md` | not tested |
| Copilot | pointer to `AGENTS.md` (`--copilot`) | not tested |
| ChatGPT / Claude.ai / Gemini (chat) | paste `PROMPT.md` | not tested |

## Quick start

```sh
git clone https://github.com/hyderhusainarastu/author-style-profile-mining
cd author-style-profile-mining
./install.sh --claude              # ~/.claude/skills/author-style-profile-mining
./install.sh --agents --project .  # .agents/skills in the current project
./install.sh -h                    # all options; --dry-run and --uninstall are supported
```

For a chat UI, paste `PROMPT.md` and then your samples. No dependencies; the skill is `SKILL.md` plus the reference template.

Then ask your agent, for example:

> Use the author-style-profile-mining skill on the 8 posts in `samples/`. Profile the voice only, then give me a DO/DON'T checklist I can hand to a drafting agent. Mark anything that appears in only one sample as a topic artifact.

You get back one profile document with a count or quote behind every rule.

## Worked example (synthetic data)

`examples/synthetic-corpus/` contains three short, entirely fabricated blog-style posts from a
made-up voice ("Backyard Beds," a fictional gardening blog written for this example only).
`examples/synthetic-style-profile.md` is the full profile produced by running this skill's
procedure against those three files — computed from real counts against the sample text, so you
can see exactly what a completed profile looks like at every phase: the sentence-length
distribution table, the transition-marker table, the hedging-vs-throat-clearing classification,
and the final DO/DON'T list.

A short excerpt of the pattern it surfaces:

> **DO:** Open by stating what the author believed and acted on, then pivot with "Turns out" to
> the corrected finding — not "however" or "it turns out that," the bare two-word phrase.
>
> **DON'T:** Don't scatter soft qualifiers ("arguably," "to some extent") through ordinary
> declarative sentences — this author's hedges are concentrated, named, and scope-narrowing
> only.

Every rule in that list traces back to a specific count or quoted instance in the profile —
that traceability is the point of the method, and worth preserving in any profile you build
from real material.

## Reference material

`references/output-template.md` is a ready-to-fill markdown skeleton mirroring every phase in
`SKILL.md` — copy it as the starting point for a new profile rather than building the section
structure from scratch each time.

## Limits

- Counts are only as good as the sample: under 5 samples gives a low-confidence profile.
- Sentence splitting is regex-based, not a full linguistic parser.
- It profiles voice, not content, and does not detect who wrote a text.

## Related

- [ai-writing-humanizer](https://github.com/hyderhusainarastu/ai-writing-humanizer): flags AI-sounding patterns and rewrites drafts in plainer prose.
- [structural-checklist-from-exemplars](https://github.com/hyderhusainarastu/structural-checklist-from-exemplars): derives a structural checklist from exemplar documents.
- [palimnote-skills](https://github.com/hyderhusainarastu/palimnote-skills): catalog of sibling skills.

## Keywords

stylometry, writing style analysis, style guide, voice matching, copyediting, hedging, agent skill, SKILL.md

## License

MIT. See `LICENSE`.

---
Part of palimnote-skills - more at https://github.com/hyderhusainarastu
