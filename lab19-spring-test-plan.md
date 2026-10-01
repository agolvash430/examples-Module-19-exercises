# Lab 19 — Plan the Spring Integration Tests

## Slice Choice
Use a **web + service + repository** slice wired through Spring Boot’s test context, but with external systems (DB, HTTP clients) replaced by in‑memory or test doubles. This keeps the test realistic without pulling in the full environment.

## Two Cases
1. **Happy path GET** — request an existing customer ID and verify the controller → service → repository chain returns the correct DTO and status.  
2. **Create flow** — POST a valid new customer and confirm persistence, mapping, and returned status/URI.

## What It Proves
It demonstrates that Spring wiring, JSON binding, validation, and repository interaction all behave correctly together. It proves the contract, the HTTP shape, and the real collaboration across layers.

## Context Cost
Higher than unit tests because Spring must start a slice of the application context, but far cheaper than full end‑to‑end tests. Startup time is moderate; execution is still fast enough for iterative development.

## Scope
Pre-lab only — do not finish the full lab in this exercise.
