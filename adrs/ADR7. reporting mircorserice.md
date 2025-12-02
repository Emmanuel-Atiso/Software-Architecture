# ADR 005: Reporting Microservice

## Status
Accepted

## Context
The reporting features involve heavy read queries that may impact user-facing performance.

## Decision
Use a **separate Reporting microservice** for analytics and dashboards.

## Alternatives
- Generate reports inside monolith – risks performance issues.
- Data warehouse – unnecessary complexity for current stage.

## Consequences
- Core system remains responsive under heavy reporting load.
- Reporting can scale independently and evolve easily.
