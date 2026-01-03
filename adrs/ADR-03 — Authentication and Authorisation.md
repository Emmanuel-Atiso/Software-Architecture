# ADR-003: Role-Based Access Control (RBAC)

## Status
Accepted

## Context
Different users (consumers, agents, managers, administrators) require different permissions within the CMS.

## Decision
Role-Based Access Control (RBAC) was implemented to restrict system actions based on user roles.

## Alternatives Considered
- Single user role for all users: Rejected due to security and usability risks.
- Attribute-based access control (ABAC): Rejected due to complexity beyond the proof-of-concept scope.

## Consequences
RBAC improves security and ensures users only access features relevant to their role. It is simple to implement and aligns with the system’s functional requirements.
