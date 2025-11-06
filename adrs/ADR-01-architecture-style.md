# ADR-01 – Architecture Style (Modular Monolith)

**Status:** Accepted  
**Date:** 2025-11-06  

## Context
Need rapid delivery with clear boundaries and tenant isolation.

## Decision
Adopt modular monolith (Complaint, Workflow, Notification, Auth modules) behind a single REST interface.

## Alternatives
- Microservices (too much overhead for PoC)
- Layered monolith (risk of coupling)

## Consequences
✅ Simple deploy and testing  
⚠️ Must enforce boundaries with reviews/linting  


