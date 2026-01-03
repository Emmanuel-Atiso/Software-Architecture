# ADR-005: Web-Based Role-Specific User Interface

## Status
Accepted

## Context
Users interact with the CMS through different roles, each requiring tailored views and actions.

## Decision
A single web interface was designed with role-based views, where content and actions change depending on the user’s role.

## Alternatives Considered
- Separate applications per role: Rejected due to duplication and maintenance overhead.
- CLI-based interface: Rejected due to poor usability.

## Consequences
This approach improves usability, supports accessibility standards, and simplifies maintenance while still meeting diverse user needs.
