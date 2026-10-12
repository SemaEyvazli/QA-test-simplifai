# Test Cases for Smplifai Platform

## TC-001: Smplifai - My Application Yoxlanması
- **Test Case ID:** TC-001
- **Title:** Smplifai - "My Application" funksionallığının və backend inteqrasiyasının yoxlanılması
- **Prioritet:** High (Yüksək)
- **Pre-conditions:** İstifadəçi sistemdə autentifikasiyadan keçməli və aktiv Bearer Token-ə sahib olmalıdır.

### Test Addımları:
1. Smplifai saytında "New Application" düyməsinə klikləyin.
2. Email və Phone xanalarına müvafiq məlumatları daxil edin.
3. "Choose" düyməsinə, ardından "Browse files" düyməsinə klikləyərək faylı seçin.
4. "Next" düyməsinə klikləyin.

### Expected Result:
- "Document successfully uploaded" bildirişi görünür və müraciət yaradılır.
- Verification: Müraciətin yarandığını təsdiqləmək üçün siyahıda yeni record görünür.

---

## TC-002: User Registration & Sign In Validation
- **Test Case ID:** TC-002
- **Title:** Yeni istifadəçi qeydiyyatı və sistemə giriş
- **Prioritet:** High (Yüksək)

### Test Addımları:
1. Smplifai giriş səhifəsinə daxil olun.
2. Düzgün email və şifrə məlumatlarını daxil edin.
3. "Sign In" düyməsini sıxın.

### Expected Result:
- İstifadəçi uğurla profil paneline (Dashboard) yönləndirilir.
- Verification: Əsas paneldə istifadəçi profil adı görünür.

---

## TC-APP-DEL-001: Application Deletion via API (DELETE)
- **Test Case ID:** TC-APP-DEL-001
- **Title:** Smplifai saytında yaradılmış müraciətin API vasitəsilə silinməsi
- **Prioritet:** High (Yüksək)

### Test Addımları:
1. Swagger API sənədləşməsinə daxil olun.
2. "Authorize" düyməsinə klikləyib Bearer token-i daxil edin.
3. `DELETE /api/applications/{id}` sorğusunu seçin.
4. `id` xanasına silinəcək müraciətin ID-sini daxil edib "Execute" düyməsini sıxın.

### Expected Result:
- **Status Code:** `200 OK`
- **Response Body:** `"success": true`
- Verification: GET /api/applications/{id} sorğusu verdikdə 404 Not Found qayıdır.

---

## TC-APP-DEL-002: Negative Case - Unauthorized Application Deletion
- **Test Case ID:** TC-APP-DEL-002
- **Title:** Token olmadan müraciətin silinməyə cəhd edilməsi (Təhlükəsizlik Testi)
- **Prioritet:** High (Yüksək)

### Test Addımları:
1. Bearer Token daxil etmədən `DELETE /api/applications/{id}` sorğusunu icra edin.

### Expected Result:
- **Status Code:** `401 Unauthorized`
- **Response Body:** `"message": "Unauthorized"`
- Verification: Silinməyə cəhd edilən müraciət sistemdə toxunulmaz qalır.
