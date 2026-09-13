# BUG-002: No maximum length validation on First Name field during checkout

**Reporter:** Athiradh KP
**Environment:** https://www.saucedemo.com (Chrome, desktop)
**Test Case Reference:** TC-031
**Severity:** Low (P3) — data quality/usability finding, no crash or functional break
**Priority:** P3
**Status:** Open

## Steps to Reproduce
1. Log in as `standard_user`, add any item to cart, proceed to Checkout: Your Information
2. Enter a string of 200+ characters into the First Name field
3. Fill remaining required fields and click Continue

## Expected Result
The field either enforces a reasonable maximum length (rejecting or truncating
excessively long input) or displays a validation message.

## Actual Result
The application accepts the full 200+ character string with no truncation,
no error message, and no crash. Checkout proceeds normally with the
oversized value carried through to the order overview.

## Notes
Not a functional blocker, but flagged as a data-quality gap: unbounded text
input on a name field is a common source of downstream display/storage
issues in real systems (e.g. layout breakage or database column overflow
if this were a persisted production system).
