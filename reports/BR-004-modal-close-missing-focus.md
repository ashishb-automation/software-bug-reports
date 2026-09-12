# BR-004: Modal close control has no visible keyboard focus

| Field | Value |
| --- | --- |
| Area | Account settings modal |
| Severity | Medium |
| Priority | High |
| Type | Accessibility / keyboard navigation |
| Frequency | 3 of 3 attempts |
| Status | Ready for triage |

## Environment

- Desktop web
- Chrome
- Windows 11
- Keyboard-only navigation
- 100% browser zoom

## Preconditions

The account settings modal is open.

## Steps to reproduce

1. Use `Tab` to move through the modal controls.
2. Continue until focus reaches the close control.
3. Observe the control without using the mouse.

## Expected result

The focused close control should have a clearly visible indicator with sufficient contrast. Its accessible name should describe the action.

## Actual result

Keyboard focus reaches the control, but there is no visible focus indicator. The icon is announced only as “button” by the screen reader.

## Impact

Keyboard and screen-reader users may not know where focus is or what the control does, making the modal harder to dismiss independently.

## Severity and priority reasoning

**Medium severity:** the workflow remains possible, but an important control is difficult to identify for assistive-technology users.

**High priority:** this is an accessibility barrier in a shared component and may affect every modal using the same control.

## Evidence

- Screenshot: focused close control with focus outline absent
- Keyboard recording: tab order from modal heading to close control
- Accessibility-tree capture: button without an accessible name
- Suggested folder: `evidence/BR-004/`

## Retest criteria

Confirm a visible focus style at 100%, 200% and high-contrast settings. Verify the accessible name in Chrome and Firefox with keyboard and screen-reader checks.
