# Transaction State Machine

## Scope

This document defines a conceptual transaction state model for an e-commerce card payment flow.

---

## States

- INITIATED
- 3DS_REQUIRED
- 3DS_SUCCESS
- 3DS_FAILED
- AUTH_IN_PROGRESS
- AUTHORIZED
- DECLINED
- UNKNOWN
- REVERSED

---

## State Flow (High Level)

INITIATED  
→ 3DS_REQUIRED (if 3DS needed)  
→ 3DS_SUCCESS or 3DS_FAILED  
→ AUTH_IN_PROGRESS  
→ AUTHORIZED or DECLINED  

UNKNOWN may occur in case of timeout.
