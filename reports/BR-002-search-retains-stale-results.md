# BR-002: Search keeps previous results after a no-match query

| Field | Value |
| --- | --- |
| Area | Product search |
| Severity | Medium |
| Priority | Medium |
| Type | Functional / state management |
| Frequency | 3 of 3 attempts |
| Status | Ready for triage |

## Environment

- Desktop web
- Firefox
- Windows 11
- Guest session

## Preconditions

At least one searchable product is available.

## Steps to reproduce

1. Search for a valid product name.
2. Wait for matching results to appear.
3. Replace the search text with a value that has no matches.
4. Submit the second search.

## Expected result

The earlier results should be cleared and a no-results message should describe the second query.

## Actual result

The earlier product cards remain on screen below the no-results message until the page is refreshed.

## Impact

A customer can select a result that does not match the current query. This reduces trust in search and creates a risk of adding the wrong item.

## Severity and priority reasoning

**Medium severity:** search remains usable after refresh, but the displayed state is misleading.

**Medium priority:** the issue should be fixed in the next search-related release unless analytics show a high no-result rate.

## Evidence

- Video to capture: valid search followed by no-match search
- Suggested filename: `evidence/BR-002/stale-search-results.mp4`
- Network note: both search requests returned successfully
- Screenshot: no-results message displayed above stale cards

## Retest criteria

Repeat with keyboard submission, the search button and rapid consecutive queries. Confirm old results are removed while the latest request is pending and after it completes.
