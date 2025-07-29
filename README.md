# Garson-Yemek Takip Sistemi 

Bu proje, bir restoranda masalara gelen yemeklerin kamera görüntüsü üzerinden otomatik olarak tanınmasını ve loglanmasını sağlar. Sistem:

- QR kod ile masa tanıma  
- Yüz tanıma ile garson belirleme 
- YOLOv8 ile yemek sınıflandırma  
- Ürün fiyatları ile hesap toplama  
- `loglar.csv` çıktısı üretme

Bu sistem **web arayüzü olmadan**, doğrudan **VS Code veya terminal üzerinden** çalışacak şekilde yapılandırılmıştır.

---

## Özellikler

- Terminalde çalışır, web sunucusu gerekmez  
- `.mov` ve `.mp4` videolarla analiz yapar    
- Masa, garson, yemek ve hesap bilgilerini `loglar.csv` dosyasına yazar  
- Jupyter Notebook ile uyumludur (face_recognition destekli)

---

## Klasör Yapısı

- `Untitled-1.ipynb` – Video dosyasından analiz yapan fonksiyon  
- `garson_fotograflari/` – Garson yüz görselleri (.jpg/.png)  
- `food_yolo_best.pt` – YOLOv8 yemek tanıma modeli  
- `loglar.csv` – Otomatik oluşturulan analiz çıktısı  

---

## Kurulum

### 1. Ortam oluştur (opsiyonel)

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
 ``` 

### 2.Gerekli kütüphaneleri kur

```bash
pip install opencv-python face_recognition dlib pyzbar ultralytics numpy
Mac kullanıcıları ayrıca şunu kurmalı:

brew install cmake boost boost-python zbar
 ```
### Çıktılar
- loglar.csv dosyası otomatik olarak oluşturulur.


Tüm klasöre ulaşmak isterseniz: https://drive.google.com/drive/folders/1LPISDUsLo7ex6MDnYsUwJJwMV-ilMFTT?usp=sharing

Projenin anlatıldığını ve denendiği Youtube videosu: https://www.youtube.com/watch?v=3sq2HrR0we4

 
