# 🛍️ Customer Segmentation for Retail Strategies

Segmenting retail customers with RFM analysis and unsupervised clustering to drive targeted marketing strategies.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Clustering-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## 📈 Overview

Not all customers are equal. This project groups customers by their purchasing behavior so a retailer can tailor campaigns — rewarding loyal high-spenders, re-engaging those who are slipping away, and nurturing newcomers.

## 📊 Dataset

**Online Retail** transactional data (`OnlineRetail.csv`) — invoices, dates, quantities, prices and customer IDs from an online store.

## 🧠 Approach

1. **Cleaning** — drop rows without a `CustomerID`, parse invoice dates.
2. **RFM feature engineering** — compute **Recency** (days since last purchase), **Frequency** (number of orders) and **Monetary** (total spend) per customer.
3. **Scaling** — standardize features with `StandardScaler`.
4. **Clustering** — apply and compare **K-Means** and **DBSCAN**.
5. **Evaluation & viz** — assess cluster quality with the **silhouette score**; reduce to 2D with **PCA** for visualization.

## 🛠️ Tech Stack

`Python` · `pandas` · `numpy` · `scikit-learn` (KMeans, DBSCAN, PCA, silhouette) · `matplotlib` · `seaborn`

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook CustomerSegmentationforRetailStrategies.ipynb
```

Update the `OnlineRetail.csv` path at the top of the notebook, then run all cells.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Her müşteri aynı değildir. Bu proje, müşterileri satın alma davranışlarına göre gruplayarak perakendecinin kampanyalarını kişiselleştirmesini sağlar — sadık yüksek harcayanları ödüllendirmek, uzaklaşanları geri kazanmak ve yeni gelenleri büyütmek.

### Veri Seti
**Online Retail** işlem verisi (`OnlineRetail.csv`) — bir çevrimiçi mağazaya ait faturalar, tarihler, miktarlar, fiyatlar ve müşteri kimlikleri.

### Yaklaşım
1. **Temizlik** — `CustomerID` olmayan satırları at, fatura tarihlerini ayrıştır.
2. **RFM öznitelikleri** — müşteri başına **Recency** (son alışverişten bu yana geçen gün), **Frequency** (sipariş sayısı) ve **Monetary** (toplam harcama).
3. **Ölçekleme** — `StandardScaler` ile standartlaştırma.
4. **Kümeleme** — **K-Means** ve **DBSCAN** uygulanıp karşılaştırılır.
5. **Değerlendirme & görselleştirme** — küme kalitesi **silhouette skoru** ile ölçülür; **PCA** ile 2B'ye indirgenip görselleştirilir.

### Teknolojiler
`Python` · `pandas` · `numpy` · `scikit-learn` · `matplotlib` · `seaborn`

### Çalıştırma
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook CustomerSegmentationforRetailStrategies.ipynb
```
Notebook'un başındaki `OnlineRetail.csv` yolunu güncelle ve tüm hücreleri çalıştır.
