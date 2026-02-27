# Case 5 – 3DS Risk-Based Strategy Decision Framework

## Overview

This case focuses on the strategic decision behind 3D Secure enforcement.

Instead of modeling authentication rules,
this document analyzes when 3DS should be mandatory
and when risk-based triggering may be more appropriate.

The objective is to balance fraud risk and conversion rate.

---

## 1. Current State Analysis

In the current scenario:

- 3DS is applied to all transactions
- No risk segmentation is used
- All customers go through authentication

Observed impact:

- Increased checkout friction
- Higher cart abandonment rate
- Customer dissatisfaction

Fraud rate is low, but conversion loss is increasing.

---

## 2. Problem Statement

Applying 3DS to every transaction may reduce fraud,
but it also negatively impacts user experience and revenue.

Key question:

Should 3DS be mandatory for all transactions,
or should it be triggered based on risk?

---

## 3. Risk-Based Strategy Approach

A risk-based 3DS strategy introduces segmentation.

Example risk indicators:

- High transaction amount
- New customer
- High-risk BIN
- Suspicious IP address
- Cross-border transaction

Low-risk transactions may bypass 3DS (frictionless),
while high-risk transactions require authentication.

---

## 4. Future State Definition

Proposed model:

- Low risk → Frictionless flow
- Medium risk → Optional challenge
- High risk → Mandatory 3DS challenge

This approach aims to:

- Protect against fraud
- Improve conversion rate
- Reduce unnecessary friction

---

## 5. Risk Assessment

Potential risks of risk-based strategy:

- Increased fraud exposure if thresholds are misconfigured
- Regulatory constraints in certain regions
- Merchant liability considerations

Mitigation:

- Continuous monitoring
- Threshold adjustment
- Fraud KPI tracking

---

## 6. Business Impact Evaluation

Expected outcomes:

- Higher approval rate
- Lower abandonment rate
- Balanced fraud ratio
- Improved customer experience

---

## Conclusion

3DS enforcement is not only a technical decision.
It is a strategic trade-off between security and conversion.

A structured risk-based framework allows
data-driven decision making in payment systems.
