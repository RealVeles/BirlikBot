# Birlik Bot Yönetim Paneli

Birlik Bot Yönetim Paneli, Discord botlarınızı tek bir web arayüzünden yönetmenizi sağlayan kapsamlı bir çözümdür. Farklı tokenlerde birden fazla Discord botunu tek bir arayüzden yönetebilir, tüm bot aktivitelerini SQL ve TXT formatında loglayabilirsiniz.

![Dashboard](https://placeholder-for-dashboard-screenshot.png)

## 🌟 Özellikler

- **Çoklu Bot Desteği**: Discord tokeni olan her botu ekleyebilir ve yönetebilirsiniz
- **Detaylı Loglama**: Tüm bot aktiviteleri hem SQL veritabanında hem de TXT dosyalarında loglanır
- **Modern Arayüz**: Neon turkuaz temalı, responsive ve animasyonlu modern arayüz
- **Özelleştirilebilir**: Tüm ayarlar web arayüzünden yapılandırılabilir
- **Çeşitli Bot Türleri**:
  - 🎵 **Müzik Botu**: Ses kanallarında müzik çalma
  - 🛡️ **Moderasyon Botu**: Sunucu yönetimi için komutlar
  - 🔰 **Guard Botu**: Sunucu koruması için gelişmiş özellikler
  - 📝 **Kayıt Botu**: Kullanıcı kayıt işlemleri
  - 🏷️ **Oto Rol Botu**: Otomatik rol verme işlemleri
  - ⚠️ **Ceza Kayıtları/Blacklist**: Kullanıcı ceza geçmişi ve blacklist sistemi
  - 📊 **Log Botu**: Sunucu olaylarını loglama
  - 🔧 **Kanal ve Rol Moderasyonu**: Kanal ve rol yönetimi
  - 📈 **Sıralama Sistemi**: Aktivite bazlı sıralama sistemi (ses ve mesaj)

## 💻 Kurulum

### Gereksinimler

- Node.js (v16.0.0 veya daha yüksek)
- npm veya yarn
- SQLite veya MongoDB (varsayılan SQLite)

### Adımlar

1. Projeyi klonlayın:
```bash
git clone https://github.com/RealVeles/BirlikBot.git
cd BirlikBot
```

2. Gerekli paketleri yükleyin:
```bash
npm run install-all
```

3. `.env` dosyasını ayarlayın:
```
PORT=3000
JWT_SECRET=sizin-gizli-anahtariniz
ENCRYPTION_KEY=token-sifreleme-anahtariniz
NODE_ENV=development
# MongoDB kullanmak istiyorsanız (opsiyonel)
# MONGODB_URI=mongodb://localhost:27017/birlik-bot-panel
```

4. Uygulamayı başlatın:
```bash
npm run dev
```

5. Tarayıcınızda `http://localhost:3000` adresine gidin ve kurulum sihirbazını başlatın.

## 🚀 Kullanım

### İlk Kurulum

1. Kurulum sayfasını açın (`http://localhost:3000/setup`)
2. Yönetici kullanıcı bilgilerini girin
3. Kurulumu tamamlayın ve giriş yapın

### Bot Ekleme

1. Dashboard'dan "Botlar" sayfasına gidin
2. "Yeni Bot Ekle" butonuna tıklayın
3. Bot bilgilerini (isim, token, tür) girin
4. Bot özelliklerini seçin ve ekleyin
5. Botu başlatın ve yönetmeye başlayın

### Bot Yönetimi

- **Başlatma/Durdurma**: Bot sayfasından başlatabilir veya durdurabilirsiniz
- **Ayarları Değiştirme**: Bot ayarlarını düzenleyebilirsiniz
- **İstatistikler**: Bot kullanım istatistiklerini görüntüleyebilirsiniz
- **Loglar**: Bot aktivite loglarını inceleyebilirsiniz

## 📊 Bot Türleri ve Özellikleri

### 🎵 Müzik Botu
- YouTube, Spotify, SoundCloud'dan müzik çalma
- Çalma listesi desteği
- Ses kontrolü
- Sıra yönetimi

### 🛡️ Moderasyon Botu
- Mesaj silme
- Kullanıcı yasaklama/atma
- Susturma işlemleri
- Uyarı sistemi

### 🔰 Guard Botu
- Spam koruması
- Sunucu ayarları koruması
- İzin değişikliği takibi
- Zararlı içerik filtreleme

### 📝 Kayıt Botu
- Otomatik rol verme
- Kayıt bilgisi kaydetme
- Özelleştirilebilir hoş geldin mesajları
- İsim formatları

### 🏷️ Oto Rol Botu
- Katılımda otomatik rol
- Seviye bazlı rol verme
- Tepki rolü sistemi
- Geçici rol verme

### ⚠️ Ceza Kayıtları/Blacklist
- Ceza geçmişi kaydetme
- Blacklist yönetimi
- Ceza sorgulama
- Otomatik ceza sistemi

### 📊 Log Botu
- Kanal işlemleri logları
- Rol işlemleri logları
- Üye giriş/çıkış logları
- Mesaj logları

### 🔧 Kanal ve Rol Moderasyonu
- Kanal oluşturma/silme
- Rol oluşturma/silme
- Toplu rol verme/alma
- Kanal ve rol izinleri yönetimi

### 📈 Sıralama Sistemi
- Mesaj aktivite sıralaması
- Ses aktivite sıralaması
- Günlük, haftalık, aylık, genel sıralamalar
- Kanal bazlı sıralamalar

## 🔧 Gelişmiş Ayarlar

### Veritabanı Değiştirme
SQLite'dan MongoDB'ye geçiş yapmak için:

1. `.env` dosyasında `MONGODB_URI` değişkenini ayarlayın
2. Ayarlar sayfasında "Veritabanı" sekmesinden MongoDB'yi seçin
3. Yeniden başlatın

### Loglama Ayarları
Loglama ayarlarını değiştirmek için:

1. Ayarlar sayfasında "Loglama" sekmesine gidin
2. SQL ve TXT loglamayı açıp kapatabilirsiniz
3. Log seviyesini ayarlayabilirsiniz
4. Log rotasyonu ayarlarını değiştirebilirsiniz

## 🔒 Güvenlik

- Tüm Discord bot tokenleri veritabanında şifrelenmiş şekilde saklanır
- JWT tabanlı kimlik doğrulama kullanılır
- Kullanıcı yetkilendirme sistemi mevcuttur
- HTTPS kullanımı önerilir (production ortamında)

## 📚 API Dokümantasyonu

REST API'ye `/api` endpoint'inden erişilebilir. Temel endpoint'ler:

- `/api/auth`: Kimlik doğrulama işlemleri
- `/api/bots`: Bot yönetimi
- `/api/users`: Kullanıcı yönetimi
- `/api/stats`: İstatistik verileri
- `/api/settings`: Sistem ayarları

Ayrıntılı API dokümantasyonu için API endpoint'lerini kullanırken tarayıcı konsolunda `Network` sekmesini inceleyebilirsiniz.

## 🤝 Katkıda Bulunma

Katkıda bulunmak için lütfen aşağıdaki adımları izleyin:

1. Bu repo'yu fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some amazing feature'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## 📜 Lisans

Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.

## 📮 İletişim

Sorularınız veya önerileriniz için [billkafasi@gmail.com](mailto:billkafasi@gmail.com) adresine e-posta gönderebilirsiniz.
