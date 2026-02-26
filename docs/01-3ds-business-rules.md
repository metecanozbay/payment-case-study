# 3DS Business Rules

## Scope

This document defines the main business rules for the 3D Secure (3DS) flow in an e-commerce card payment process.

---

## Decision Rules

### BR-01 – Mandatory 3DS

IF (merchant.3ds_required = true)  
THEN the transaction must be redirected to the 3DS flow.

---

### BR-02 – Risk-Based 3DS

IF (merchant.3ds_optional = true AND risk_score >= threshold)  
THEN the transaction must be redirected to the 3DS flow.

---

### BR-03 – 3DS Result Logic (XOR)

The 3DS result can be only one of the following:

- SUCCESS
- FAIL
- TIMEOUT / UNKNOWN

Only one status can be valid at a time.

---

### BR-04 – Successful 3DS

IF (3ds_status = SUCCESS)  
THEN the transaction proceeds to the Authorization stage.

---

### BR-05 – Failed 3DS

IF (3ds_status = FAIL)  
THEN transaction.status = DECLINED  
AND decline_reason = "3DS_FAILED"

---

### BR-06 – Timeout or Unknown Result

IF (3ds_status = TIMEOUT OR 3ds_status = UNKNOWN)  
THEN transaction.status = PENDING_REVIEW  
AND operational review may be required.
