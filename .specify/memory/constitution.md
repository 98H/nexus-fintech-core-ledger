# Spec Kit Constitution: FinTech Core Ledger

## Product Intent
Double-entry bookkeeping and compliance reporting engine.

## Architectural Invariants
- Zero Blast-Radius: Isolated sandbox execution per task.
- Strict TDD: BDD acceptance tests frozen before code development.
- Clean Code & Deterministic Verification: Sole oracle is test runner exit code == 0.
