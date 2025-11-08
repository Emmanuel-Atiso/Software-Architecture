# ADR-01 – Architecture Style: Modular Monolith

**Status:** Accepted  
**Date:** 2025-11-08

## Context
We must deliver a coherent CMS design and PoC quickly, while maintaining separation of concerns and tenant isolation.

## Decision
Adopt a **modular monolith**: clear modules (Complaint, Workflow, Notification, Auth) behind a single Laravel app/API.

## Alternatives
- Microservices now (higher infra/ops overhead, complexity).
- Layered monolith with weak boundaries (risk of tight coupling).

## Consequences
✅ Simple deployment and testing; fewer moving parts.  
⚠️ We must enforce module boundaries via folder structure, service/repository layers, and code review.

## Follow-ups
Document module boundaries in the repo and reflect them in C4 L3/L4.
