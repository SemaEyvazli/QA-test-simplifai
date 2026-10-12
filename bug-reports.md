# Bug Reports

| Bug ID | Title | Module | Environment | Severity | Priority | Preconditions | Steps to Reproduce | Actual Result | Expected Result | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| **BUG-001** | Şifrə sıfırlama linki/e-poçtu istifadəçiyə getmir | Password Reset | Windows 11 / Chrome | High | High | 1. İstifadəçinin aktiv hesabı var.<br>2. Şifrə sıfırlama səhifəsindədir. | 1. "Forgot password" düyməsini sıx.<br>2. Valid email daxil et.<br>3. "Reset password" düyməsini sıx. | Sistem e-poçt göndərmir. | Sistem şifrə sıfırlama linkini e-poçtla göndərməlidir. | Open |
| **BUG-002** | Profil şəkli hesabdan çıxış edib yenidən daxil olduqda silinir | Profil | Windows 11 / Chrome | Medium | Medium | 1. İstifadəçi hesabına daxil olub. | 1. Profile Settings bölməsinə keç.<br>2. Yeni JPG profil şəkli yüklə.<br>3. Log out ol və yenidən daxil ol. | Yüklənmiş profil şəkli silinir, standart ikon görünür. | Şəkil yadda qalmalı və yenidən daxil olduqda görünməlidir. | Open |
| **BUG-003** | Səhifə mobil cihazlarda düzgün açılmır, bəzi düymələr görünmür | Mobile UI | Android / Chrome Mobile | High | High | 1. İstifadəçi mobil brauzerdən daxil olub. | 1. Mobil cihazda saytı aç.<br>2. Panellərə və idarəetmə düymələrinə bax. | Düymələr ekrandan kənara çıxır və görünmür. | Bütün elementlər mobil ekrana uyğunlaşmalıdır. | Open |
