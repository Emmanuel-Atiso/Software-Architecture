# ADR-001: Use of Layered Monolithic Architecture

## Status
Accepted

## Context
The Complaint Management System (CMS) is being developed as a proof of concept with limited time and scope. The system must be easy to understand, implement, and demonstrate, while still supporting future scalability.

## Decision
A layered monolithic architecture was chosen, separating the system into presentation, application, and data layers.

## Alternatives Considered
- Microservices architecture: Rejected due to added complexity and deployment overhead for a proof of concept.
- Serverless architecture: Rejected due to reduced control over application flow and increased architectural complexity.

## Consequences
The system is simpler to develop and test, with clear separation of concerns. While less scalable than microservices, it is suitable for a proof of concept and can be refactored in the future.
