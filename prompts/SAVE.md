# Save and Retrieve

## Language and Paths

Before writing, apply the explicit saved-language choice in `private/PREFERENCES.md`.
If it is absent, ask for the preferred language and wait before writing personal records.
Write note prose, judgments and new index descriptions in that language; keep
structured field names English and preserve original user quotes verbatim.
Do not translate existing entries without a request. Local saving does not include
Git staging, committing, pushing or syncing. Resolve workspace paths from
[MAIN.md](../MAIN.md)'s directory, not from the prompts directory. Use UTF-8.

## First Save

Only `.gitkeep` placeholders for `private/papers/` and `private/notes/` are shipped;
no personal records are included. Once the language preference
is confirmed and the user requests a record, create missing `private/notes/`,
`private/LIBRARY.md` and `private/TAGS.md` automatically. Create `private/papers/`
only if needed; an original PDF may remain at its supplied external path. Never
overwrite an existing index to initialize it. No setup script or prebuilt library
is required.

Initialize the library with `Archived`, `In Progress`, `Paused`, and
`Provisional Summary` sections. Use `summary_not_archived` for a provisional
record. Populate only the section matching the note's current status. A progress
record remains `in_progress`; saving alone does not mean reading is complete.
Initialize the tag index with a library backlink and entries for the current
paper's tags. Create tag anchors only as needed.

## One Paper, One Note

On save, use [NOTE.md](../templates/NOTE.md). Choose a stable `paper_id`
(letters, digits, hyphens, underscores), checking existing DOI/title to avoid duplicates.
Create `private/notes/<paper_id>.md`; update it on continuation. No duplicate JSON,
database or required script is needed.

Record title, DOI/version, source filename and relative path when available.
For an external source, retain its original path. A checksum is optional for version
matching; never invent it. Unknown DOI stays unknown; label related preprints.

Preserve the user's judgment, why they saved it, technical clarifications, evidence
locations, useful figures and limits on reuse. On revisions, append a dated History
entry with the old/new judgment or tag and reason; do not erase earlier feedback.
This restores saved conclusions, not every unsaved chat message.

## Tags

Use a few stable snake_case tags:

- `decided_tags`: explicitly confirmed by the user; the main retrieval categories.
- `suggested_tags`: proposed, not confirmed.
- `warning_tags`: assumptions and limits affecting reuse.
- `negative_tags`: negative judgments.
- `not_primary_tags`: related concepts that must not imply a main endorsement.

Topics, methods, writing/visual references and personal recall phrases can all be
tags. Keep their confirmation/category explicit. A tag revision changes current
tags and indexes; the previous decision remains in History.
Do not treat praise for a topic or figure as confirmation of an exact tag name.
Unless the user confirms a tag or directly requests that label, put inferred tags
in `suggested_tags`. Preserve the expressed judgment in the note regardless.

## Two Indexes

1. `private/LIBRARY.md`: separate archived, in_progress, paused and provisional
   summaries. Each row links title/note, DOI (if known), original and tags.
2. `private/TAGS.md`: one stable anchor per tag; link papers grouped by decided,
   suggested, warning, negative and not_primary. Link back to the library.

Use relative links inside private/. A missing source stays listed by its filename
with an availability warning. Excluded papers have no entry. Update only the current
paper's entries; retain unrelated notes and tags.

## Before Finishing

Open the written note; check metadata, status, conclusion, tags and evidence.
Follow the note, original and tag links in both directions. Personal files remain
under `private/`; personal Markdown files are ignored. Do not publish them. Report the note
and library links; never claim a successful
write or check that was not performed. If writing is unavailable, return the filled
note and index updates as text and state that they were not saved locally.

Apply MAIN.md's original-reading reminder only if the reply also analyzes the
paper; omit it from save-only confirmations.
