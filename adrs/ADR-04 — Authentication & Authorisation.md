# ADR-04 — Authentication and Authorisation

**Status:** Accepted  
**Date:** 2025-11-XX  

## Context
The CMS includes several roles with varying permissions and must support multi-tenant access control. The PoC must be achievable without full IdP/SSO integration.

## Decision
Use **session-based authentication** (PHP sessions; secure cookies) for the PoC.  
Apply **RBAC** with roles: Consumer, Agent, Engineer, Manager, Admin.  
Every request enforces:  
1. user authenticated  
2. user has appropriate role  
3. request belongs to the correct tenant (`tenant_id`)  

Path to future upgrade: integrate **OIDC/JWT** with an external Identity Provider for SSO.

## Consequences
+ Fast and simple to implement for PoC.  
+ Strong role and tenant enforcement inside application layer.  
− SSO not available in PoC unless implemented later.

## Alternatives Considered
- **Immediate OIDC/JWT:** secure, scalable, but more complex.  
- **Basic Auth:** insecure → rejected.

## References
Security View; C4 L2; ADR-01, ADR-02
