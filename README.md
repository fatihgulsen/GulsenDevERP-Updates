# Gulsen.dev ERP — Güncelleme Merkezi

> Bu depo, **Gulsen.dev ERP** uygulamasının otomatik güncelleme altyapısını barındırır.  
> Kaynak kodu için: [fatihgulsen/Gulsen.dev-ERP](https://github.com/fatihgulsen/Gulsen.dev-ERP)

---

## 📥 Kurulum

### Gereksinimler
- **İşletim Sistemi:** Windows 10 / 11 (64-bit)
- **.NET 8 Runtime:** [İndir](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- **PostgreSQL 15+:** Veritabanı sunucusu (sistem yöneticiniz tarafından kurulur)

### İlk Kurulum Adımları

1. **En son sürümü indirin**  
   Sağ taraftaki **Releases** bölümünden en güncel `GulsenDevERP-{versiyon}.zip` dosyasını indirin.

2. **Arşivi açın**  
   İndirilen `.zip` dosyasını `C:\GulsenDevERP\` gibi bir klasöre çıkarın.

3. **Yapılandırma dosyasını düzenleyin**  
   `appsettings.json` dosyasını açın ve veritabanı bağlantı bilgilerini girin:
   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Host=SUNUCU_IP;Database=erp_db;Username=kullanici;Password=sifre"
     }
   }
   ```

4. **Uygulamayı başlatın**  
   `GulsenDevERP.Win.exe` dosyasını çalıştırın.  
   İlk açılışta veritabanı şeması otomatik olarak oluşturulur.

---

## 🔄 Otomatik Güncelleme

Uygulama, her açılışta bu depodaki `update-info.json` dosyasını kontrol eder.

- **Yeni sürüm varsa:** Ekranda güncelleme bildirimi gösterilir.
- **Güncellemeyi kabul ederseniz:** Uygulama otomatik olarak indirir, doğrular ve yükler. Eski sürümün yedeği alınır.
- **Güncellemeyi reddederseniz:** Bir sonraki açılışa kadar ertelenir (zorunlu güncellemeler hariç).

### Güncelleme Kanalları

| Kanal | Açıklama |
|-------|----------|
| `stable` | Üretim ortamı için test edilmiş, kararlı sürümler |
| `beta` | Yeni özellikler içeren ön sürümler (test amaçlı) |
| `dev` | Geliştirici yapıları (yalnızca iç kullanım) |

---

## 🚀 Temel Kullanım

### Giriş
- Uygulama açıldığında kullanıcı adı ve şifrenizi girin.
- İlk kurulumda varsayılan yönetici hesabı: `Admin` / `Admin` *(ilk girişte değiştirmeniz önerilir)*

### Ana Modüller

| Modül | Açıklama |
|-------|----------|
| **Stok Yönetimi** | Ürün kartları, stok hareketleri, depo takibi |
| **Satış** | Teklifler, siparişler, faturalar, e-Fatura/e-İrsaliye |
| **Satınalma** | Satınalma talepleri, siparişler, onay süreçleri |
| **Üretim** | Üretim emirleri, reçeteler, iş istasyonları |
| **Finans** | Cari hesaplar, kasa, çek/senet takibi |
| **CRM** | Müşteri aktiviteleri, fırsatlar, kampanyalar |
| **İnsan Kaynakları** | Personel, bordro, izin takibi |
| **Kalite Kontrol** | Kalite formları, kontrol noktaları |
| **WMS** | Depo konumları, sayım fişleri, barkod okuma |

### Klavye Kısayolları

| Kısayol | İşlev |
|---------|-------|
| `F5` | Listeyi yenile |
| `Ctrl+N` | Yeni kayıt |
| `Ctrl+S` | Kaydet |
| `Ctrl+F` | Ara |
| `Esc` | İptal / Geri |

---

## 🛠️ Sorun Giderme

### Uygulama açılmıyor
- .NET 8 Runtime kurulu olduğundan emin olun.
- `appsettings.json` içindeki bağlantı bilgilerini kontrol edin.
- Güvenlik duvarının PostgreSQL portuna (5432) izin verdiğini doğrulayın.

### Güncelleme başarısız oluyor
- İnternet bağlantınızı kontrol edin.
- `C:\GulsenDevERP\` klasörüne yazma izniniz olduğundan emin olun.
- Antivirüs yazılımının uygulamayı engellemediğini kontrol edin.

### Veritabanı bağlantı hatası
- PostgreSQL servisinin çalıştığını doğrulayın.
- Kullanıcı adı ve şifrenin doğru olduğunu kontrol edin.
- Sunucu IP adresinin erişilebilir olduğundan emin olun.

---

## 📞 Destek

Sorunlarınız için:
- 📧 **E-posta:** destek@gulsen.dev
- 🐛 **Hata Bildirimi:** [GitHub Issues](https://github.com/fatihgulsen/Gulsen.dev-ERP/issues)

---

## 📋 Sürüm Geçmişi

Tüm değişiklikler için: [CHANGELOG.md](https://github.com/fatihgulsen/Gulsen.dev-ERP/blob/master/CHANGELOG.md)

---

*Bu depo otomatik olarak yönetilmektedir. Lütfen doğrudan dosya değişikliği yapmayın.*
