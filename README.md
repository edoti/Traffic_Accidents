# 🚗 UK Trafik Kazaları (2005–2014) Veri Analizi ve Kaza Tahmini

Bu projede, Birleşik Krallık'ta 2005–2014 yılları arasında gerçekleşen trafik kazalarına ait veriler analiz edilmiştir. Üç farklı CSV dosyasındaki kaza verileri birleştirilmiş ve görselleştirme, istatistiksel analiz ve regresyon modelleri ile kaza nedenleri ve tahminleri incelenmiştir.

## 📁 Veri Seti
Veri, Kaggle üzerinden sağlanmıştır:  
🔗 [2000-16 Traffic Flow England Scotland Wales](https://www.kaggle.com/daveianhickey/2000-16-traffic-flow-england-scotland-wales)

Kullanılan dosyalar:
- `accidents_2005_to_2007.csv`
- `accidents_2009_to_2011.csv`
- `accidents_2012_to_2014.csv`

Veriler `Accident_Index` üzerinden birleştirilebilecek şekilde yapılandırılmıştır. Ancak bu çalışmada yalnızca **accidents** dosyaları kullanılmıştır.

## 🎯 Projenin Amacı

Aşağıdaki sorulara veri bilimi yöntemleri ile yanıt aranmıştır:
- Trafik akışının değişmesi kazaları nasıl etkiler?
- Kaza oranlarını ne artırır?
- Zaman içinde kaza oranlarını tahmin edebilir miyiz?
- Kırsal ve kentsel alanlar nasıl farklılık gösteriyor?

---

## 🔍 Uygulanan Adımlar

### 1. 📚 Veri Birleştirme ve Temizleme
- Farklı yıllara ait CSV dosyaları Pandas `concat()` fonksiyonu ile birleştirildi.
- `Date` sütunu datetime formatına çevrildi.
- Eksik veriler ve aykırı değerler kontrol edildi.

### 2. 📊 Veri Keşfi (EDA)
- Aylara, yıllara, hava durumuna, yol tipine göre kazalar incelendi.
- Kırsal ve kentsel alanlardaki farklılıklar karşılaştırıldı.
- Bar grafikleri, histogramlar ve heatmap'ler kullanıldı.

### 3. 📈 Regresyon ile Zaman Serisi Tahmini
- Kazalar aylık olarak gruplandı.
- Eğitim ve test setleri oluşturuldu.
- Lineer regresyon modeli eğitildi.
- Aylık bazda tahmin yapıldı ve `RMSE` manuel olarak hesaplandı.

---

## 📌 Kullanılan Kütüphaneler

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 📉 Model Performansı

Regresyon Modeli ile Aylık Kaza Sayısı Tahmini:

- Kullanılan metrik: **Root Mean Squared Error (RMSE)**
- Test setindeki tahmin başarısı: `RMSE ≈ ...` *(çalıştırılan versiyona göre yazılmalı)*

---

## 📅 Yayınlanan Kaza Sayısı (Zaman Analizi)

![](gorsel_gelirse_eklenebilir.png)

---

## 📝 Notlar

- Bu çalışma temel düzeyde analiz ve tahminler içermektedir.
- Model geliştirilebilir: ARIMA, Facebook Prophet gibi daha gelişmiş zaman serisi yöntemleri kullanılabilir.
- Trafik yoğunluğu, hava durumu ve sürücü hataları gibi etmenlerin etkisi daha derin analizlerle ortaya konabilir.

---

## 📂 Projeyi Çalıştırmak

1. Gerekli kütüphaneleri yükleyin:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
