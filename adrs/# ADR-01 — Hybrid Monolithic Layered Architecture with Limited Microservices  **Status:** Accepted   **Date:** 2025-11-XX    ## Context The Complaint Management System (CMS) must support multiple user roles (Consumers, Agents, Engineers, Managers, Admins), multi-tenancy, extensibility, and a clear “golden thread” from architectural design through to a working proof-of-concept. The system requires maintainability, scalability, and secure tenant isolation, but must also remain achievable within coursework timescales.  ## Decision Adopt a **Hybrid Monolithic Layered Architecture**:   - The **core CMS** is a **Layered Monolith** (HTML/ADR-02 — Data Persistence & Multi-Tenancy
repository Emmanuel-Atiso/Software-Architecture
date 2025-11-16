# ADR-02 — Data Persistence and Multi-Tenancy Strategy

**Status:** Accepted  
**Date:** 2025-11-XX  

## Context
The CMS must support multiple organisations (tenants) without data leakage. The solution must be easy to implement for a PoC but also adaptable for future enterprise-scale expansion.

## Decision
Use **MySQL** with **`tenant_id` on all tables** (Complaints, Users, Feedback, Organisations, Roles).  
Tenant isolation is enforced in:  
- PHP controllers (per-request tenant check)  
- Repository/DAO layer (automatic tenant filtering)  
- Database constraints (unique keys combined with tenant_id)

**Compound indexes:** `(tenant_id, created_at)`, `(tenant_id, ticket_number)`  
**Future option:** database-per-tenant if scale or compliance requires stronger isolation.

## Consequences
+ Simple to implement; good performance for joins and reporting.  
+ Strong logical isolation; consistent with monolith + microservices hybrid.  
− Not physical isolation; must rely on strict validation and tenant checks.

## Alternatives Considered
- **Database-per-tenant:** best isolation, more operational overhead.  
- **PostgreSQL row-level security:** elegant but changes chosen tech stack.

## References
C4 L2; Data Model; Security View; ADR-04
