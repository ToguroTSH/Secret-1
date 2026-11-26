---
name: uc-auditor
model: opus
description: Final packet audit across all 4 PIQs and all 20 UC Activities & Awards.
---

Read `CLAUDE.md`, all 4 PIQ files in `04-final/`, `00-context/activities-list.md`, `00-context/courses-and-majors.md`, `00-context/voice-sample.md`, and `01-research/winning-patterns.md`.

## 1. Cross-PIQ audit
Table: PIQ | Story | Evidence used | Opening style | Core trait. Verify zero story/evidence/trait overlap, 4 distinct opening styles, and zero leakage from `voice-sample.md` (meditation, BrighterMinds, Arjun, running/cross-country, Nikhil, Coach Esayas, box-breathing, panic attacks).

## 2. Prompt alignment
For each PIQ, list every sub-clause of its prompt and mark answered / partial / missing, quoting the line that answers it.

## 3. Strict compliance (use scripts, not eyeballing)
- Essay body 325-350 words (PowerShell: `($body -split '\s+' | Where-Object { $_ }).Count`).
- Plain ASCII: no character above code 127, no smart quotes, no em/en dashes, no markdown in the body.
- Fact guardrails from `CLAUDE.md`: no planned Spring 2027 course claimed as taken; every number traceable to `00-context/`.
- Banned words: delve, tapestry, testament, foster, showcase, underscore, pivotal, transformative, impactful, meaningful, journey, passion, multifaceted, resonate, navigate, landscape, empower, elevate.

## 4. EC-to-PIQ bridge
Write `04-final/uc-activities-350char.md`: all 20 Activities & Awards, each description tightened to strictly <= 350 characters (count with a script; count every character including spaces), plain ASCII, with the exact character count printed beside each entry. Keep each entry's category, title, and hours/weeks above its description. Complement the PIQs instead of repeating them: where a PIQ tells the story, the entry gives the hard facts (scope, numbers, tools). Use only facts in `activities-list.md`, and fix the consistency flags listed there (do not claim Physics 421/431 or other planned courses as taken).

## 5. Fix and report
Fix any failing PIQ directly in `04-final/` (minimal edits, no new facts), re-run every check, and write `04-final/AUDIT-REPORT.md`: pass/fail scorecard (PIQ x check, before fix and after fix), the overlap table, a list of every fix made, and a consolidated "Facts to verify with applicant" list from all 4 PIQs. Use [[wikilinks]] to the files. Return the scorecard.
