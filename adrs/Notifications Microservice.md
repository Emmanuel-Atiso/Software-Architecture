# ADR-05 — Notifications Microservice

**Status:** Accepted  
**Date:** 2025-11-XX  

## Context
Notifications (email/SMS) must not slow down or block the monolith. They are high-change and likely to grow in complexity over time (templates, retries, tracking).

## Decision
Implement a **Notification microservice** separate from the monolith.  
Monolith writes a "notification job" (HTTP POST with message payload).  
Microservice sends the email/SMS via a provider (e.g., SendGrid/Twilio).  
Supports asynchronous execution through optional job queue/cron.

## Consequences
+ Independent scaling for high-volume notifications.  
+ Microservice can be updated without redeploying the core CMS.  
+ Cleaner separation of concerns.  
− Requires maintaining a second deployable unit.

## Alternatives Considered
- **Synchronous calls inside monolith:** simple but slow/blocking.  
- **Full event-driven architecture:** flexible but unnecessary overhead for PoC.

## References
C4 L2; Sequence Diagram (Resolve/Notify)
