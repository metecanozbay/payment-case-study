# payment-case-study

Payment domain focused Business Analysis mini-case studies.

This repository contains conceptual BA case studies related to card payment flows, including 3D Secure (3DS) and Authorization processes.

---

## Experience Context

I have around 4 years of hands-on experience in card processing and payment operations.

During this period, I worked on card transaction flows, operational processes, and system integrations.  
This repository reflects my effort to translate that practical experience into structured Business Analysis artifacts.

---

## Conceptual Case Study Note

This repository presents a conceptual Business Analysis case study.

The flows and business rules are modeled based on:

- EMVCo 3DS 2.x principles  
- ISO 8583 authorization response logic  
- Publicly available Visa and Mastercard documentation  

This work does not represent any specific institution or production system.

---

## Case 1 – 3D Secure (3DS)

Medium article:  
https://medium.com/@metecanozbay/3d-secureun-görünmeyen-dünyasına-kısa-bir-yolculuk-5d816dcabe1d

### Scope of this case:

- 3DS decision logic (XOR / OR)
- Success / failure / timeout scenarios
- Business rules definition
- Edge-case considerations
- Transition to authorization

---

## Case 2 – Authorization Flow

This case models the authorization stage after 3DS validation.

Covered topics:

- Authorization response handling
- Success and decline logic
- Timeout and unknown state handling
- Retry concept (conceptual)
- Basic state transition thinking

---

## Purpose

To demonstrate how hands-on payment operations experience can be structured and expressed using Business Analysis methodology.
