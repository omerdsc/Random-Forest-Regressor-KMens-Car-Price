## 📊 Kullanılan Veri Seti
Kaynak: Vehicle Sales Data – Kaggle

Boyut: 550.000+ araç kaydı

Kullanılan sütunlar:

Kategorik: make, model, body, transmission, color, interior

Sayısal: year, odometer

Hedef değişken: sellingprice

## 🔍 Keşifsel Veri Analizi (EDA)
Notebook dosyasında:

Eksik veriler analiz edilip mode() ve fillna() ile tamamlandı

Korelasyon matrisi ve scatter plotlar ile ilişkiler incelendi

Kategorik değişkenlerin dağılımı görselleştirildi

Özellik mühendisliğiyle km_per_year gibi ek değişkenler oluşturuldu

# 🧠 Modelleme
## 🎯 Gözetimli Öğrenme: Random Forest Regressor
Kullanılan algoritma: RandomForestRegressor (Scikit-learn)

Model ve veri ön işleme, Pipeline yapısı ile birleştirildi

Hiperparametre optimizasyonu için GridSearchCV kullanıldı:
En iyi parametreler:
{'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 5, 'n_estimators': 100}
Model Performansı (Test Verisi Üzerinde)
✅ R² Skoru: 0.914

✅ MSE :8149058.714023462

Bu değerler, modelin satış fiyatını yüksek doğrulukla tahmin ettiğini göstermektedir.

## 🧠 Gözetimsiz Öğrenme: KMeans Kümeleme
Yöntem: KMeans algoritması (Scikit-learn)

Küme sayısı k = 4 olarak seçildi (Elbow yöntemiyle)

Küme içi hata (inertia): 2,248,319.49

Küme Analizi:
Küme 0: Uygun fiyatlı, ekonomik araçlar

Küme 1: Orta segment SUV ve sedanlar

Küme 2: Lüks ve performans odaklı araçlar

Küme 3: Eski ve yüksek kilometreli araçlar

## 🌐 Web Arayüzü (Streamlit)
Kullanıcı, araç bilgilerini girerek fiyat tahmini alabilir. Web uygulaması şu girişleri alır:

Model yılı, marka, model

Kasa tipi, vites, kilometre

Dış renk, iç renk

Kullanılan Kütüphaneler:
pandas, numpy

scikit-learn

streamlit

joblib, pickle

![image](https://github.com/user-attachments/assets/31e0ac39-1cc4-4f01-b672-6ea40f58e625)
![image](https://github.com/user-attachments/assets/dd223f0f-6c3c-4c2c-ad47-a9f3e45ea6fd)


Uygulamayı Çalıştırmak İçin:
python model_egit.py
streamlit run app.py


## 📘 Kaggle Notebook
Tüm analiz süreci, model eğitimi ve hiperparametre ayarlamaları bu notebook içinde paylaşılmıştır.
🔗 https://www.kaggle.com/code/omerdasc/kmens-randomforesrregresor-vehicle-sales-data

## 📝 Projeden Çıkarımlar
Random Forest Regressor, veri setine yüksek uyum sağlamış ve başarılı tahminler yapmıştır.

KMeans ile araçları segmentlere ayırmak, pazarlama ve fiyatlandırma stratejileri için güçlü içgörüler sağlar.

Web arayüzü sayesinde model son kullanıcıya ulaşabilecek duruma getirilmiştir.

## 🚀 Gelecekte Geliştirilebilir Noktalar
Farklı algoritmalarla (XGBoost, LightGBM, CatBoost) model performansı karşılaştırılabilir.

Kümeleme için GMM veya DBSCAN gibi alternatif yöntemler denenebilir.

Kullanıcı CSV yükleyerek toplu tahmin yapabilir hale getirilebilir.

Arayüz, Streamlit Cloud gibi platformlarda deploy edilerek web'den erişilebilir hale getirilebilir.

## 🔗 Bağlantılar
📘 Kaggle Notebook : https://www.kaggle.com/code/omerdasc/kmens-randomforesrregresor-vehicle-sales-data
📘 Veri Seti : https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data

🐙 GitHub Repo: (Buraya linkini eklersin)



