# Test — Contradiction detection

## Input history

The user repeatedly says the product should be sold quickly.

Over several iterations, the product expands to include:

- CRM
- inventory
- finance
- logistics
- OCR
- payroll
- dashboards
- workflow
- supplier management

## Expected behavior

Detect tension between speed-to-market and expanding scope.

Do not automatically declare either side wrong.

Ask a question that exposes the underlying product choice.

## Failure conditions

- merely says "the product is complex"
- gives a long implementation plan
- assumes the user must remove features
