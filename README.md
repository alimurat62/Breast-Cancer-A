# Proje Özeti: 
Breast Cancer Classification with Deep Learning ve Makine Öğrenimi Modelleri Performans Değerlendirmesi
Bu proje, meme kanseri sınıflandırma problemini çözmek amacıyla farklı makine öğrenimi modellerinin performansını analiz etmekte ve derin öğrenme yaklaşımıyla elde edilen sonuçları değerlendirmektedir. 
İki veri setiyle çalışılmıştır: Özellik seçimi yapılmış bir set (İlk Set) ve tüm özelliklerin kullanıldığı bir set (İkinci Set).
Proje, meme kanseri sınıflandırmasında derin öğrenme ve geleneksel makine öğrenimi yöntemlerinin etkinliğini kıyaslamak için önemli bir çalışma ortaya koymaktadır.


# Model Performans Değerlendirmesi

Bu belge, çeşitli makine öğrenimi modellerinin performans değerlendirmesini ve Breast Cancer Classification with Deep Learning modeli üzerine yapılan analizleri içermektedir.

## Genel Performans
- **İLK SET = Ozellik_Secme_Makine_Öğrenmesi
- **İKİNCİ SET = Tum_Ozellikler_Makine_Öğrenmesi

### Lojistik Regresyon (log):
- **İlk set:** %96.49 doğruluk, AUC = 0.995
- **İkinci set:** %98.25 doğruluk, AUC = 0.997
- **Yorum:** Lojistik regresyon ikinci set için daha iyi performans gösteriyor. Doğruluk ve AUC değeri daha yüksek.

### Karar Ağacı (tree):
- **İlk set:** %94.15 doğruluk, AUC = 0.937
- **İkinci set:** %94.15 doğruluk, AUC = 0.944
- **Yorum:** Karar ağacı modelinin doğruluğu her iki sette de aynı, ancak AUC değeri ikinci sette biraz daha yüksek.

### Rastgele Orman (forest):
- **İlk set:** %95.91 doğruluk, AUC = 0.991
- **İkinci set:** %97.08 doğruluk, AUC = 0.996
- **Yorum:** Rastgele orman modelinin ikinci sette daha yüksek doğruluk ve AUC değerlerine sahip olduğu görülüyor.

### K-En Yakın Komşu (kneigh):
- **İlk set:** %95.32 doğruluk, AUC = 0.978
- **İkinci set:** %95.91 doğruluk, AUC = 0.976
- **Yorum:** K-en yakın komşu modelinin performansı her iki sette de oldukça benzer, doğruluk oranları arasında çok küçük bir fark var, ancak AUC ilk sette biraz daha yüksek.

## Sınıflandırma Raporları (Precision, Recall, F1-Score)

### Lojistik Regresyon:
- Her iki sette de 0 sınıfı için yüksek recall (ilk set %97, ikinci set %98) ve 1 sınıfı için yüksek precision (ilk set %98, ikinci set %99) değerleri bulunuyor.
- **F1-Skorları:** Her iki set için de çok yakın, genelde çok yüksek.
- **Yorum:** Lojistik regresyon, özellikle sınıf dengesini iyi bir şekilde yakalayan bir modeldir ve ikinci sette daha iyi sonuçlar elde edilmiştir.

### Karar Ağacı:
- **0 sınıfı için:** Precision ve recall değerleri oldukça düşük (ilk set: precision %92, recall %92; ikinci set: precision %90, recall %95).
- **1 sınıfı için:** Yüksek (ilk set: precision %95, recall %94; ikinci set: precision %97, recall %94).
- **F1-Skoru:** Her iki set için de 1 sınıfı daha yüksek performans gösteriyor.
- **Yorum:** Karar ağacı modeli, 0 sınıfında tam olarak güçlü değil ancak 1 sınıfını oldukça iyi sınıflandırıyor. AUC değeri de nispeten daha düşük.

### Rastgele Orman:
- **0 sınıfı için:** Precision ve recall değerleri çok yakın.
- **1 sınıfı için:** Oldukça yüksek precision ve recall (ilk set: precision %96, recall %97; ikinci set: precision %96, recall %99).
- **Yorum:** Rastgele orman modeli, her iki sınıf için de yüksek performans sağlıyor, ancak 1 sınıfı daha doğru sınıflandırılmış.

### K-En Yakın Komşu:
- **0 sınıfı için:** Precision ve recall değerleri oldukça yüksek (ilk set: precision %94, recall %94; ikinci set: precision %95, recall %94).
- **1 sınıfı için:** Yüksek precision ve recall (ilk set: precision %96, recall %96; ikinci set: precision %96, recall %97).
- **Yorum:** K-en yakın komşu modeli oldukça dengeli bir performans sergiliyor, her iki sınıf için de yüksek doğruluk sağlıyor.

## Karışıklık Matrisi (Confusion Matrix)

### Lojistik Regresyon:
- **İlk set:** 
  - 0 sınıfı: 61 doğru sınıflandırma, 2 yanlış sınıflandırma
  - 1 sınıfı: 104 doğru sınıflandırma, 4 yanlış sınıflandırma
- **İkinci set:** 
  - 0 sınıfı: 62 doğru sınıflandırma, 1 yanlış sınıflandırma
  - 1 sınıfı: 106 doğru sınıflandırma, 2 yanlış sınıflandırma
- **Yorum:** Lojistik regresyon çok az hata yapıyor ve ikinci sette mükemmel sınıflandırma sağlıyor.

### Karar Ağacı:
- **İlk set:** 
  - 0 sınıfı: 58 doğru sınıflandırma, 5 yanlış sınıflandırma
  - 1 sınıfı: 103 doğru sınıflandırma, 5 yanlış sınıflandırma
- **İkinci set:** 
  - 0 sınıfı: 60 doğru sınıflandırma, 3 yanlış sınıflandırma
  - 1 sınıfı: 101 doğru sınıflandırma, 7 yanlış sınıflandırma
- **Yorum:** Karar ağacının doğruluğu biraz daha düşük, 1 sınıfını sınıflandırırken bazı yanlış sınıflandırmalar mevcut.

### Rastgele Orman:
- **İlk set:** 
  - 0 sınıfı: 59 doğru sınıflandırma, 4 yanlış sınıflandırma
  - 1 sınıfı: 105 doğru sınıflandırma, 3 yanlış sınıflandırma
- **İkinci set:** 
  - 0 sınıfı: 59 doğru sınıflandırma, 4 yanlış sınıflandırma
  - 1 sınıfı: 107 doğru sınıflandırma, 1 yanlış sınıflandırma
- **Yorum:** Rastgele orman modelinde oldukça düşük hata oranları, ikinci sette mükemmel sonuçlar.

### K-En Yakın Komşu:
- **İlk set:** 
  - 0 sınıfı: 59 doğru sınıflandırma, 4 yanlış sınıflandırma
  - 1 sınıfı: 104 doğru sınıflandırma, 4 yanlış sınıflandırma
- **İkinci set:** 
  - 0 sınıfı: 59 doğru sınıflandırma, 4 yanlış sınıflandırma
  - 1 sınıfı: 105 doğru sınıflandırma, 3 yanlış sınıflandırma
- **Yorum:** K-en yakın komşu modeli de oldukça iyi performans sergiliyor, ancak doğruluğu diğer modellere göre biraz daha düşük.

## Sonuçlar:
- **En iyi performansı gösteren model:** Lojistik regresyon ikinci set için yüksek doğruluk ve AUC değerlerine sahip.
- **En dengeli model:** K-en yakın komşu, her iki sınıfı da yüksek doğrulukla sınıflandırıyor.
- **En güçlü model 1 sınıfı için:** Rastgele orman, özellikle 1 sınıfında çok iyi bir sonuç veriyor.


## Breast Cancer Classification with Deep Learning Model

### Genel Performans:
- **Doğruluk (Accuracy):** Modelin doğruluk oranı %97.66. Bu, modelin test verilerinde %97.66 doğru tahminler yaptığı anlamına geliyor.

### Confusion Matrix (Karışıklık Matrisi):
- **Malignant (0) sınıfı:** 61 doğru tahmin (true negatives), 2 yanlış tahmin (false positives).
- **Benign (1) sınıfı:** 106 doğru tahmin (true positives), 2 yanlış tahmin (false negatives).
- **Yorum:** Model her iki sınıfı da oldukça doğru bir şekilde sınıflandırmıştır.

### ROC-AUC (Receiver Operating Characteristic - Area Under Curve):
- ROC-AUC değeri 0.9966. Model oldukça iyi bir ayrım gücüne sahiptir. 

### Log Loss:
- Log loss değeri 0.0552. Bu değer, modelin doğruluğunun yüksek olduğunu ve sınıflandırma hatalarının oldukça küçük olduğunu göstermektedir.

### Sınıflandırma Raporu (Classification Report):
- **Precision:** Benign sınıfı için %98, Malignant sınıfı için %97.
- **Recall:** Benign sınıfı için %98, Malignant sınıfı için %97.
- **F1-Score:** 0 sınıfı için 0.97, 1 sınıfı için 0.98. Bu değerler, modelin dengeli bir performans sergilediğini göstermektedir.

### Sonuçlar:
- Model yüksek doğruluk, iyi bir ROC-AUC değeri ve düşük log loss ile oldukça iyi performans göstermiştir.
- Hem precision hem de recall değerlerinin yüksek olması, modelin sınıflandırma hatalarını minimize ettiğini ve her iki sınıfı da doğru şekilde ayırt ettiğini gösterir.
