# Risk Assessment Report

| Risk Name | Severity | Notes |
| :--- | :--- | :--- |
| Hardcoded Credentials | High | `config.php` faylında şifrələr və API açarları birbaşa yazılıb. Repozitoriyaya giriş olan hər kəs bazaya sızma edə bilər. |
| SQL Injection Vulnerability | High | İstifadəçi girişləri (input) sanitizasiya olunmur. Hücumçular bazanı oğurlaya və ya silə bilər. |
| Deprecated API Usage | High | Köhnəlmiş PHP funksiyalarından istifadə olunur. Server yenilənməsində tətbiq tamamilə fəaliyyətini dayandıra bilər. |
| Insecure File Permissions | Medium | Konfiqurasiya faylları "world-readable" statusundadır. Serverdəki digər istifadəçilər həssas məlumatları oxuya bilər. |
| Missing Unit Tests | Medium | Kritik modulların testi yoxdur. Dəyişikliklər proqramın digər hissələrini sıradan çıxara bilər (Regression). |
| Tight Coupling | Medium | Modullar arasındakı asılılıq çoxdur. Bu, kodun oxunmasını çətinləşdirir və texniki borcu (technical debt) artırır. |
| No Logging Mechanism | Low | Sistem xətaları qeydə alınmır. Nasazlıqların səbəbini tapmaq və debugging prosesi çox vaxt aparır. |
| Lack of Rate Limiting | Medium | Login hissəsində "brute-force" hücumlarına qarşı limit yoxdur. Şifrələr asanlıqla sındırıla bilər. |
