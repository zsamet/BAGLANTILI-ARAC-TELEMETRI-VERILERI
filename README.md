# BAĞLANTILI ARAÇ TELEMETRİ VERİLERİ
# Unsupervised Anomaly Detection on Connected Car Telemetry Data 🚗📊
> **A Dual-Model Architecture for Driver Risk Profiling and Predictive Maintenance**

Bu proje, bağlantılı araçlardan (connected cars) elde edilen yüksek frekanslı ve etiketsiz telemetri verileri üzerinden, **Sürücü Risk Skorlaması** ve **Kestirimci Bakım (Predictive Maintenance)** analizleri gerçekleştiren gözetimsiz bir makine öğrenmesi (Unsupervised Machine Learning) mimarisidir.

## 🎯 Projenin Amacı ve İş Değeri (Business Value)
Geleneksel filo yönetim sistemleri, arıza gerçekleştikten sonra devreye giren reaktif bir yapıya sahiptir. Bu proje, "İkili Model Mimarisi" (Dual-Model Architecture) kullanarak:
- Operasyonel (downtime) bakım maliyetlerini sıfırlamayı,
- "Nasıl Kullanıyorsan Öyle Öde" tabanlı dinamik kasko/risk primi hesaplamasını mümkün kılmayı,
- Geleceğin Otonom Yapay Zeka Ajanları (AI Agents) için eyleme geçirilebilir (actionable) bir veri temeli sunmayı hedeflemektedir.

## 🧠 İkili Model Mimarisi (Dual-Model Architecture)
Proje kapsamında, `Scikit-Learn` kütüphanesinin **Isolation Forest (İzolasyon Ormanı)** algoritması kullanılarak birbirinden bağımsız iki farklı anomali tespiti modeli kurgulanmıştır:

### 1. Model: Sürücü Riski ve Davranış Skorlama Modeli
* **Kullanılan Değişkenler:** `Hız (speed)`, `İvme (acceleration)`, `Fren Durumu (brakePedalIndicator)`
* **Tespit Edilen Anomaliler:** Otoyol hızlarında panik frenleme, şehir içi agresif kalkışlar ve takip mesafesi ihlalleri.
* **Çıktı:** Filo sürücüleri için 3 boyutlu analiz uzayında risk skorlaması.

### 2. Model: Kestirimci Bakım ve Mekanik Sağlık Modeli
* **Kullanılan Değişkenler:** `Hız (speed)`, `Motor Devri (engineRpm)`, `Motor Sıcaklığı (engineTemperature)`, `Soğutma Suyu (coolTemp)`
* **Tespit Edilen Anomaliler:** Düşük hız/rölanti durumlarında yükselen termal yükler (gizli hararet riski) ve şanzıman/aktarma organı zorlanmaları.
* **Çıktı:** Motor yatak sarması veya conta yanması gibi ağır arızalar gerçekleşmeden önce üretilen erken uyarı skorları.

## 🛠️ Kullanılan Teknolojiler
- **Veri İşleme & Analiz:** `Python`, `Pandas`, `NumPy`
- **Makine Öğrenmesi:** `Scikit-Learn` (Isolation Forest)
- **Büyük Veri Ortamı:** `Databricks` (Log işleme ve analiz)
- **Veri Görselleştirme:** `Plotly` (3D Etkileşimli Scatter Plot grafikleri)

## 👨‍💻 Geliştirici
**Samet Çevik** 
*Yönetim Bilişim Sistemleri*
