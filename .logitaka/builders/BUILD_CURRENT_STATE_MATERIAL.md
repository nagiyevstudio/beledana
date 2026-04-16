# BUILD CURRENT STATE MATERIAL

## Dev Team Repo Bootstrap

- Target file: `.logitaka/CURRENT_STATE_MATERIAL.md`
- Work only on the current repository and current branch.
- Replace the target file with the final generated report content.
- Commit and push the generated target file to the current branch after the report is ready.
- Leave this builder file in place; Logitaka will remove it after importing the updated context.

## Builder Prompt

You are extracting the current execution state from an existing code repository.

Your task is to create CURRENT_STATE_MATERIAL.md as raw material for Logitaka.

This is NOT a final current-state document.
This is only a compact evidence-based snapshot of what appears to be happening now.

---

## GOAL

Extract a useful current-state snapshot that helps Logitaka understand:

- what changed recently
- what areas are active now
- what appears unfinished or in-progress
- what likely needs review or clarification

---

## STEP 1 — Inspect recent execution evidence

Use available sources:

- .logitaka/DEVLOG.md
- recent git diff / changed files / recent commits (if accessible)
- .logitaka/INDEX.md
- .logitaka/SYSTEM_MAP.md

Focus on recent activity and visible implementation evidence.

---

## STEP 2 — Identify recent changes

Extract:

- recent completed changes
- recently touched modules or directories
- areas with concentrated activity

Keep this factual and short.

---

## STEP 3 — Identify active or in-progress work

Find evidence of work that appears ongoing:

- partially changed modules
- recently touched but clearly unfinished areas
- integration points that appear incomplete
- TODO / FIXME / placeholders if directly relevant to current active work

Only include visible evidence.

---

## STEP 4 — Detect drift or mismatches

Identify cases where there may be a mismatch between code state and documented/project state.

Examples:

- recent implementation evidence suggests progress not yet reflected elsewhere
- module was changed but related area still looks incomplete
- active work seems split across several files without closure

Be conservative.
If unsure, omit.

---

## STEP 5 — Identify review-needed points

Extract short points that may require Logitaka review:

- unclear completion state
- unfinished integration
- possible follow-up needed
- possible need to update roadmap / decisions / zone context

Do not prescribe solutions.
Only surface review-worthy evidence.

---

## STEP 6 — Build CURRENT_STATE_MATERIAL.md

Structure:

# CURRENT STATE MATERIAL

## PURPOSE

Raw evidence-based snapshot of current execution state.
Not a final current-state document.

## RECENT CHANGES

(list recent factual changes)

## ACTIVE AREAS

(list areas currently active)

## IN-PROGRESS OR INCOMPLETE WORK

(list clearly unfinished work)

## DRIFT OR MISMATCH SIGNALS

(list possible mismatches, only if visible)

## REVIEW NEEDED

(list points that may need Logitaka review)

---

## RULES

- Only include observable evidence
- Do not invent intent or roadmap
- Do not repeat full devlog history
- Keep entries short
- Prefer omission over guessing

---

## CONSTRAINTS

- Keep under ~150 lines
- Use bullet points
- Avoid long explanations
- No business/product speculation
- No final conclusions beyond visible evidence

---

## OUTPUT

Return only CURRENT_STATE_MATERIAL.md content.
