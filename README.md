# Garson-Yemek Takip Sistemi 

Bu proje, bir restoranda masalara gelen yemeklerin kamera görüntüsü üzerinden otomatik olarak tanınmasını ve loglanmasını sağlar. Sistem:

- QR kod ile masa tanıma  
- Yüz tanıma ile garson belirleme (isteğe bağlı)  
- YOLOv8 ile yemek sınıflandırma  
- Ürün fiyatları ile hesap toplama  
- `loglar.csv` çıktısı üretme

Bu sistem **web arayüzü olmadan**, doğrudan **VS Code veya terminal üzerinden** çalışacak şekilde yapılandırılmıştır.

---

## Özellikler

- Terminalde çalışır, web sunucusu gerekmez  
- `.mov` ve `.mp4` videolarla analiz yapar  
- Canlı kamera ile anlık analiz yapılabilir  
- Masa, garson, yemek ve hesap bilgilerini `loglar.csv` dosyasına yazar  
- Jupyter Notebook ile uyumludur (face_recognition destekli)

---

# Garson-Yemek Takip Sistemi (Terminal Uygulaması)

Bu proje, bir restoranda masalara gelen yemeklerin kamera görüntüsü üzerinden otomatik olarak tanınmasını ve loglanmasını sağlar. Sistem:

- QR kod ile masa tanıma  
- Yüz tanıma ile garson belirleme (isteğe bağlı)  
- YOLOv8 ile yemek sınıflandırma  
- Ürün fiyatları ile hesap toplama  
- `loglar.csv` çıktısı üretme

Bu sistem **web arayüzü olmadan**, doğrudan **VS Code veya terminal üzerinden** çalışacak şekilde yapılandırılmıştır.

---

## Özellikler

- Terminalde çalışır, web sunucusu gerekmez  
- `.mov` ve `.mp4` videolarla analiz yapar  
- Canlı kamera ile anlık analiz yapılabilir  
- Masa, garson, yemek ve hesap bilgilerini `loglar.csv` dosyasına yazar  
- Jupyter Notebook ile uyumludur (face_recognition destekli)

---

## Klasör Yapısı

- `video_isleme.py` – Video dosyasından analiz yapan fonksiyon  
- `kamera_analiz.py` – Canlı kameradan analiz (gerçek zamanlı)  
- `garson_fotograflari/` – Garson yüz görselleri (.jpg/.png)  
- `food_yolo_best.pt` – YOLOv8 yemek tanıma modeli  
- `loglar.csv` – Otomatik oluşturulan analiz çıktısı  

---

## Kurulum

### 1. Ortam oluştur (opsiyonel)

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

2.Gerekli kütüphaneleri kur
```bash
pip install opencv-python face_recognition dlib pyzbar ultralytics numpy
Mac kullanıcıları ayrıca şunu kurmalı:

brew install cmake boost boost-python zbar

Çıktı: loglar.csv dosyası otomatik olarak oluşturulur.

3.Canlı kamera ile çalıştırmak için:
python kamera_analiz.py

---




