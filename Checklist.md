# QA Testing Checklist – Smplifai Platform

**Project:** Smplifai  
**Author:** Səmayə Heybətova  

---

## 1. Authentication & User Management
- [x] Sign In / Giriş səhifəsinin açılması və elementlərin yoxlanılması
- [x] Düzgün məlumatlarla sistemə uğurlu giriş (Valid Login)
- [x] Yanlış məlumatlarla giriş cəhdi - Negative Test (Invalid credentials)

## 2. Application Submission & File Upload ("My Application")
- [x] "New Application" düyməsinin işləkliyinin yoxlanılması
- [x] Məcburi xanaların boş qaldıqda validasiya mesajlarının çıxması
- [x] Sənəd faylının seçilməsi (Browse files) və yüklənməsi
- [x] "Next" düyməsinə kliklədikdə müraciətin uğurla yaradılması və bildirişin alınması

## 3. API Testing (Swagger & Postman Integration)
- [x] Bearer Token ilə Swagger/Postman üzərindən avtorizasiya olunma
- [x] `GET /api/applications` sorğusu ilə mövcud müraciətlərin siyahısının əldə edilməsi (200 OK)
- [x] `DELETE /api/applications/{id}` sorğusu ilə müraciətin uğurla silinməsi (200 OK)
- [x] Tokendsiz DELETE sorğusu verilərkən `401 Unauthorized` xətasının alınması (Security/Negative)
- [x] Yanlış/saxta ID ilə DELETE sorğusu verilərkən `404 Not Found` xətasının alınması

## 4. UI / UX & Responsiveness
- [x] Google Chrome brauzerində səhifə elementlərinin düzgün yerləşməsi
- [x] Düymələrin və formaların aktivlik və hover effektlərinin yoxlanılması
- [x] Əsas interfeys elementlərinin vizual uyğunluğunun yoxlanılması
