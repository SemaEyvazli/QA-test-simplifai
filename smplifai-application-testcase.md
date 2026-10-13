# Test Case: Create New Application via API

| Sahə | Məlumat |
| :--- | :--- |
| **Test Case ID** | TC_APP_POST_001 |
| **Title** | Smplifai API vasitəsilə yeni müraciətin (Application) yaratması |
| **Pre-conditions** | 1. İstifadəçi sistemdə autentifikasiyadan keçməli və aktiv Bearer Token-ə sahip olmalıdır.<br>2. Endpoint əlçatan olmalıdır: `https://smplifai-backend.vercel.app/api/applications` |

---

### Test Addımları (Steps)

| # | Addım (Action) | Gözlənilən Nəticə (Expected Result) |
| :-: | :--- | :--- |
| **1** | Swagger API UI və ya Postman vasitəsilə `POST /api/applications` endpoint-ini seçin. | `POST` sorğusu bölməsi açılır. |
| **2** | **Headers** bölməsində müvafiq Bearer Token-i daxil edin. | Autentifikasiya header-i daxil edilir. |
| **3** | `POST` sorğusunu göndərmək üçün **Execute** (və ya **Send**) düyməsinə klikləyin. | Sorğu serverə uğurla göndərilir. |
| **4** | Cavabın (Response) **Status Code**-nu və **Body** məlumatlarını yoxlayın. | Cavab kimi `201 Created` status kodu və yaradılmış obyektin məlumatları (DRAFT statusunda) qaytarılır. |

---

### Gözlənilən Nəticə (Expected Result)

* **HTTP Status Code:** `201 Created`
* **Response Body:**

```json
{
  "id": "f6c4373c-e6b9-4727-ab2e-73fac97f10e7",
  "user_id": "54efe78c-f0d3-4ee2-a318-2d1ad24941b9",
  "type": "My Passport",
  "email": null,
  "phone": null,
  "passport_data": null,
  "file_url": null,
  "status": "DRAFT",
  "created_at": "2026-09-09T16:04:44.747629+00:00",
  "updated_at": "2026-09-09T16:04:44.747629+00:00",
  "documents_uploaded": false,
  "reject_reason": null
}
