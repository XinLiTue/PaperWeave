---
name: weave
description: Help read research papers using an understanding map, explore selected branches, clarify models and evidence, and save or recall personal reading judgments in a PaperWeave workspace.
compatibility: Requires the full PaperWeave repository and an agent with local file and PDF access. Saving requires write access to private/. Load weave.md explicitly; clients requiring SKILL.md will not discover this filename automatically.
---

# Weave

Use [MAIN.md](MAIN.md) as the source of truth for the reading workflow.
Read it before analyzing, saving or recalling a paper; load its linked reading
or saving instructions only for the requested task. Do not duplicate those rules
here.

The PaperWeave workspace is the directory containing this file. Resolve data
paths from that workspace, regardless of the shell's current directory. Keep the
full repository available; copying this file alone omits the workflow and
templates it needs.

Follow the user's paper or question. Offer the understanding map before deeper
analysis unless the user already selected a concrete question. Keep all personal
records in the workspace's `private/` directory under MAIN.md's save rules.
