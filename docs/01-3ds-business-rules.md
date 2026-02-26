# 3DS Business Rules

## Scope

Bu doküman, e-commerce kartlı ödeme sürecinde 3D Secure (3DS) akışına ilişkin temel iş kurallarını tanımlar.

---

## Decision Rules

### BR-01 – 3DS Zorunluluğu

IF (merchant.3ds_required = true)  
THEN işlem 3DS akışına yönlendirilir.

---

### BR-02 – Risk Bazlı 3DS

IF (merchant.3ds_optional = true AND risk_score >= threshold)  
THEN işlem 3DS akışına yönlendirilir.

---

### BR-03 – 3DS Sonuç Mantığı (XOR)

3DS sonucu aşağıdakilerden yalnızca biri olabilir:

- SUCCESS
- FAIL
- TIMEOUT / UNKNOWN

---

### BR-04 – Başarılı 3DS

IF (3ds_status = SUCCESS)  
THEN işlem Authorization sürecine geçer.

---

### BR-05 – Başarısız 3DS

IF (3ds_status = FAIL)  
THEN transaction.status = DECLINED  
AND decline_reason = "3DS_FAILED"

---

### BR-06 – Timeout Durumu

IF (3ds_status = TIMEOUT)  
THEN transaction.status = PENDING_REVIEW  
AND operasyonel kontrol ihtiyacı oluşur.
