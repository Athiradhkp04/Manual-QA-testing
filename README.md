# Manual QA Test Suite — SauceDemo

Manual functional, boundary, negative, and usability testing of
[SauceDemo](https://www.saucedemo.com), a sample e-commerce application used
for QA practice.

## Contents
- [`test-plan-saucedemo.md`](./test-plan-saucedemo.md) — scope, test types,
  entry/exit criteria
- [`test-matrix-saucedemo.xlsx`](./test-matrix-saucedemo.xlsx) — 35 executed
  test cases across Auth, Product Catalog, Cart, Checkout, and
  Boundary/Security modules
- [`defects/`](./defects) — 4 defect reports (1 functional defect, 3
  data-quality/usability findings), written in Jira-ticket format

## Results Summary
- 35 test cases executed
- 34 Passed / 1 Failed
- 4 defects logged, with reproduction steps, expected vs. actual results,
  and severity/priority

## What This Demonstrates
- Test Plan authoring: scope definition, entry/exit criteria
- Structured test case design across functional, boundary, and negative
  categories
- Manual test execution with documented, specific actual results (not just
  pass/fail)
- Defect reporting with clear reproduction steps and calibrated severity —
  including distinguishing a genuine functional defect from lower-severity
  data-quality/usability findings

## Scope Note
This phase covers manual UI-level testing only. A planned second phase
(automated regression via Selenium/Playwright and backend SQL data-integrity
checks against a self-hosted OrangeHRM instance) is scoped but not yet
started, pending local environment setup.
