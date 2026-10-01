# Lab 19 — Choose the Test Database Strategy

## Pick One
Use an **in‑memory test database** (H2 or similar) that Spring Boot can auto‑configure for integration tests. It keeps tests fast, isolated, and repeatable.

## Same Engine
Match the **SQL dialect and schema behavior** of production as closely as possible. Even if the engine differs, align naming, constraints, and migrations so logic behaves the same.

## Isolation
Each test should run with a **fresh schema** and no leftover rows. Use transactional rollback or schema‑reset so tests never influence each other.

## Seed Data
Load only **minimal fixtures** required for the slice tests — typically via migrations or test‑specific SQL scripts. Avoid large datasets; keep it focused on the contract.

## Scope
Pre-lab only — do not finish the full lab in this exercise.
