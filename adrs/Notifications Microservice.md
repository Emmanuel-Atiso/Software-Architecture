# ADR 004: Notification Microservice

## Status
Accepted

## Context
Notifications generate high load and change more often than core business logic.

## Decision
Implement a small **Notification microservice** (Node.js or Python) communicating via REST.

## Alternatives
- Embed notifications into monolith – simpler but reduces scalability.
- Use message queues – powerful but too heavy for PoC.

## Consequences
- Notification spikes don't slow down the core CMS.
- Microservice can be scaled independently.
- Simple enough for PoC while extendable long-term.
