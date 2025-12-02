# ADR 003: Backend Framework Choice

## Status
Accepted

## Context
The CMS backend needs security, routing, validation, RBAC, and quick development for the PoC.

## Decision
Use **Laravel (PHP)** as the primary backend framework.

## Alternatives
- **Node.js/Express** – lightweight but requires writing many features manually.
- **Django** – full-featured but not aligned with existing project structure.

## Consequences
- Faster development due to Laravel’s built-in tooling.
- Built-in features (auth, CSRF, ORM) reduce risk and boilerplate.
- Aligns well with the layered architecture in the C4 diagrams.
