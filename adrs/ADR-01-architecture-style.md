# ADR 001:Architecture Style

## Status
Accepted

## Context
The CMS must support millions of users, multiple organisations, and future features such as chatbot integration. The system also needs to remain manageable for the Proof of Concept.

## Decision
Adopt a **hybrid architecture**: a layered monolith for core logic, supported by two independent microservices (Notifications and Reporting).

## Alternatives
- **Full Monolith** – simple, but limits long-term scalability and extension.
- **Full Microservices** – scalable, but too complex for early development, increases operational overhead.

## Consequences
- Core system remains simple and maintainable.
- High-load features can scale independently.
- Architecture remains flexible for future features.
