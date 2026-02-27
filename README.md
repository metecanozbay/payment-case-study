# 3D Secure Flow Modeling – Business Analyst Perspective

This repository presents a structured modeling of a 3D Secure (3DS) flow
from a Business Analyst perspective.

The purpose of this project is to demonstrate how authentication logic,
business rules, and transaction state transitions can be clearly defined
and separated within a payment system.

This is not a coding project.
It focuses on business rule modeling and system behavior analysis.

---

## Case 1 – 3DS Business Rules

This case defines the core business rules behind 3DS authentication.

Scope:

- Mandatory vs risk-based 3DS
- SUCCESS / FAIL / TIMEOUT outcomes
- Authentication decision logic
- Edge case handling
- Clear separation from authorization layer

Why this matters:

3DS authentication result should not directly determine
the final transaction outcome without structured logic.

Related document:
`docs/01-3ds-business-rules.md`

---

## Case 2 – Authorization Interaction (Contextual Layer)

Although the main focus is 3DS,
authorization behavior is considered as a dependent layer.

Scope:

- Approved / Declined responses
- Timeout / unknown scenarios
- Interaction with 3DS result

Why this matters:

Authentication and authorization are separate domains.
Understanding their interaction prevents incorrect status mapping.

Related document:
`docs/02-authorization-flow.md`

---

## Case 3 – Transaction State Machine

This case models how a transaction moves between states
after 3DS authentication.

Scope:

- Initial transaction creation
- 3DS result transition
- Authorization transition
- Final states (APPROVED / DECLINED / FAILED)

Why this matters:

A clear state machine:

- Prevents inconsistent updates
- Improves traceability
- Simplifies debugging

Related document:
`docs/03-transaction-state-machine.md`

---

## Case 4 – ER Model & Data Perspective

This case focuses on the data structure supporting the 3DS flow.

Scope:

- Transaction entity
- 3DS result entity
- Authorization result entity
- Relationship modeling

Why this matters:

Data modeling ensures:

- Consistent tracking
- Accurate reporting
- Clear separation of authentication and authorization data

Related document:
`docs/04-er-model.md`

---

## Purpose of This Project

This repository is created as a portfolio case study
to demonstrate structured 3DS analysis from a Business Analyst perspective.

The project intentionally focuses on clarity,
rule definition, and system modeling.
