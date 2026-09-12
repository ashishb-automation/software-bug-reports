# BR-005: Sticky footer obscures the checkout action on a narrow viewport

| Field | Value |
| --- | --- |
| Area | Mobile cart |
| Severity | High |
| Priority | High |
| Type | Responsive UI |
| Frequency | 3 of 3 attempts |
| Status | Ready for triage |

## Environment

- Responsive web
- Chrome device emulation
- Viewport: 320 × 568
- Browser zoom: 100%
- Cart contains one in-stock item

## Steps to reproduce

1. Open the cart at a `320 × 568` viewport.
2. Scroll to the order summary.
3. Attempt to select **Proceed to checkout**.

## Expected result

The checkout action should remain fully visible and selectable without changing zoom or orientation.

## Actual result

The sticky promotional footer overlaps the lower portion of the checkout action. Selecting the visible edge activates the footer link instead of checkout.

## Impact

Customers using narrow mobile screens can be blocked from starting checkout or can be sent to an unrelated page.

## Severity and priority reasoning

**High severity:** the defect can block a revenue-critical workflow for an affected viewport.

**High priority:** the overlap should be corrected before the next responsive layout release.

## Evidence

- Screenshot: complete viewport showing the overlap
- Video: tap attempt opening the promotional destination
- Suggested folder: `evidence/BR-005/`
- DOM note: record the footer and checkout element stacking values during investigation

## Retest criteria

Check widths from 320px through 480px, portrait and landscape orientation, 200% zoom and browser back navigation. Confirm the correct action receives the tap.
