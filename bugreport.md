# Bug Report

## BUG-001

| Field | Value |
|---|---|
| **Bug ID** | BUG-001 |
| **Title** | Şifrə sıfırlama linki/e-poçtu istifadəçiyə getmir |
| **Project** | Smplifai website |
| **Module** | Password Reset |
| **Browser** | Chrome |
| **OS** | Windows 11 |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |

### Preconditions

1. İstifadəçinin aktiv hesabı var.
2. İstifadəçi şifrə sıfırlama səhifəsindədir.

### Steps

1. Smplifai linkini açın.
2. "Forgot password" buttonuna klikləyin.
3. Qeydiyyatdan keçdiyiniz valid e-poçt ünvanını (smaeyvazli@mail.ru) daxil edin.
4. "Terms of Use" xanasını işarələyin.
5. "Reset password" buttonuna klikləyin.
6. Həmin e-poçt ünvanını yoxlayın.

### Actual Result

Sistem istifadəçinin e-poçt ünvanına şifrə sıfırlama ilə bağlı heç bir məktub və ya keçid linki göndərmir.

### Expected Result

Sistem şifrə sıfırlama e-poçtunu göndərməli və "Şifrə sıfırlama linki e-poçtunuza göndərildi" mesajı göstərməlidir.

### Attachments

- Screenshot
- Video recording

---

## BUG-002

| Field | Value |
|---|---|
| **Bug ID** | BUG-002 |
| **Title** | Profil şəkli hesabdan çıxış edib yenidən daxil olduqda silinir. |
| **Project** | Smplifai |
| **Module** | Profil |
| **Browser** | Chrome |
| **OS** | Windows 11 |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |

### Preconditions

1. İstifadəçi öz hesabına daxil olub.

### Steps

1. Smplifai linkini açın və hesaba daxil olun.
2. Profile Settings bölməsinə keçin.
3. Yeni profil şəkli JPG formatında yükləyin.
4. "Save changes" buttonuna klikləyin.
5. Hesabdan çıxış (Log out) edin.
6. Yenidən hesaba daxil olun və profil səhifəsinə keçin.

### Actual Result

Yüklənmiş profil şəkli silinir və onun yerində sistemin standart boş profil iconu görünür.

### Expected Result

Yüklənmiş profil şəkli yenidən daxil olduqda istifadəçiyə görünməlidir.

### Attachments

- Screenshot

---

## BUG-003

| Field | Value |
|---|---|
| **Bug ID** | BUG-003 |
| **Title** | Səhifə mobil cihazlarda düzgün açılmır, bəzi buttonlar və panellər görünmür. |
| **Project** | Smplifai website |
| **Module** | Saytin dizayninin mobil telefon ve kompyuterlerde eyni gorunmesi. |
| **Browser** | Chrome Mobile |
| **OS** | Android |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |

### Preconditions

- Istifadechi mobil cihaz brauzerindən daxil olub.
- Istifadechi Smplifai saytinin əsas səhifəsindədir.

### Steps

1. Mobil cihazda brauzeri açın.
2. Smplifai saytinin sehifesine daxil olun.
3. Kompyuter(desktop) versiyası ilə müqayisə edin.
4. Səhifədəki panellərə və idareetme buttonlarina (menyu, təsdiqləmə ve ya kechid buttonlarina) diqqət edin.
5. Görünməyən panellerin yerləşdiyi hissələri yoxlayın.

### Actual Result

Səhifənin dizaynı mobil ekrana uyğunlaşmır. Mühüm panellər və buttonlar ekrandan kənara çıxır və ya tamamilə istifadəçi üçün görünməz olur.

### Expected Result

Səhifənin bütün elementləri (buttonlar, panellər, yazılar) mobil ekran ölçülərinə tam uyğunlaşmalı və istifadəçi asanlıqla hər bir buttona klikləyə bilməlidir.

### Attachments

- Mobile Screenshot
