# Bug Reports – Smplifai Platform

**Project:** Smplifai  
**Author:** Səmayə Heybətova  

---

## Bug ID: BUG-001
- **Başlıq:** Şifrə sıfırlama linki/e-poçtu istifadəçiyə getmir
- **Layihə:** Smplifai
- **Modul:** Password Reset
- **Mühit (Environment):** Windows 11 / Chrome
- **Severity:** High
- **Priority:** High
- **İlkin şərtlər (Preconditions):** İstifadəçinin aktiv hesabı var.
- **Təkrar etmək üçün addımlar (Steps to Reproduce):**
  1. Şifrə sıfırlama səhifəsinə keç.
  2. "Forgot password" düyməsini sıx və valid email daxil et.
  3. "Reset password" düyməsini sıx.
- **Faktiki nəticə (Actual Result):** Sistem e-poçt göndərmir.
- **Gözlənilən nəticə (Expected Result):** Sistem şifrə sıfırlama linkini e-poçtla göndərməlidir.
- **Status:** Open

---

## Bug ID: BUG-002
- **Başlıq:** Profil şəkli hesabdan çıxış edib yenidən daxil olduqda silinir
- **Layihə:** Smplifai
- **Modul:** Profil
- **Mühit (Environment):** Windows 11 / Chrome
- **Severity:** Medium
- **Priority:** Medium
- **İlkin şərtlər (Preconditions):** İstifadəçi hesabına daxil olub.
- **Təkrar etmək üçün addımlar (Steps to Reproduce):**
  1. Profile Settings bölməsinə keç.
  2. Yeni JPG profil şəkli yüklə.
  3. Log out ol və yenidən daxil ol.
- **Faktiki nəticə (Actual Result):** Yüklənmiş profil şəkli silinir, standart ikon görünür.
- **Gözlənilən nəticə (Expected Result):** Şəkil yadda qalmalı və yenidən daxil olduqda görünməlidir.
- **Status:** Open

---

## Bug ID: BUG-003
- **Başlıq:** Səhifə mobil cihazlarda düzgün açılmır, bəzi düymələr görünmür
- **Layihə:** Smplifai
- **Modul:** Mobile UI
- **Mühit (Environment):** Android / Chrome Mobile
- **Severity:** High
- **Priority:** High
- **İlkin şərtlər (Preconditions):** İstifadəçi mobil brauzerdən daxil olub.
- **Təkrar etmək üçün addımlar (Steps to Reproduce):**
  1. Mobil cihazda saytı aç.
  2. Panellərə və idarəetmə düymələrinə bax.
- **Faktiki nəticə (Actual Result):** Düymələr ekrandan kənara çıxır və görünmür.
- **Gözlənilən nəticə (Expected Result):** Bütün elementlər mobil ekrana uyğunlaşmalıdır.
- **Status:** Open
