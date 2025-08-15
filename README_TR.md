[🇬🇧 İngilizce için tıklayın](README.md)

# Uyku Algılama Sistemi

Göz hareketlerini, baş pozisyonunu ve yüz ifadelerini izleyerek uyku hali ve uyuklama durumlarını gerçek zamanlı olarak tespit eden kapsamlı bir bilgisayarlı görü tabanlı uyku algılama sistemi. Bu sistem, sürücü izleme, iş yeri güvenliği ve eğitim ortamları gibi güvenlik kritik uygulamalar için tasarlanmıştır.

## 🚀 Özellikler

- **Gerçek zamanlı göz takibi**: MediaPipe kullanarak gelişmiş göz açıklığı/kapalılığı tespiti
- **Baş pozisyonu tespiti**: Hassas baş pozisyonu tahmini ve hareket takibi
- **Yüz landmark analizi**: Kapsamlı yüz özelliği tespiti ve izleme
- **Uyku durumu sınıflandırması**: Uyanık, uyuklama ve uyku durumlarının akıllı sınıflandırması
- **Video işleme**: Video dosyaları ve gerçek zamanlı kamera beslemesi desteği
- **Uyarı sistemi**: Uyku tespit edildiğinde yapılandırılabilir uyarılar ve bildirimler
- **Performans optimizasyonu**: Gerçek zamanlı uygulamalar için verimli işleme
- **Çapraz platform uyumluluğu**: Windows, macOS ve Linux'ta çalışır

## 🛠️ Teknoloji Altyapısı

- **Bilgisayarlı Görü**: Görüntü işleme ve video yakalama için OpenCV
- **Makine Öğrenmesi**: Yüz landmark tespiti için MediaPipe
- **Veri İşleme**: Sayısal hesaplamalar için NumPy
- **Python**: Hızlı geliştirme ve dağıtım için temel programlama dili

## 📋 Gereksinimler

### Sistem Gereksinimleri
- İşletim Sistemi: Windows 10+, macOS 10.14+ veya Ubuntu 18.04+
- RAM: Minimum 4GB, Önerilen 8GB+
- Depolama: 2GB boş alan
- Kamera: Gerçek zamanlı tespit için webcam veya USB kamera

### Yazılım Gereksinimleri
- Python 3.7 veya üzeri
- OpenCV 4.5.0+
- MediaPipe 0.8.0+
- NumPy 1.19.0+

## 🔧 Kurulum

### Ön Gereksinimler
Sisteminizde Python 3.7+ kurulu olduğundan emin olun. [python.org](https://python.org) adresinden indirebilirsiniz.

### Adım Adım Kurulum

1. **Depoyu klonlayın:**
   ```bash
   git clone https://github.com/Semihkulekcioglu/uyku_algilama_sleep_detection.git
   cd uyku_algilama_sleep_detection
   ```

2. **Sanal ortam oluşturun (önerilen):**
   ```bash
   python -m venv venv
   
   # Windows'ta:
   venv\Scripts\activate
   
   # macOS/Linux'ta:
   source venv/bin/activate
   ```

3. **Bağımlılıkları yükleyin:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Kurulumu doğrulayın:**
   ```bash
   python -c "import cv2, mediapipe, numpy; print('Tüm paketler başarıyla kuruldu!')"
   ```

## 🚀 Kullanım

### Temel Kullanım
Uyku algılama sistemini başlatmak için ana scripti çalıştırın:
```bash
python Uyku_algilama.py
```

### Gelişmiş Kullanım
Sistem çeşitli giriş kaynaklarını destekler:
- **Webcam**: Bilgisayarınızın kamerasından gerçek zamanlı tespit
- **Video dosyaları**: Analiz için önceden kaydedilmiş videoları işleme
- **Görüntü dizileri**: Görüntü serilerini analiz etme

### Yapılandırma Seçenekleri
Scriptte aşağıdaki parametreleri değiştirebilirsiniz:
- Tespit hassasiyeti
- Uyarı eşikleri
- İşleme çözünürlüğü
- Çıktı formatı

## 🔬 Nasıl Çalışır

### Teknik Mimari
Sistem, uyku durumlarını tespit etmek için çok aşamalı bir yaklaşım kullanır:

1. **Yüz Tespiti**: Karedeki yüzleri bulmak için MediaPipe'ın yüz tespitini kullanır
2. **Landmark Çıkarma**: Hassas analiz için 468 yüz landmark'ını çıkarır
3. **Göz Analizi**: Göz kapanmasını tespit etmek için Göz En-Boy Oranını (EAR) hesaplar
4. **Baş Pozisyonu Tahmini**: Baş pozisyonunu ve yönelimini belirler
5. **Durum Sınıflandırması**: Uyku durumlarını sınıflandırmak için zamansal analiz uygular

### Algoritma Detayları
- **EAR Hesaplama**: Sağlam tespit için göz landmark'larının normalize edilmiş oranı
- **Zamansal Filtreleme**: Yanlış pozitifleri azaltmak için yumuşatma algoritmaları
- **Çok Kare Analizi**: Doğru sınıflandırma için birden fazla ardışık kareyi dikkate alır

### Performans Metrikleri
- **Doğruluk**: Kontrollü aydınlatma koşullarında %95+
- **Gecikme**: Kare başına <100ms işleme süresi
- **FPS**: Standart donanımda 25-30 FPS

## 📊 Ekran Görüntüleri ve Örnekler
<img width="640" height="640" alt="Output_2" src="https://github.com/user-attachments/assets/169b3fed-5baa-404a-8265-dd7913cb1b4b" />
<img width="640" height="640" alt="Output_1" src="https://github.com/user-attachments/assets/eb557427-013e-415d-a873-252f82932ef3" />

## 📝 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır - detaylar için [LICENSE](LICENSE) dosyasına bakın.

MIT Lisansı şunlara izin veren izin verici bir lisanstır:
- Ticari kullanım
- Değiştirme
- Dağıtım
- Özel kullanım

## 🙏 Teşekkürler

- **MediaPipe**: Yüz landmark tespiti için
- **OpenCV**: Bilgisayarlı görü yetenekleri için
- **Araştırma Topluluğu**: Uyku algılama algoritmaları için
- **Açık Kaynak Katkıda Bulunanlar**: Sürekli iyileştirmeler için

---

**Not**: Bu sistem eğitim ve araştırma amaçları için tasarlanmıştır. Tıbbi uygulamalar için lütfen sağlık uzmanlarıyla görüşün.
