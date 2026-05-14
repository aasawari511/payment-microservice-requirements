# Transaction Status Tracking

**ID:** A1-D7729E  
**Status:** draft  
**Priority:** 1  

## Actors

- Internal backend services
- merchant partners
- admin teams

## Overview

The system shall provide real-time access to transaction status information through RESTful endpoints. It shall maintain consistent status updates and enable querying of transaction states across all lifecycle stages.

## Functional Requirements

1. System shall accept GET requests to /payments/{id}/status with transaction identifier
2. System shall return current transaction status including authorization, capture, and refund states
3. System shall provide status updates for all transaction lifecycle events
4. System shall maintain historical status change logs for audit purposes
5. System shall support filtering of transactions by status for reporting purposes

## Non-Functional Requirements

1. API response time < 100 ms at p99 under 1 000 concurrent users
2. 99.99% availability SLA for status queries