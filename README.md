# unreal-fiction

A skill for writing speculative fiction, fanfiction, and AU — in Chinese or English.

AI fiction fails in predictable ways: characters agree too fast, the world is decoration, every sentence is equally smooth. This is a set of editorial instructions that push back. The model has to fix a canon cutoff before writing, keep canon / AU divergence / invention as separate layers, trace at least three causal steps from a world rule to a personal consequence, and run a revision pass that targets prose symptoms in clusters instead of banned words.

## Install

Claude Code:

```bash
git clone https://github.com/sylviachangdou-prayer/fanfic-AU-apocrypha ~/.claude/skills/unreal-fiction
```

Claude app: zip the folder and upload it under Settings → Capabilities → Skills.

To update: `git pull` in that directory, or re-upload the zip.

Then just ask for the story. The skill loads itself, and loads only the reference files your request needs.

## Inside

`SKILL.md` routes the request and holds the core workflow. `references/` has the detail: canon grounding, craft, prose tells, Chinese web-fiction quality gates, relationship tropes, and settings — interstellar, vampires, wizarding world, Westeros, assassins, apocalypse, wasteland, medieval, cyberpunk, ABO. `templates/story-bible.md` carries continuity across chapters.

## What this is not

No training, no fine-tuning, no distillation, no scraped corpus, no dataset. The repository is about 1,700 lines of Markdown and you can read all of it. Nothing was learned from anyone's writing without permission, because nothing was learned at all — these are written instructions, not weights.

The skill forbids reproducing source wording, and it never claims output is undetectable or human-written.

## License

MIT. Whatever you write with it is yours.
