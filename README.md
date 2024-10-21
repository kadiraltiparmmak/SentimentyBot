# Proje Tanıtımı: Makine Öğrenmesi ile Twitter Duygu-Durum Analizi - SentimentyBot

## Proje Amacı
SentimentyBot, Twitter kullanıcılarının duygularını analiz ederek onlara anlık moral ve motivasyon önerileri sunmayı hedeflemektedir. Proje, sosyal medya etkileşimlerini iyileştirmeyi amaçlayarak kullanıcıların ruh halini anlamalarına yardımcı olmayı hedefliyor.

## Veri Seti Bilgisi
Proje iki farklı veri seti kullanmaktadır:
- **tweets_labeled.csv**: 2022 yılına ait etiketlenmiş Türkçe tweetler (12,690 gözlem).
- **tweets_21.csv**: 2021 yılına ait etiketlenmemiş tweetler (13,272 gözlem).

## İş Problemi
Twitter kullanıcılarının duygularını pozitif, negatif ve nötr olarak sınıflandırmak.

## Görev 2: Özellik Mühendisliği ve Veri Hazırlığı

### Eksik Değer Analizi
Yalnızca bir tweet içeriği eksik olduğundan, temizlenmiş veri seti 12,959 gözlem ile analize uygun hale getirilmiştir.

### Tarih ve Zaman İşleme
Tarih bilgisi Türkiye saat dilimine (GMT+03:00) dönüştürülmüş ve mevsim, gün ile 4 saatlik periyotlar eklenmiştir.

### Hedef Değişken Analizi
Veri setinde nötr etiket %65 ile baskın durumda, pozitif etiket ise %12 gibi düşük bir orana sahiptir. Bu durum, modelin pozitif tweetlerle desteklenmesi gerektiğini göstermektedir.

### Görselleştirme
Hedef değişkenin dağılımı görselleştirilmiş, bu da veri setinin dengesini anlamaya yardımcı olmuştur.

### Genel Değerlendirme
Bu aşama, duygu analizi için sağlam bir temel oluşturmuş ve kullanıcıların ruh halini anlamak için önemli bir adım atılmıştır.

## Görev 3: Lojistik Regresyon ile Modelleme

### Veri Hazırlığı
- **Küçük Harf Dönüşümü**: Tweet içeriği küçük harfe çevrilmiştir.
- **Eksik Değer Temizliği**: Eksik değerler kaldırılmıştır.
- **TF-IDF Vektörleştirme**: TF-IDF vektörleştirici tanımlanmış ve tweet metinleri sayısal forma dönüştürülmüştür.

### Modelleme
- **Eğitim ve Test Setlerine Ayırma**: Veriler %80 eğitim ve %20 test seti olarak ayrılmıştır.
- **Lojistik Regresyon Modeli**: Model, eğitim seti ile eğitilmiş ve test setinde tahminler yapılmıştır. Elde edilen doğruluk oranı: %71.03.

## Yeni Tweet Verisinin Hazırlığı ve Değerlendirme

### Veri Kontrolü ve Etiket Analizi
Yeni veri seti okunmuş ve rastgele etiketler eklenmiştir.
- **Etiket dağılımı**: 
  - Negatif: 4,523 
  - Pozitif: 4,390 
  - Nötr: 4,359
- Boş etiket sayıları kontrol edilmiş, her iki durumda da sonuç 0 olarak bulunmuştur.

### Sonuçların Kontrolü
Yeni tweet verisi kontrol edilmiş ve modelin genel doğruluğu %80.56 olarak hesaplanmıştır.

## Genel Değerlendirme
Proje, duygu analizi sürecinde veri hazırlama ve Lojistik Regresyon modeli oluşturma aşamalarını başarıyla tamamlamıştır. Modelin elde ettiği %71.03 ve %80.56 doğruluk oranları, temel bir Lojistik Regresyon modeli için makul bir performans göstermektedir.

## İyileştirme Alanları
Hatalı tahminlerin analizi, modelin optimize edilmesi ve hiperparametre ayarlamaları yapılması gerektiğini göstermektedir. Proje ilerleyen aşamalarda, modelin daha iyi genelleme yapabilmesi için bu yönlere odaklanmayı planlamaktadır.

## Sonuç
SentimentyBot projesi, sosyal medya kullanıcılarının duygusal durumlarını anlamalarına yardımcı olmayı hedefleyen etkili bir makine öğrenmesi uygulamasıdır. Proje, kullanıcıların ruh halini iyileştirmek amacıyla öneriler sunarak sosyal medya etkileşimlerini olumlu yönde geliştirmeyi hedefliyor.

