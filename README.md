# DefectVision: NEU Metal Yüzey Hataları Sınıflandırıcı

![Python](https://img.shields.io/badge/Python-3.11-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15-orange)
![Accuracy](https://img.shields.io/badge/Accuracy-94.63%25-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

## Proje Özeti
Akbank Derin Öğrenme Bootcamp kapsamında geliştirilen bu proje, CNN mimarisi kullanarak endüstrideki metallerin yüzeylerinde oluşan hataları **%94.63 doğruluk** oranıyla sınıflandırmaktadır.

## Proje Amacı
-  Endüstriyel kalite kontrol için otomatik hata tespiti
-  Derin öğrenme modellerinin endüstriyel uygulamaları
-  CNN mimarilerinin performans değerlendirmesi

## 📈 Sonuçlar
| Metric | Value |
|--------|-------|
| Test Accuracy | 94.63% |
| Training Accuracy | 85.62% |
| Validation Accuracy | 90.56% |
| Overfitting | Yok ✅ |

### Sınıf Bazlı Performans
| Defect Type | Accuracy | Samples |
|-------------|----------|---------|
| Crazing | 100.0% | 90 |
| Inclusion | 100.0% | 90 |
| Patches | 98.9% | 90 |
| Pitted | 98.9% | 90 |
| Rolled | 100.0% | 90 |
| Scratches | 100.0% | 90 |

##  Model Mimarisi
```python
Model: "DefectVision_CNN"
├── Conv2D(32, (3,3)) + BatchNormalization + Dropout(0.3)
├── Conv2D(64, (3,3)) + BatchNormalization + Dropout(0.4)
├── Flatten()
├── Dense(128) + Dropout(0.5)
└── Dense(6, activation='softmax')

##  Veri Seti
Dataset: NEU Metal Surface Defects Data
Total Images: 1,800
Classes: 6
Image Size: 200x200 pixels

```

https://www.kaggle.com/code/aykansoydan/d3fectvision
https://www.kaggle.com/code/yamuryavuz77/ai-powered-industrial-quality-control
