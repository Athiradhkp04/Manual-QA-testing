# BUG-004: Noticeably degraded page load time for performance_glitch_user

**Reporter:** Athiradh KP
**Environment:** https://www.saucedemo.com (Chrome, desktop)
**Test Case Reference:** TC-035
**Severity:** Low (P3) — usability/performance observation, not a functional break
**Priority:** P3
**Status:** Open

## Steps to Reproduce
1. Go to https://www.saucedemo.com
2. Log in with username `performance_glitch_user`, password `secret_sauce`
3. Observe load time of the Products (inventory) page compared to logging in
   as `standard_user`

## Expected Result
Page load time should be broadly consistent with the `standard_user`
account, within normal variance.

## Actual Result
The Products page load is noticeably delayed by several seconds compared to
`standard_user`, under otherwise identical conditions (same browser,
network, and action sequence).

## Notes
This account is intentionally seeded by SauceDemo to simulate a performance
issue for QA practice purposes. Logged here as a usability concern — a
multi-second delay on a core landing page would be a real user-experience
issue in a production application, even without any functional error.
