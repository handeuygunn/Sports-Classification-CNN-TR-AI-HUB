# 🏋️‍♂️ Sports Classification with Deep Learning (CNN)

Bu proje, farklı spor dallarını sınıflandırmak için sıfırdan geliştirilmiş bir **Convolutional Neural Network (CNN)** modelini içermektedir. Eğitim sürecinde veri artırma (data augmentation), callback mekanizmaları ve model kaydetme adımları kullanılmıştır.  

---

## 📌 Özellikler

- **Veri Hazırlama**
  - `ImageDataGenerator` ile eğitim verisine data augmentation (zoom, kaydırma, döndürme, yatay çevirme).
  - Validasyon ve test verisine yalnızca `rescale`.

- **CNN Mimarisi**
  - `Conv2D`, `BatchNormalization`, `ReLU` katmanlarıyla özellik çıkarımı.
  - `MaxPooling2D` ile boyut küçültme.
  - `GlobalAveragePooling2D` ve `Dense` katmanlarıyla sınıflandırma.
  - Aşırı öğrenmeyi azaltmak için `Dropout`.

- **Derleme ve Eğitim**
  - Optimizasyon: `Adam (lr=3e-4)`
  - Loss fonksiyonu: `categorical_crossentropy`
  - Metrik: `accuracy`
  - Callback’ler:
    - `EarlyStopping` (patience=5, restore_best_weights=True)
    - `ReduceLROnPlateau` (factor=0.5, patience=3)

- **Sonuçlar**
  - Eğitim/Doğrulama doğruluk grafikleri.
  - Test seti kayıp ve doğruluk değerleri. %81 doğruluk değerine sahip.
  - Eğitim sonrası model `.h5` formatında kaydedilir.

---

## 🚀 Çalıştırma

https://www.kaggle.com/code/handeuygun/sports-classification-ai-hub-deeplearning-cnn
