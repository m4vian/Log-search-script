<div align="center">

# 🚀 LogSearch.xyz

**Modern, Hızlı ve Güvenilir API Tabanlı Log Arama Altyapısı**

[![PHP Version](https://img.shields.io/badge/PHP-8.1+-7A86B8.svg?style=flat-square&logo=php)](https://php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1.svg?style=flat-square&logo=mysql&logoColor=white)](https://mysql.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

LogSearch.xyz, uygulamalarınızın ve projelerinizin `.txt` veya benzeri log kayıtları içerisinde çok hızlı bir şekilde arama yapmanıza olanak tanıyan, açık kaynak kodlu bir web ve API projesidir. **Gelişmiş kullanıcı yönetimi, entegre plan-bakiye sistemi ve tamamen özelleştirilebilir altyapısı** ile kendi "Log Arama" servisinizi birkaç dakika içerisinde başlatabilirsiniz.

---

## 🌟 Neden LogSearch?

- ⚡ **Hızlı Çalışma Prensibi:** Dosyaları optimize bir şekilde tarayarak anında sonuç döndürür.
- 🔒 **Güvenli Kimlik Doğrulama:** JWT/Token tarzı API anahtarları ile sadece yetkili kullanıcıların işlem yapmasını sağlar.
- 📊 **Detaylı Analitik:** Dashboard üzerinden hangi API anahtarının ne kadar harcama yaptığını ve başarı oranlarını izleyebilirsiniz.
- 💳 **Discord Entegreli Plan Sistemi:** Ödemeler geleneksel portallar yerine direkt olarak belirlediğiniz Discord sunucusu üzerinden sağlanır.

## 🛠 Teknik Altyapı
- **Backend:** PHP 8.1+ (Vanilla PHP, Herhangi bir ağır framework içermez). Sadece PDO kullanılarak geliştirildi.
- **Frontend:** Vanilla JavaScript (SPA), HTML5, Özel Token Tabanlı CSS.
- **Veritabanı:** MySQL / MariaDB

---

## 🚀 Kurulum Adımları

### 1. Dosya Düzeni ve Web Sunucusu
1. Projeyi bilgisayarınıza veya sunucunuza kopyalayın.
2. HTTP sunucunuzun kök dizinini projenin bulunduğu dizin olarak ayarlayın. (Klasörde yer alan `.htaccess` sayesinde yönlendirmeler hazırdır.)

### 2. Veritabanı Yapılandırması
1. Ana klasörde bulunan `database.sql` dosyasını oluşturduğunuz yeni bir MySQL veritabanına import edin.
2. `server/database/Database.php` dosyasını açarak veritabanı ayarlarını ve Discord adresinizi kendinize göre düzenleyin:

```php
    private const CONFIG = [
        'host'    => 'localhost',
        'port'    => 3306,
        'dbname'  => 'logsearch', // Burayı projenize göre güncelleyin.
        'charset' => 'utf8mb4',
        'user'    => 'root',
        'pass'    => '',
    ];

    /**
     * Discord URL - Ödemeler ve destek için yönlendirme adresi
     */
    public const DISCORD_URL = 'https://discord.gg/your_discord_invite';
```

### 3. Yönetici (Admin) Hesabı

Veritabanını başarıyla import ettiğinizde sizin için otomatik bir Admin hesabı oluşacaktır. Bu hesapla tüm sistemi yönetebilir, kullanıcılara müdahale edebilirsiniz:

- **E-posta:** `lightning@demo.com`
- **Şifre:** `lightning3162`

*(Güvenliğiniz için sisteme giriş yaptıktan sonra bu bilgileri değiştirmeniz tavsiye edilir.)*

### 4. Log Dosyalarının Ekleneceği Yer
Aramaların gerçekleştirildiği yer `server/logs/` klasörüdür. Taratmak istediğiniz tüm `.txt` veya desteklenen metin formatlarını bu dizinin içerisine yüklemelisiniz. Klasörde varsayılan olarak `sample_logs.txt` bulunmaktadır. Test amacıyla kullanabilirsiniz.

---

## 💻 Kullanım / Ekran Görüntüleri

### Müşteri Kullanımı: 
Kullanıcılar sisteme giriş yaptıklarında kendilerine tahsis edilen günlük arama limiti kadarını kullanarak, "Log Arama" sayfasından sonuçlarını eş zamanlı görüntüleyebilir veya indirebilirler.

### Bakiye Yükleme ve Ödemeler:
Proje açık kaynak kodlu ve ücretsiz bir felsefe üzerine yayıldığı için harici pos modülleri dahil edilmemiştir. Kullanıcılarınızın planlarını yenilemeleri veya bakiye yüklemeleri gerektiğinde onlara doğrudan **Discord** bağlantınız çıkarılarak "Bakiye Yükle" veya "Satın Al (Discord)" imkanı tanınır.

---

## 🤝 Katkıda Bulunma
Projeyi dilediğiniz gibi geliştirebilir, fork'layabilir veya pull-request göndererek geliştirmemize yardımcı olabilirsiniz! Yeni özellikler ve hata bildirimleri için [Issues] bölümünü kullanmayı unutmayın.

## 📄 Lisans
Bu proje **MIT Lisansı** altında özgürce paylaşılmıştır.
