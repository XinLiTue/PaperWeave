# Read and Understand

Before the first understanding map, follow [MAIN.md](../MAIN.md)'s saved-language preference
check. Ask for the preferred language if no explicit preference exists; reading the paper
can proceed while awaiting the answer, but personal records must wait.
Apply MAIN.md's original-reading reminder only to replies containing paper
analysis, using the user's confirmed language preference.

## First Response: Understanding Map

Identify the title, authors, year, DOI/version and available source content.
Give a 2-4 sentence orientation, then a compact table with these nodes:

| node | question |
| --- | --- |
| background | Why does the problem matter? |
| problem | What precise question is being answered? |
| approach | How do data, models and algorithms connect? |
| effect | What evidence and results support the answer? |
| innovation | What is new, and what is reused? |
| limitations | Under which assumptions does the answer hold? |
| user_fit | Why would the user retain or ignore it? |
| recall_hooks | What phrase would help find it later? |

Keep each row short. Explain that the map offers reading directions, and the user
can select one or multiple nodes to deepen, switch branches, or examine connections
between them. When useful, show a compact branching diagram; it is a navigation aid,
not necessarily a formal concept map. Ask which node(s) to deepen: depth 1 for
structured explanation, depth 2 for technical analysis. These are optional depth
choices, not a required form. A concrete question already selects the direction;
answer it directly rather than forcing a menu. Limit confidence for partial inputs.
The initial map may be a table; do not require diagram generation. Use a diagram
only when it helps clarify the paper or the user asks for one.

## Selected Deepening

- Explain the mechanism and define variables before manipulating formulas.
- Locate the evidence: section, PDF page, equation, figure or table.
- Check assumptions, baselines, data provenance and the scope of guarantees.
- Distinguish model validity from solver success; sufficient from necessary
  conditions; simulation from measurement; new algorithms from integration.
- Mark your own examples and inferences. A suspected printed error is not proof
  of a code defect. Simple formulas do not establish small actual workload.
- Capture questions, clarifications and important user quotes. Invite brief feedback.
  Keep them in the current discussion until the user requests a saved record.

When useful, record the diagram/chart type, figure number, its explanatory role
and why the user would reuse it. Visual value and modeling value are independent.
Do not read fictional demonstrations or another person's notes as source evidence.
