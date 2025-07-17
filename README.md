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

## Klasör Yapısı

- `video_isleme.py` – Video dosyasından analiz yapan fonksiyon  
- `kamera_analiz.py` – Canlı kameradan analiz (gerçek zamanlı)  
- `garson_fotograflari/` – Garson yüz görselleri (.jpg/.png)  
- `food_yolo_best.pt` – YOLOv8 yemek tanıma modeli  
- `loglar.csv` – Otomatik oluşturulan analiz çıktısı  

---

## Kullanım

### Video dosyasını analiz etmek için

Python ortamında şu şekilde kullanabilirsin:

```python
from video_isleme import process_video
process_video("ornek_video.mov")  # veya .mp4

