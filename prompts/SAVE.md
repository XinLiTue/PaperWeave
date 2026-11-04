# Save and Retrieve

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
Follow the note, original and tag links in both directions. Leave library tracking
and sharing decisions to the user; PDFs are ignored by default. Report the note
and library links; never claim a successful
write or check that was not performed. If writing is unavailable, return the filled
note and index updates as text and state that they were not saved locally.
