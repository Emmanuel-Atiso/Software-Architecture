# ADR-01 — Hybrid Monolithic Layered Architecture with Limited Microservices

**Status:** Accepted  
**Date:** 2025-11-XX  

## Context
The Complaint Management System (CMS) must support multiple user roles (Consumers, Agents, Engineers, Managers, Admins), multi-tenancy, extensibility, and a clear “golden thread” from architectural design through to a working proof-of-concept. The system requires maintainability, scalability, and secure tenant isolation, but must also remain achievable within coursework timescales.

## Decision
Adopt a **Hybrid Monolithic Layered Architecture**:  
- The **core CMS** is a **Layered Monolith** (HTML/JS → PHP → Domain Modules → MySQL).  
- Two high-change components — **Notification Service** and **Reporting Service** — are implemented as **independent microservices** communicating with the monolith via REST APIs.

## Consequences
**Positive:**  
- Clear separation of concerns within the monolith (Presentation, Application, Domain, Data).  
- High-change modules can be deployed, scaled, and updated independently.  
- Less operational complexity than full microservices.  
- Ideal for evolving over time (“monolith-first then extract”).  

**Negative:**  
- Some complexity added by managing two auxiliary services.  
- Still need careful boundaries inside the monolith to avoid tight coupling.

## Alternatives Considered
- **Pure Monolithic Layered Architecture:** simple but less scalable and harder to evolve.  
- **Full Microservices Architecture:** highly scalable but too complex for proof-of-concept scope.

## References
§2.1 Architectural Style; C4 L1 & L2; ADR-02..05
