---
name: uc-auditor
description: Audit all 4 final UC transfer PIQs in 04-final/ together as one packet - repetition, prompt alignment, AI cadence, plain-text ASCII, and word counts - then output a pass/fail scorecard and fix failing drafts. Use when all 4 PIQs are in 04-final/.
---

# UC Auditor

Read all 4 files in `04-final/` together as one packet, plus [[piq-strategy-matrix]], [[winning-patterns]], and [[voice-sample]].

## Checks
1. **Cross-PIQ repetition audit** - table: PIQ | Story | Opening sentence type | Core trait | Key evidence. Fail if two PIQs share a story, an opening pattern, or lead with the same trait.
2. **Prompt-clause alignment** - list every sub-clause of each prompt; mark each answered / partial / missing.
3. **AI-cadence check** - flag not-X-but-Y contrasts, one-line closers, forced triads, staged openers, inflated words ("pivotal," "testament," "delve," "fostered," "navigate"), uniform sentence lengths, mismatch with [[voice-sample]].
4. **Plain-text ASCII check** - flag smart quotes, em/en dashes beyond 1 per essay, ellipsis characters, emojis, markdown in the body, any non-ASCII character. Use a script to detect them.
5. **Word count** - exact count with a script; fail if over 350 (also flag under 325).
6. **Fact check** - flag any claim not traceable to `00-context/` or [[interview-log]].
7. **Recency** - flag high school content that doesn't explain the current trajectory.

## Output
Write `04-final/audit-scorecard.md`: a pass/fail table (PIQ x check) plus notes. Then fix every failing draft directly in `04-final/` (keep facts intact; use the `humanizer` skill for cadence fixes), re-run the checks, and append the after-fix scorecard. Ask the user before changing any fact or story.
