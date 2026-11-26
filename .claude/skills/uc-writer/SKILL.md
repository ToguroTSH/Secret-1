---
name: uc-writer
description: Draft one UC transfer PIQ at a time (325-350 words) from the approved strategy matrix, interview log, and the applicant's voice sample. Use only after piq-strategy-matrix.md is approved.
---

# UC Writer

## Inputs (read all before writing)
- `01-research/winning-patterns.md`
- `02-interrogation/piq-strategy-matrix.md` (must be approved by the user)
- `02-interrogation/interview-log.md`
- `00-context/voice-sample.md`
- Any existing drafts in `03-drafts/` (to avoid repeating stories, openings, or traits)

Draft ONE PIQ per run unless the user asks otherwise.

## Positioning
- Frame every real action, responsibility, and outcome at its highest defensible level of ownership, rigor, and impact. Use active verbs and the applicant's specific decisions.
- Never fabricate anything: no invented orgs, awards, titles, numbers, dates, or events. Every claim must trace to `00-context/` or [[interview-log]]. If a stronger draft needs a missing fact, stop and ask the user for it.

## Tone: UC interview, not a movie
- No cinematic hooks, metaphors, quotes, or throat-clearing ("Ever since I was young..."). Open directly with the problem, action, or decision.
- Plain, direct sentences in the applicant's own rhythm and vocabulary from [[voice-sample]].
- Self-contained: no jargon, acronyms, or references a reader can't understand without clicking a link. Define anything specialized in a few words.
- Answer every sub-clause of the prompt explicitly (check them off).
- Show, then reflect briefly: what they did, what changed, what it means for them now / at UC.

## Format
- Strictly 325-350 words (count with a script, not by eye).
- Plain ASCII text: straight quotes, minimal dashes, no markdown inside the essay body.
- Save to the matching file: `03-drafts/piq-required-major.md`, `piq-opt-1.md`, `piq-opt-2.md`, or `piq-opt-3.md`.
- File layout:
  ```
  # <Slot> - <Prompt short name>
  Prompt: <full prompt text>
  Story: <one line, from [[piq-strategy-matrix]]>

  <essay body>

  Word count: N
  Sub-clauses answered: <list>
  Facts to verify with applicant: <list or "none">
  ```

## After drafting
Run the `humanizer` skill in file mode on the draft, matched to [[voice-sample]], then recount words. Remind the user: read it aloud, change any line that doesn't sound like them (UC requires the PIQs to be their own work), then `/clear` before the next PIQ.
