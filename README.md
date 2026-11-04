# PaperWeave

**A Structured Tool for Literature Reading, Understanding Maps, and Tag Organization**

Read papers with an AI agent, explore an understanding map, save your own judgment
and tags, and find the paper later by a remembered idea, DOI or filename.

## Start

Open this folder in an AI app with file/PDF access. Give it [MAIN.md](MAIN.md):

```text
Read MAIN.md and follow it. Use Chinese for conversation and English field names.
```

Then provide a paper, choose a map node or ask a question, and say "save" when ready.
Use "pause" for a checkpoint or "do not archive". Apps supporting AGENTS.md can
discover the entry automatically.

## Your Library

```text
private/
  papers/           original PDFs (or use an external source path)
  notes/            one Markdown reading record per paper
  LIBRARY.md        paper, DOI, note, original and tag links
  TAGS.md           tags -> papers
```

Put papers in `private/papers/` or supply an external path. On first save, the agent
creates the note and indexes. Notes and indexes are eligible for Git tracking;
PDFs are ignored. The folder name private/ does not enforce access restrictions.

Later ask by remembered judgment, tag, DOI, title or original filename.

## What Is Included

[MAIN](MAIN.md) links the [reading rules](prompts/READ.md),
[saving rules](prompts/SAVE.md) and [single note template](templates/NOTE.md).

No Python package or server is required. Automatic saving needs an AI app that can
write files; plain chat only returns text. Notes preserve conclusions, not full chats.

You decide whether to keep your library local, back it up in a private repository,
or share selected notes. Add `/private/` to your own .gitignore if you want to
exclude the whole library. Choose your own repository and license.
# PaperWeave
