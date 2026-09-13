# Test Plan — SauceDemo E-Commerce Application

**Project:** Enterprise Web App QA Suite (Phase 1 — Manual Testing)
**Target Application:** https://www.saucedemo.com
**Author:** Athiradh KP
**Date:** [fill in]

## 1. Introduction
This test plan covers manual functional, boundary, negative, and usability testing of
SauceDemo, a sample e-commerce web application used for QA practice. Testing focuses
on the core purchase flow: authentication, product browsing, cart management, and
checkout.

## 2. Scope

### In Scope
- Login / Authentication (including SauceDemo's special test accounts)
- Product Catalog (listing, sorting, product detail view)
- Shopping Cart (add/remove items, cart persistence)
- Checkout Flow (customer info form, order overview, order confirmation)
- Boundary and negative input handling across the above

### Out of Scope
- Backend/database verification (no accessible backend on the public demo —
  planned as a separate phase against a self-hosted environment)
- Performance/load testing
- Cross-browser/cross-device compatibility (single-browser testing only for this phase)
- Payment gateway integration testing (checkout is simulated, no real payment processor)

## 3. Test Objectives
- Verify core purchase flow works end-to-end for a standard user
- Verify the application behaves correctly under invalid/boundary input
- Identify and document any functional defects, using SauceDemo's intentionally
  seeded problem accounts as part of the process
- Produce a traceable, reviewable record of test coverage (Test Matrix) and findings
  (Jira bug tickets)

## 4. Test Types
| Type | Purpose |
|---|---|
| Functional | Core flows work as expected for valid input |
| Boundary | Behavior at the edges of valid input (max length, min/max quantities) |
| Negative | Behavior under invalid input (empty required fields, malformed data) |
| Usability | Basic clarity of error messages, navigation, and feedback to the user |

## 5. Test Environment
- **Application URL:** https://www.saucedemo.com
- **Browser:** [state which browser/version you test in]
- **Test Accounts:**
  - `standard_user` / `secret_sauce` — baseline working account
  - `locked_out_user` / `secret_sauce` — should be blocked at login
  - `problem_user` / `secret_sauce` — has known UI defects (useful for negative/usability findings)
  - `performance_glitch_user` / `secret_sauce` — simulates slow responses

## 6. Entry Criteria
- Application is reachable at the URL above
- All listed test accounts are confirmed to exist and be usable
- Test Matrix (test case spreadsheet) is drafted and reviewed before execution begins

## 7. Exit Criteria
- 100% of planned test cases in the Test Matrix have been executed at least once
- All identified defects are logged in Jira with severity/priority assigned
- No open P1 (blocker) defects remain undocumented

## 8. Roles
- Test design, execution, and defect logging: Athiradh KP (self-directed portfolio project)

## 9. Deliverables
- This Test Plan
- Test Matrix (30–35 test cases, spreadsheet)
- Jira bug tickets (4–6, with repro steps, severity/priority, screenshots)
- (Phase 2, pending environment setup) SQL data-integrity checks against a
  self-hosted OrangeHRM instance
