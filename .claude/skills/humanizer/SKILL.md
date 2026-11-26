---
name: humanizer
version: 2.4.0
description: |
  Editorial style guide based on Wikipedia's "Signs of AI writing" (WikiProject AI Cleanup).
  Strips textbook clichés, inflated symbolism, promotional phrasing, superficial -ing endings,
  em-dash spam, rule-of-three lists, copula avoidance, and soulless uniform cadence while
  injecting authentic human voice, varied sentence rhythm, and concrete specificity.
allowed-tools:
- Read
- Write
- Edit
- Grep
- Glob
---

# Humanizer v2.4: Editorial Style & Voice Guide

## Core Task
1. Scan text for all 30 patterns below (24 classic WikiProject AI Cleanup patterns + 6 v2.4 social/editorial clichés).
2. Replace sterile, predictable phrasing with natural, plain-spoken language.
3. Preserve all confirmed facts, technical metrics, and core meaning.
4. Inject genuine human voice: opinions, mixed feelings, first-person honesty, and irregular sentence rhythm.

## Personality and Soul (Anti-Sterility Rules)
- **Have opinions & mixed feelings:** Don't just report events neutrally; react to them honestly.
- **Vary rhythm:** Mix blunt 3–6 word sentences with longer, winding 25+ word sentences. Never let three sentences of similar length follow each other.
- **Let some mess in:** Avoid algorithmic symmetry. Use asides, natural contractions, and plain verbs (`is`, `are`, `has`, `built`, `fixed`) instead of elaborate phrasing.

## 30 Patterns to Strip Immediately
1. **v2.4 Permission & Staged Openers:** Never use `"The truth is"` as a standalone opener, `"And honestly?"` before a non-controversial claim, `"Read that again"`, `"Let that sink in"`, formulaic achievement-post endings (emotion word + team thanks + generic lesson), or fake staged dialogue.
2. **Significance Inflation:** Cut `serves as`, `stands as`, `testament`, `pivotal`, `crucial`, `vital`, `underscores`, `highlights its importance`, `marking a shift`, `evolving landscape`, `indelible mark`.
3. **Superficial `-ing` Endings:** Cut tacked-on present participles (`highlighting...`, `underscoring...`, `ensuring...`, `reflecting...`, `fostering...`, `showcasing...`).
4. **Promotional Tone:** Cut `boasts`, `vibrant`, `rich`, `profound`, `groundbreaking`, `nestled`, `exemplifies`, `commitment to`.
5. **Vague Attributions:** Replace `experts say` or `observers note` with concrete first-hand facts.
6. **Formulaic Challenges:** Cut `Despite these challenges...` transitions.
7. **Banned AI Vocabulary:** `Additionally`, `align with`, `delve`, `emphasizing`, `enduring`, `enhance`, `fostering`, `garner`, `interplay`, `intricate`, `key` (adj), `landscape`, `tapestry`, `underscore`, `valuable`, `navigate`, `empower`, `elevate`, `resonate`, `multifaceted`, `journey`, `passion`.
8. **Copula Avoidance:** Replace `serves as / stands as / functions as / features / offers` with `is`, `are`, or `has`.
9. **Negative Parallelisms:** Cut `Not only X, but Y` and `It's not just about X; it's Y`.
10. **Rule of Three:** Break up forced triplets of adjectives, nouns, or clauses.
11. **Synonym Cycling:** Don't swap synonyms awkwardly just to avoid repeating a plain noun.
12. **False Ranges:** Cut `from X to Y` when X and Y aren't on a real scale.
13. **Em Dash Overuse:** Replace em dashes (`—`) with commas, periods, or parentheses.
14. **Formatting & Punctuation:** Plain-text ASCII only inside essay bodies—no boldface, no emojis, no curly quotes (`“`/`”`/`’`), only straight quotes (`"`/`'`).
15. **Filler & Hedging:** Cut `In order to`, `Due to the fact that`, `At this point in time`, `It is important to note`, `could potentially`, `might have some`.
16. **Generic Upbeat Endings:** Cut `The future looks bright` or neat inspirational wrap-ups; end on concrete actions or plans.
