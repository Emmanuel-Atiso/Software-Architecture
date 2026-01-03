# ADR-006: Use PHP for Backend API Implementation

## Status
Accepted

## Context
The proof of concept requires a backend service to handle complaint workflows (log complaint, assign, update status, add resolution notes) and expose these via a web interface/API.

## Decision
PHP was selected to implement the backend application logic and API endpoints. The backend follows a layered structure (controllers/services/repositories) and communicates with the relational database using PDO.

## Alternatives Considered
- Node.js/Express: Rejected to keep the implementation aligned with the chosen stack and existing familiarity.
- Java/Spring Boot: Rejected due to higher setup and boilerplate overhead for the proof of concept.
- Python/Django: Rejected to avoid switching stacks and to keep implementation consistent with PHP tooling.

## Consequences
PHP enables fast development and has mature support for database access and web apps. The trade-off is that strict architectural enforcement relies on project structure and conventions, but this is manageable for the proof of concept and well supported through a layered layout.
