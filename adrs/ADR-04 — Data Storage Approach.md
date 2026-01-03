# ADR-004: Relational Database for Complaint Data (MySQL + PHP Integration)

## Status
Accepted

## Context
The CMS must store structured data such as users, complaints, statuses, assignment details, and resolution notes. The proof of concept also needs a storage approach that is easy to build quickly, supports consistent relationships between entities, and works reliably with a PHP backend.

## Decision
A relational database was selected as the primary data store for the CMS, implemented using MySQL (or MariaDB). The PHP backend accesses the database using a standard database driver (e.g., PDO) to perform CRUD operations and enforce basic data integrity.

## Alternatives Considered
- NoSQL (e.g., MongoDB): Rejected because the CMS data is highly relational (complaints link to users, statuses, and assignments) and the proof of concept benefits from SQL joins and transactional consistency.
- File-based storage (JSON/CSV): Rejected due to poor scalability, weak concurrency handling, and higher risk of data integrity issues.
- In-memory storage only: Rejected because it does not persist complaint records reliably and is not suitable for demonstrating a realistic CMS lifecycle.

## Consequences
Using a relational database provides strong data consistency, supports reporting queries (e.g., complaints by status, resolution time), and fits the complaint lifecycle model. Integrating MySQL with PHP is widely supported and straightforward, reducing implementation risk for the proof of concept. A trade-off is that schema changes require migrations, but this is manageable at proof-of-concept scale.
