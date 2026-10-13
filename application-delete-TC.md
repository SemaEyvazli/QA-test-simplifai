# Test Case: Application Deletion via API

| Sahə | Məlumat |
| :--- | :--- |
| **Test Case ID** | TC_APP_DEL_001 |
| **Title** | Smplifai saytında yaradılmış müraciətin (My Application) API vasitəsilə silinməsi (DELETE) |
| **Pre-conditions** | 1. İstifadəçi sistemdə autentifikasiyadan keçməli və aktiv Bearer Token-ə sahib olmalıdır.<br>2. Silinəcək müraciət sistemdə mövcud olmalıdır. |

---

### Test Addımları (Steps)

| # | Addım (Action) | Gözlənilən Nəticə (Expected Result) |
| :-: | :--- | :--- |
| **1** | **Smplifai** saytına daxil olub **"New Application"** düyməsinə klikləyin. | Müraciət forması açılır. |
| **2** | **Email** və **Phone** xanalarına müvafiq məlumatları daxil edin. | Məlumatlar xanalara uğurla yazılır. |
| **3** | **"Choose"** düyməsinə, ardından **"Browse files"** düyməsinə klikləyərək faylı seçin. | Fayl uğurla seçilir. |
| **4** | **"Next"** düyməsinə klikləyin. | *"Document successfully uploaded"* bildirişi görünür və müraciət yaradılır. |
| **5** | Swagger API sənədləşməsinə (`Smplifai API Docs`) daxil olun. | API sənədləşmə səhifəsi açılır. |
| **6** | Yuxarıda yerləşən **"Authorize"** düyməsinə klikləyin, Bearer tokeni daxil edin və təsdiqləyin. | Autentifikasiya uğurla tamamlanır. |
| **7** | `DELETE /api/applications/{id}` sorğusunu seçin. | Sorğunun parametrlər bölməsi açılır. |
| **8** | `id` xanasına silinəcək müraciətin ID-sini (`72a38e24-5f54-43d5-82bc-d20bad97dd81`) daxil edib **"Execute"** düyməsinə klikləyin. | API sorğusu icra olunur. |

---

### Gözlənilən Yoxlama (Verification)

Silinmə addımının uğurlu olduğunu doğrulamaq üçün Swagger cavabını yoxlayın:
* **Status Code:** `200 OK`
* **Response Body:** Müraciətin uğurla silindiyini təsdiqləyən mesaj (`"success": true`).

---

### Xəta Ssenarisi və Həlli (Troubleshooting / Negative Case)

Əgər **Authorize** olunmadan sorğu göndərilərsə:

* **Request URL:** `DELETE https://smplifai-backend.vercel.app/api/applications/72a38e24-5f54-43d5-82bc-d20bad97dd81`
* **Status Code:** `401 Unauthorized`
* **Response Body:**
  ```json
  {
    "success": false,
    "message": "Unauthorized"
  }
