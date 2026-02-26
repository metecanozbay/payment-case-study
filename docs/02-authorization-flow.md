# Authorization Flow

## Scope

This document describes the conceptual authorization stage in a card payment process after 3DS validation (if applicable).

This is an industry-aligned conceptual model based on common payment processing patterns.

---

## High-Level Flow

1. Transaction is sent to the payment gateway.
2. Gateway forwards the request to the acquirer.
3. Acquirer routes the request through the card network.
4. Issuer evaluates the transaction.
5. Authorization response is returned.

---

## Decision Logic

### AR-01 – Approved Authorization

IF (response_code = "00")  
THEN transaction.status = AUTHORIZED

---

### AR-02 – Declined Authorization

IF (response_code != "00")  
THEN transaction.status = DECLINED

---

### AR-03 – Timeout or No Final Response

IF (no response received within defined time limit)  
THEN transaction.status = UNKNOWN

UNKNOWN status may require further verification (reconciliation process).

---

## Conceptual Considerations

- Authorization and settlement are separate stages.
- AUTHORIZED status does not guarantee settlement.
- UNKNOWN state represents uncertainty and must be handled carefully.
