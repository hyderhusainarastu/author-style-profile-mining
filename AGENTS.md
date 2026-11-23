# author-style-profile-mining

An Agent Skill (SKILL.md) that mines a writing corpus for an author's measurable stylistic habits and turns them into a DO/DON'T checklist.

## Using this in your project

- Use this skill when the user wants to match a person's or publication's voice, build a style guide from sample documents, or audit hedging and filler without erasing a writer's real voice.
- Invoke it by loading `SKILL.md` (native skill install, or paste `PROMPT.md` into a chat). Follow its phases in order.
- Inputs: at least 5 writing samples from one voice (8-15 is better). With 1-2 samples, label the profile low-confidence.
- Output: one style-profile document, structured like `references/output-template.md`. Write it where the user asks; default to a new file in the user's working directory, never inside the skill folder.
- Report only habits that recur across several unrelated samples. Back every rule with a count or a quoted instance.
- Never copy sentences, arguments or facts from the corpus into a draft. The profile covers voice, not content.
- Never publish a profile built from private or unpublished text without the owner's consent.
- `PROMPT.md` is the paste version of this skill for chat UIs.

## Working on this repo

- Setup: none. There are no dependencies and no code besides `install.sh`.
- Install into a tool: `./install.sh --claude` or `./install.sh --agents --project .` (run `./install.sh -h`).
- Test: `bash -n install.sh` checks syntax. The examples in `examples/` are synthetic; keep any new example synthetic too.
- Keep the `SKILL.md` frontmatter description at 300 characters or fewer.
- Do not add real author text or personal data to `examples/`.
