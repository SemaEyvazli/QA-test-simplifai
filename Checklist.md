# QA Testing Checklist – Smplifai Platform

**Project:** Smplifai (Student Registration & Document Automation)  
**Author:** Səmayə Heybətova  

---

## 1. Authentication & User Management
- [x] Sign In səhifəsinin açılması və giriş elementlərinin (Email, Password, Login button) işləkliyinin yoxlanılması
- [x] Düzgün məlumatlar daxil edildikdə sistemə uğurlu giriş (Valid Login)
- [x] Yanlış məlumatlar və ya səhv şifrə daxil edildikdə xəta mesajlarının alınması (Negative Test)

## 2. Application Submission & File Upload ("My Application")
- [x] "New Application" düyməsinin kliklənməsi və müraciət formasının açılması
- [x] Məcburi sahələrin (Email, Phone) doldurulması və validasiya yoxlamaları
- [x] "Browse files" vasitəsilə sənəd faylının seçilməsi və sistemə yüklənməsi
- [x] "Next" düyməsinə basıldıqda müraciətin uğurla yaradılması və siyahıda görünməsi

## 3. API Testing (Swagger & Postman Integration)
- [x] Bearer Token əldə edilərək Swagger UI / Postman üzərində avtorizasiya olunması
- [x] `GET /api/applications` sorğusu vasitəsilə mövcud müraciətlər siyahısının çəkilməsi (200 OK)
- [x] `DELETE /api/applications/{id}` sorğusu ilə yaradılmış müraciətin uğurla silinməsi (200 OK)
- [x] Token daxil edilmədən DELETE sorğusu verildikdə `401 Unauthorized` xətasının alınması (Security/Negative)
- [x] Yanlış və ya saxta ID ilə DELETE sorğusu verildikdə `404 Not Found` xətasının alınması

## 4. UI / UX & Responsiveness
- [x] Google Chrome brauzerində səhifə elementlərinin və dizaynın düzgün hizalanması
- [x] Mobil brauzerlərdə düymələrin, formaların və panellərin görünməsi və uyğunluğu
