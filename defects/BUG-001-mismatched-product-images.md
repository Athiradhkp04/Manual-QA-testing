# BUG-001: Incorrect product images displayed for problem_user account

**Reporter:** Athiradh KP
**Environment:** https://www.saucedemo.com (Chrome, desktop)
**Test Case Reference:** TC-014
**Severity:** Medium (P2) — visual/functional defect, does not block core purchase flow
**Priority:** P2
**Status:** Open

## Steps to Reproduce
1. Go to https://www.saucedemo.com
2. Log in with username `problem_user`, password `secret_sauce`
3. Observe the product list (Products page)

## Expected Result
Each of the 6 products displays its own correct, unique product image, matching
the images shown when logged in as `standard_user`.

## Actual Result
Login succeeds (the account is not locked out — this was confirmed directly,
ruling out an auth-related cause). However, all 6 products display the same
incorrect/mismatched product image instead of their individual correct images.

## Notes
This is a genuine UI rendering defect specific to the `problem_user` account —
SauceDemo intentionally seeds this account with known bugs for QA practice
purposes, so this finding is expected to exist by design, but is documented
here exactly as it would be for a real defect.

## Evidence
Screenshot: [attach screenshot of product list under problem_user]
