# BR-001: Cart retains an item when quantity is changed to zero

| Field | Value |
| --- | --- |
| Area | Shopping cart |
| Severity | High |
| Priority | High |
| Type | Functional / data validation |
| Frequency | 3 of 3 attempts |
| Status | Ready for triage |

## Environment

- Desktop web
- Chrome 153
- macOS
- Signed-in test customer
- Test data: one in-stock product

## Preconditions

The customer has one product in the cart and the cart page is open.

## Steps to reproduce

1. Select the quantity field for the cart item.
2. Replace the current value with `0`.
3. Select **Update cart**.
4. Refresh the page.

## Expected result

The application should either remove the item or reject zero with a clear validation message. The cart total and item count should remain consistent.

## Actual result

The item remains visible with a quantity of zero. The header still shows one cart item, while the order total is displayed as zero.

## Impact

The customer receives conflicting cart information and may believe the product is still part of the order. Any downstream service that assumes quantity is at least one could also receive invalid cart data.

## Severity and priority reasoning

**High severity:** the cart enters an invalid business state and displays inconsistent totals.

**High priority:** the problem affects a core purchase path and should be addressed before changes to checkout are released.

## Evidence

- Screenshot to capture: full cart showing quantity, header count and total
- Suggested filename: `evidence/BR-001/cart-zero-quantity.png`
- Console errors: none observed
- Network note: capture the update-cart request payload during retest

## Retest criteria

Verify values `0`, `-1`, blank text and a valid positive quantity. Confirm the UI message, cart count, total and update request remain consistent.
