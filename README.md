# 🛍️ Customer Segmentation for Retail Strategies

Turning **500K+ online-retail transactions** into named customer segments with RFM scoring and unsupervised clustering.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-KMeans%20%7C%20DBSCAN-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## 📈 Overview

A UK online gift shop wants to treat customers differently based on **how recently, how often, and how much** they buy. This project builds those segments two complementary ways — rule-based **RFM scoring** and unsupervised **clustering** — so marketing can target each group.

## 📊 Dataset

**Online Retail** (`OnlineRetail.csv`) — real transactions from a UK-based online retailer (2010–2011): `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`. Rows without a `CustomerID` are dropped and only customers with positive spend are kept.

## 🧠 Approach

1. **RFM engineering** — per customer: **Recency** (days since last order, relative to a snapshot date), **Frequency** (unique invoices), **Monetary** (total spend = Quantity × UnitPrice).
2. **RFM scoring** — each dimension bucketed into **1–5 quintiles** with `qcut`.
3. **Rule-based segments** — regular expressions on the RFM score map customers to named segments: **Champions, Loyal Customers, Potential Loyalists, New Customers, At Risk, Cannot Lose Them, Lost**.
4. **Clustering** — `StandardScaler` + **K-Means** and **DBSCAN**; cluster quality judged by the **silhouette score**, and **PCA** projects the clusters to 2D for visualization.

## 🛠️ Tech Stack

`Python` · `pandas` · `numpy` · `scikit-learn` (KMeans, DBSCAN, PCA, silhouette_score) · `matplotlib` · `seaborn`

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook CustomerSegmentationforRetailStrategies.ipynb
```

Set the `OnlineRetail.csv` path near the top of the notebook, then run all cells.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
İngiltere merkezli bir çevrimiçi hediyelik mağaza, müşterilerini **ne kadar yakın zamanda, ne sıklıkta ve ne kadar** alışveriş yaptıklarına göre farklı ele almak ister. Bu proje bu segmentleri iki tamamlayıcı yolla kurar — kural tabanlı **RFM skorlaması** ve gözetimsiz **kümeleme**.

### Veri Seti
**Online Retail** (`OnlineRetail.csv`) — İngiltere merkezli bir perakendecinin gerçek işlemleri (2010–2011): `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`. `CustomerID` olmayan satırlar atılır, yalnızca pozitif harcamalı müşteriler tutulur.

### Yaklaşım
1. **RFM öznitelikleri** — müşteri başına **Recency** (anlık tarihe göre son siparişten geçen gün), **Frequency** (benzersiz fatura sayısı), **Monetary** (toplam harcama = Quantity × UnitPrice).
2. **RFM skorlama** — her boyut `qcut` ile **1–5 beşli dilime** ayrılır.
3. **Kural tabanlı segmentler** — RFM skoruna uygulanan düzenli ifadelerle müşteriler isimli segmentlere atanır: **Champions, Loyal Customers, Potential Loyalists, New Customers, At Risk, Cannot Lose Them, Lost**.
4. **Kümeleme** — `StandardScaler` + **K-Means** ve **DBSCAN**; küme kalitesi **silhouette skoru** ile ölçülür, **PCA** ile kümeler 2B'ye yansıtılıp görselleştirilir.

### Teknolojiler
`Python` · `pandas` · `numpy` · `scikit-learn` · `matplotlib` · `seaborn`

### Çalıştırma
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook CustomerSegmentationforRetailStrategies.ipynb
```
Notebook'un başındaki `OnlineRetail.csv` yolunu ayarla ve tüm hücreleri çalıştır.
