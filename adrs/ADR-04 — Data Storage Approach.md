# ADR-004: Relational Database for Complaint Data

## Status
Accepted

## Context
The CMS must store structured data such as users, complaints, statuses, and resolution notes in a secure and consistent manner.

## Decision
A relational database was selected to store all CMS data.

## Alternatives Considered
- NoSQL database: Rejected due to weaker support for relational data and transactions.
- File-based storage: Rejected due to scalability and security limitations.

## Consequences
Relational storage ensures data integrity, supports reporting, and aligns with the system’s data model and future scalability needs.
