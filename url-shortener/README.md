# URL Shortener System Design

This project presents the **system design** of a scalable and performant URL Shortener service (like TinyURL or Bitly). The goal is to demonstrate high-level and low-level design skills, architechtural decision-making, and readiness for real-world implementation.

> This repo starts with the design documentation and will later be extended to a working backend system.

## Problem Statement

Design a system that:

- Converts long URLs into unique, short aliases.
- Redirects short URLs to the original long URL.
- Optionally supports expiration, analytics and custom aliases.
- It is highly available, low latency, and horizontally scalable.

## Functional Requirements

- `POST /shorten`: Create a short URL for a given long URL.
- `GET /short-code`: Redirect to the original URL
- Expiry: Optional TTL for each short URL.
- Prevent short code reuse immediately after deletion.
- (Optional) Analytics: Track click counts, region, timestamp

## System Design Coverage

| Area               | Status | Description                                            |
| ------------------ | ------ | ------------------------------------------------------ |
| High-Level Desgin  | 🔜     | Components, data flow, scaling                         |
| Low-Level Design   | 🔜     | API Contracts, DB Schema, sequence diagrams            |
| Data Modeling      | 🔜     | URL Mapping, TTL, metadata                             |
| Caching Strategy   | 🔜     | Redis-based Geolocation caching                        |
| Expiry + Cleanup   | 🔜     | Soft Delete + Periodic cleanup or TTL Index            |
| Scaling & Sharding | 🔜     | Geo-distributed cache/db read replicas                 |
| Security Measures  | 🔜     | Rate Limiting, Validation, Short Code reuse protection |

## Repository Structure

```bash
url-shortener/
|-- README.md
|-- hld/            # High-Level Design
|-- lld/            # Low-Level Design
|-- assets/         # Diagrams & Visuals
|-- implementation  # Placeholder for backend code (future)
```
