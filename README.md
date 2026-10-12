# Test Plan – Smplifai Platforması

**Layihə:** Smplifai  
**Müəllif:** Səmayə Heybətova  
**Repozitoriya:** `simplifaiapplicationtestcase`  

---

## 1. Objective 
Bu Test Planın əsas məqsədi Smplifai tələbə qeydiyyatı və sənəd avtomatlaşdırılması tətbiqinin funksional imkanlarını, istifadəçi interfeysini (UI) və backend API inteqrasiyasını hərtərəfli sınaqdan keçirmək, sistemdəki potensial xətaları aşkar etməkdir.

---

## 2. Scope 

### In Scope 
- **Modul 1:** İstifadəçi qeydiyyatı və sistemə giriş (Sign In) funksionallığı.
- **Modul 2:** "My Application" bölməsində yeni müraciətin yaradılması, məcburi xanaların yoxlanması və sənəd yükləmə (Browse files).
- **Modul 3:** API testləri (Swagger / Postman vasitəsilə `DELETE /api/applications/{id}` sorğusunun müsbət və mənfi/təhlükəsizlik senariləri).
- **Modul 4:** İstifadəçi profil parametrlərinin idarə olunması.

### Out of Scope 
- Əsas backend verilənlər bazasının (Database) daxili performans testləri.
- Tətbiqin server infrastrukturu və yük altında dözümlülük (Load/Stress) testləri.
- Çap avadanlıqları ilə birbaşa inteqrasiya testləri.

---

## 3. Test Types 

| Test Type | Description |
|---|---|
| **Functional Testing** | Tələbə qeydiyyatı, müraciət formalarının doldurulması və sənəd yükləmə funksiyalarının doğrulanması. |
| **API Testing** | Swagger UI vasitəsilə Bearer Token ilə avtorizasiya və müraciətlərin silinməsi (DELETE) sorğularının test edilməsi. |
| **Negative Testing** | Yanlış məlumatlar daxil edildikdə və ya avtorizasiya tokeni olmadan API-yə müraciət edildikdə sistemin verdiyi cavabların (401 Unauthorized) yoxlanması. |
| **UI / UX Testing** | Səhifələrdəki düymələrin, mətn xanalarının və formaların fərqli ekran ölçülərində (masaüstü və mobil) vizual düzgünlüyü. |
| **Regression Testing** | Aşkar edilmiş BUG-001, BUG-002 və BUG-003 xətaları düzəldildikdən sonra sistemin digər hissələrinin pozulmadığını yoxlamaq. |

---

## 4. Test Environment

| Komponent | Məlumat / Alət |
|---|---|
| **Əməliyyat Sistemi** | Windows 11 |
| **Brauzerlər** | Google Chrome (Son versiya) |
| **API Test Alətləri** | Postman, Swagger UI |
| **Sənədləşmə Aləti** | GitHub Markdown, Visual Studio Code |

---

## 5. Entry Criteria 
Test prosesi aşağıdakı şərtlər ödənildikdə başlayır:
* Smplifai tətbiqinin QA mühiti və aktiv test versiyası (build) hazır olduqda.
* Test ssenariləri (`test-cases.md`) və yoxlama siyahısı hazırlanıb təsdiqləndikdə.
* API endpoint-ləri və Swagger dokumentasiyası əlçatan olduqda.

---

## 6. Exit Criteria
Test prosesi aşağıdakı nəticələr əldə edildikdə tamamlanmış sayılır:
* Yazılmış bütün 4 test keysi tam icra olunduqda.
* Yüksək və kritik prioritetli (High/Critical) açıq xətalar qalmadıqda.
* Yekun test hesabatı (`test-report.md`) hazırlanaraq repozitoriyaya əlavə edildikdə.

---

## 7. Risks & Mitigation

| Risk | Impact |  Mitigation |
|---|---|---|
| **API Tokenlərin vaxtının bitməsi** | Sorğuların 401 Unauthorized xətası verməsi və API testlərinin dayanması. | Testdən əvvəl Postman və Swagger üzərində Bearer Token-in yenilənməsini təmin etmək. |
| **Fayl yükləmə zamanı format xətaları** | Tələbə sənəd yükləyərkən sistemin faylı qəbul etməməsi. | Test keyslərdə dəstəklənən fayl formatlarını (PDF, JPG, PNG) əvvəlcədən dəqiq müəyyən etmək. |

---

## 8. Deliverables 
- `README.md` — Əsas Test Planı
- `test-cases.md` — Test Ssenariləri
- `bug-reports.md` — Xəta Hesabatları Cədvəli
- `test-report.md` — Yekun Test İcra Hesabatı

 
