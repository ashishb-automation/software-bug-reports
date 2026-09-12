# Software Bug Reports

This repository shows how I document, assess and communicate software defects. The reports are written so that a developer, product owner or support analyst can understand the impact and reproduce the behaviour without needing a separate walkthrough.

## At a glance

| ID | Area | Summary | Severity | Status |
| --- | --- | --- | --- | --- |
| [BR-001](reports/BR-001-cart-allows-zero-quantity.md) | Cart | Zero quantity remains in the cart | High | Ready for triage |
| [BR-002](reports/BR-002-search-retains-stale-results.md) | Search | Previous results remain after a no-match search | Medium | Ready for triage |
| [BR-003](reports/BR-003-api-accepts-negative-page.md) | API | Negative page number returns a successful response | Medium | Ready for triage |
| [BR-004](reports/BR-004-modal-close-missing-focus.md) | Accessibility | Modal close control has no visible keyboard focus | Medium | Ready for triage |
| [BR-005](reports/BR-005-mobile-checkout-overlap.md) | Responsive UI | Checkout action is obscured on a narrow viewport | High | Ready for triage |

## What each report contains

- a concise, searchable title
- environment and preconditions
- numbered reproduction steps
- expected and actual behaviour
- severity and priority with separate reasoning
- customer and business impact
- supporting evidence references
- investigation notes and retest criteria

## About the examples

These are controlled portfolio exercises based on realistic behaviours seen in public QA training environments. They demonstrate my reporting approach; they are not presented as unresolved defects in a named third-party production product. Product names and account details are intentionally removed.

## Repository structure

```text
.
├── reports/                 # Completed defect reports
├── evidence/                # Evidence register and capture standards
├── templates/               # Reusable report and retest templates
├── docs/                    # Severity, priority and workflow guidance
└── .github/ISSUE_TEMPLATE/  # Structured GitHub issue form
```

## My reporting approach

I reproduce a problem at least twice before reporting it, then reduce the steps to the shortest reliable path. Severity reflects the technical and user impact; priority reflects how urgently the team should act. I avoid guessing at the root cause and clearly label investigation notes as observations.

The [severity and priority guide](docs/SEVERITY_AND_PRIORITY.md) explains the rating model. The [triage workflow](docs/TRIAGE_WORKFLOW.md) shows how a report moves from discovery through verification and closure.

## Using the template

Copy [the bug report template](templates/BUG_REPORT_TEMPLATE.md), replace every placeholder and attach evidence that does not expose personal or confidential data. A report is ready for triage only when another tester can reproduce it from the written steps.
