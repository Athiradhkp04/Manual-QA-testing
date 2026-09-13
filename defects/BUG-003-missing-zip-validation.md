# BUG-003: No format validation on Zip/Postal Code field during checkout

**Reporter:** Athiradh KP
**Environment:** https://www.saucedemo.com (Chrome, desktop)
**Test Case Reference:** TC-032
**Severity:** Low (P3) — data quality/usability finding, no crash or functional break
**Priority:** P3
**Status:** Open

## Steps to Reproduce
1. Log in as `standard_user`, add any item to cart, proceed to Checkout: Your Information
2. Enter non-numeric text (letters/symbols) into the Zip/Postal Code field
3. Fill remaining required fields and click Continue

## Expected Result
The field validates that input matches a plausible postal code format
(numeric, or a recognized alphanumeric pattern), rejecting clearly invalid
values with a message.

## Actual Result
The application accepts non-numeric text in the Zip/Postal Code field with
no format validation. Checkout proceeds normally, and the invalid value is
carried through to the order overview.

## Notes
Same category of finding as BUG-002 — the field is treated as free text with
no format enforcement. Worth flagging separately since postal code is used
in downstream tax/shipping calculations in most real e-commerce systems,
where invalid formats would cause real functional problems.
