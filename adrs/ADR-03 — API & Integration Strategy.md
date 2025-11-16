# ADR-03 — API and Integration Strategy

**Status:** Accepted  
**Date:** 2025-11-XX  

## Context
The monolith communicates with internal modules and external microservices. The system requires predictable integration points for the UI, a future chatbot, and reporting/notification services.

## Decision
Use **REST-style HTTP endpoints** from the PHP monolith.  
- UI: AJAX/Fetch calls returning JSON.  
- Microservices: communicate with the monolith and each other via REST.  
- Notifications/Reporting: exposed as REST endpoints, triggered by the monolith.

## Consequences
+ Predictable, simple, and well-understood pattern.  
+ Easy to test using Postman/Selenium.  
+ Supports future integrations (mobile app, chatbot).  
− Less flexible query patterns than GraphQL (not needed for PoC).

## Alternatives Considered
- **GraphQL:** powerful but unnecessary for CMS complexity.  
- **Server-side rendering only:** restricts reuse and extensibility.

## References
C4 L2 & L3; api.yaml; ADR-01, ADR-05
