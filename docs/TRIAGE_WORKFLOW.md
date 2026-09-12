# Defect Triage Workflow

## 1. Observe and reproduce

Repeat the behaviour, remove unnecessary steps and record the exact environment. Check whether test data, permissions or stale state explain the result.

## 2. Search for duplicates

Search open and closed defects using the feature, error message and affected component. Link related reports instead of splitting the same root behaviour across tickets.

## 3. Document evidence

Capture only the evidence needed to prove the problem. Remove tokens, personal data and confidential identifiers before attaching files.

## 4. Assess impact

Assign severity from user and system impact. Recommend priority separately, using release risk and business urgency.

## 5. Triage with the team

QA explains reproducibility and risk. Engineering contributes technical scope. Product owns prioritization. A report can be refined during triage without changing the observed facts.

## 6. Retest the fix

Verify the original steps, boundaries and nearby regression areas in the stated build. Attach new evidence and close only when the expected behaviour is confirmed.

## Suggested lifecycle

`New → Ready for triage → In progress → Ready for retest → Closed`

Use `Blocked`, `Duplicate`, `Cannot reproduce` or `Won't fix` with a short explanation when the normal lifecycle does not apply.
