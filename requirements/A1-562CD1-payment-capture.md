# Payment Capture

**ID:** A1-562CD1  
**Status:** draft  
**Priority:** 1  

## Actors

- Internal backend services
- merchant partners

## Overview

The system shall process payment captures by validating capture requests, communicating with external payment providers, and updating transaction statuses accordingly. It shall ensure capture operations are only performed on previously authorized transactions.

## Functional Requirements

1. System shall accept POST requests to /payments/capture with transaction identifier and optional capture amount
2. System shall validate capture requests against existing authorization records and capture limits
3. System shall communicate with external payment provider (Stripe) to execute capture operation
4. System shall update transaction status to captured upon successful capture
5. System shall reject capture requests for unauthorized or already-captured transactions

## Non-Functional Requirements

1. API response time < 500 ms at p99 under 1 000 concurrent users
2. 99.9% availability SLA for capture operations