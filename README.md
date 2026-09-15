# TC-001: Smplifai - My Application Yoxlanması

## 📌 Əsas Məlumatlar
* **Test Case ID:** TC-001  
* **Title:** Smplifai - "My Application" funksionallığının və backend inteqrasiyasının yoxlanılması  
* **Prioritet:** High (Yüksək)  
* **Pre-conditions:**  
  1. İstifadəçi sistemdə autentifikasiyadan keçib (Bearer token ilə sistemə daxil olunub).  
  2. Yüklənəcək sənəd faylı yerli diskdə mövcuddur.  

---

## 🧪 UI Test Addımları

| # | Addım | Gözlənilən Nəticə (Expected Result) |
|---|---|---|
| **1** | **Smplifai** saytına daxil olub **"New Application"** düyməsinə klik et. | Yeni müraciət forması ekranda açılır. |
| **2** | `Email` və `Phone` xanalarına valid (doğru) məlumatları daxil et. | Məlumatlar xanalara düzgün daxil olunur. |
| **3** | **"Choose"** düyməsinə klik et. | Sənəd növünün seçilməsi paneli açılır. |
| **4** | **"Browse files"** düyməsinə klik edərək faylı seç. | Fayl uğurla seçilir və formaya əlavə olunur. |
| **5** | **"Next"** düyməsinə klik et. | Ekranda "Document successfully uploaded" bildirişi görünür və müraciət göndərilir. |

---

## 🔍 Backend (API Validation - Swagger / Postman)

### 1. Request Detalları
* **API Docs / Swagger:** Smplifai API Docs  
* **HTTP Method:** `GET` / `POST`  
* **Request URL:** `https://smplifai-backend.vercel.app/api/applications`  
* **Headers:**  
  ```http
  Authorization: Bearer <your_token_here>
  Content-Type: application/json
