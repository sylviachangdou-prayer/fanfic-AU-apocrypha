# unreal-fiction

A skill for writing speculative fiction, fanfiction, and AU — in Chinese or English.

AI fiction fails in predictable ways: characters agree too fast, the world is decoration, every sentence is equally smooth. This is a set of editorial instructions that push back. The model has to fix a canon cutoff before writing, keep canon / AU divergence / invention as separate layers, trace at least three causal steps from a world rule to a personal consequence, and run a revision pass that targets prose symptoms in clusters instead of banned words.

## Install

Claude Code:

```bash
git clone https://github.com/sylviachangdou-prayer/fanfic-AU-apocrypha ~/.claude/skills/unreal-fiction
```

Claude app: download the zip from [Releases](https://github.com/sylviachangdou-prayer/fanfic-AU-apocrypha/releases) and upload it under Settings → Capabilities → Skills. Then just ask for the story — the skill loads itself, and pulls in only the reference files your request needs.

To update: `git pull` in that directory, or re-upload the zip.

### Other assistants

Nothing here executes. It is Markdown, so ChatGPT, DeepSeek, 豆包, Kimi, 通义 and the rest can run it too — you just load it by hand, because automatic progressive disclosure is a Claude Skills feature.

- **With a project, agent, or custom-GPT builder** (ChatGPT, 豆包, Kimi, 通义): paste `SKILL.md` into the instructions field and upload `references/` and `templates/` as knowledge files.
- **Plain chat** (DeepSeek and anything without a builder): paste `SKILL.md` as the system prompt where one exists, or as your first message where it does not.

`SKILL.md` alone is about 15 KB and gets you the workflow. Instruction fields with a length cap will not take all 136 KB, so add only what the request needs: `craft.md` and `anti-ai.md` always, `source-grounding.md` for fanfiction or AU, `chinese-web-fiction.md` for Chinese, plus the one matching setting file.

## Methodology

作为一个十余年的同人女，阅尽论坛、贴吧、LOFTER、Tumblr、AO3 的起承转合 — and none of that reading survived contact with a language model. This repository is what came out of the collision. Every rule was produced the same way: generate a passage with a frontier model, mark by hand where it failed as fiction, work out the general instruction that would have prevented the failure, write it down. Nothing was trained, fine-tuned, or distilled. There is no corpus and no dataset. The whole thing is Markdown you can read in twenty minutes, including every mistake I made getting here.

- **Failure-driven, not advice-driven.** A rule enters only after a real generated passage failed in a way a reader would notice. Nothing was added because it sounded like good writing advice.
- **Hand-adjudicated.** Each candidate rule was tested against a rewrite of the same passage. Rules that did not change the output were dropped.
- **Editorial, not evasive.** The target is prose that reads as authored. This is not detector evasion, the repository makes no claim about how any text will be classified, and it rejects the zero-AI-score objective that most Chinese 去 AI 味 tooling optimises for.
- **No third-party text retained.** Style samples were abstracted into measurable features — sentence distribution, dialogue ratio, metaphor density, habitual omission — and then discarded. No fan work, no published fiction, and no author's voice is reproduced anywhere in this repository.
- **Bilingual by construction.** The Chinese and English rules were derived separately rather than translated, because the failure modes are not the same in the two languages.

## References

Recent work on machine-generated narrative shaped the chapter on tension and disclosure in `references/craft.md`.

- Sui, P., Zhu, Y., Cheng, T., West, P., So, R. J., Long, H., & Holtzman, A. (2026). *Spoiler Alert: Narrative Forecasting as a Metric for Tension in LLM Storytelling*. arXiv:2604.09854.
- Li, Z., Zhu, Y., Wu, S., Bao, H., & Evans, J. A. (2026). *Narrative Flattening: How Post-Training Compresses Thematic, Affective, and Stylistic Variation in LLM Fiction*. arXiv:2605.27878.
- Sui, P. (2026). *LLMs Exhibit Significantly Lower Uncertainty in Creative Writing Than Professional Writers*. arXiv:2602.16162.

Existing Chinese 去 AI 味 tooling and 说人话 prompt collections were surveyed and deliberately not adopted. Their dominant objective is a zero score from AI-detection services, and their dominant method is synonym substitution and sentence shuffling — both of which this repository forbids.

## Inside

`SKILL.md` routes the request and holds the core workflow. `references/` has the detail: canon grounding, craft, prose tells, Chinese web-fiction quality gates, relationship tropes, and settings — interstellar, vampires, wizarding world, Westeros, assassins, apocalypse, wasteland, medieval, cyberpunk, ABO. `templates/story-bible.md` carries continuity across chapters.

## What this is not

No training, no fine-tuning, no distillation, no scraped corpus, no dataset. The repository is about 1,700 lines of Markdown and you can read all of it. Nothing was learned from anyone's writing without permission, because nothing was learned at all — these are written instructions, not weights.

The skill forbids reproducing source wording, and it never claims output is undetectable or human-written.

## License

MIT. Whatever you write with it is yours.
