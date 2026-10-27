# 📊 Olist Sales Performance Analysis

Analisis kinerja penjualan, faktor pertumbuhan, dan peluang pengembangan bisnis pada marketplace e-commerce Brasil, Olist, menggunakan **Python** dan **Tableau**.

![Olist Sales Performance Dashboard](Olist%20_%20Sales%20Performance.png)

🔗 **[Lihat dashboard interaktif di Tableau Public](https://public.tableau.com/views/OlistSalesPerformance_17903497974360/OlistSalesPerformance)**

---

## 📌 Latar Belakang
Olist adalah marketplace yang menghubungkan seller dengan pelanggan di seluruh Brasil. Proyek ini menganalisis transaksi historis Olist untuk membantu tim Commercial dan Management menentukan **kategori, seller, dan wilayah** yang layak diprioritaskan.

## ❓ Problem Statement
> Bagaimana Olist meningkatkan Revenue dan Orders sebesar **10% pada 2027** dibanding baseline historis (Jan–Jul 2018), melalui kategori, seller, dan wilayah terbaik, lalu mempertahankannya hingga 2029?

*Target 10% adalah sasaran bisnis, bukan prediksi.*

## 🧪 Hipotesis
| Kode | Hipotesis |
|---|---|
| H1 | Revenue berbeda antarperiode dan terkonsentrasi pada kategori, seller, serta wilayah tertentu |
| H2 | Kontribusi orders berbeda antarsegmen |
| H3 | AOV berbeda antarperiode dan segmen |

## 📂 Dataset
- **Sumber:** [Brazilian E-Commerce Public Dataset by Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Tabel:** 9 tabel sumber, 7 dipakai (orders, order_items, order_payments, customers, sellers, products, category_translation)
- **Cakupan analisis:** completed orders, 01 Jan 2017 – 29 Agu 2018
- **Definisi Revenue:** nilai produk terjual (bukan komisi atau laba Olist)

## 🛠️ Tools
- **Python (Google Colab):** Pandas, Matplotlib, Seaborn untuk data cleaning, merging, dan EDA
- **Tableau:** dashboard interaktif

## 🔄 Metodologi
1. **Business Problem:** problem statement, DARCI, issue tree, hipotesis, dan KPI
2. **Data Preparation:** cleaning, agregasi payment, merge, dan validasi
3. **Exploratory Analysis:** tren, perbandingan periode, kontribusi kategori, seller, dan state
4. **Visualization:** dashboard Tableau
5. **Business Recommendation:** insight, aksi, PIC, KPI evaluasi, dan jadwal

### Data Cleaning (ringkasan)
- 610 kategori produk kosong diisi `unknown`; 2 kategori tanpa terjemahan dipetakan manual
- Kode state customer dan seller distandarisasi (trim & uppercase)
- Timestamp dikonversi ke datetime, fitur waktu ditambahkan (year, month, month_year)
- 103.886 baris payment diagregasi menjadi 99.440 order
- Hanya **completed orders** yang dianalisis (2.963 order non-completed dikeluarkan)
- **Outlier tetap dipertahankan** sebagai transaksi valid: 14.400 order (14,93%) menyumbang 44,59% revenue. Winsorization hanya dipakai untuk sensitivity analysis.

## 📈 KPI Utama
| Metric | Nilai |
|---|---|
| Total Revenue | R$13,18 juta |
| Total Orders | 96.211 |
| Average Order Value (AOV) | R$137,00 |
| Total Units | 109.880 |

## 💡 Insight Utama
1. **Pertumbuhan didorong volume order.** Revenue Jan–Jul 2018 naik **161,59%** dibanding Jan–Jul 2017, orders naik **160,78%**, sedangkan AOV hanya naik **0,31%**.
2. **Puncak penjualan pada November 2017**, dengan revenue R$987,8 ribu dan 7.289 orders.
3. **Revenue terkonsentrasi pada 5 kategori teratas (39,88%)**, dipimpin Health & Beauty. Watches & Gifts memiliki AOV tertinggi di antara kategori utama (±R$211,89).
4. **Seller:** 10 seller teratas menyumbang 13,27% revenue, dan 533 seller menghasilkan 80% total revenue.
5. **Wilayah:** SP, RJ, dan MG menyumbang **63,39%** revenue; SP sendiri R$5,06 juta.

## ✅ Rekomendasi
| Prioritas | Fokus | Rekomendasi | Target |
|---|---|---|---|
| High | Order volume & kategori utama | Commercial meninjau stok dan seller 5 kategori teratas (Q1 2027) | Orders kategori +10% |
| Medium | Basket size (AOV) | Uji bundle / cross-sell di kategori utama (Q2–Q3 2027) | AOV +5%, orders tidak turun |
| Medium | Diversifikasi wilayah | Pilot satu state di luar SP/RJ/MG dengan kontrol freight (Q1–Q3 2027) | Revenue & orders +10% |

**Monitoring:** KPI dilaporkan bulanan, dievaluasi pada Q4 2027, lalu per kuartal pada 2028–2029.

## ⚠️ Limitasi
- Data 2016–2018 hanya acuan historis; perlu validasi dengan data terbaru sebelum eksekusi.
- Data biaya belum lengkap untuk menilai margin/profitabilitas.
- Analisis bersifat deskriptif: menunjukkan pola, bukan bukti sebab akibat.

## 📁 Struktur Repository
| File | Keterangan |
|---|---|
| `olist-sales-performance.ipynb` | Notebook analisis lengkap (cleaning, merging, EDA) |
| `Olist _ Sales Performance.png` | Screenshot dashboard Tableau |
| `README.md` | Dokumentasi proyek |

---
👤 **Johannes Krysosthomus Thedens Dominggu**  
[LinkedIn](https://www.linkedin.com/in/johannes-krysosthomus-thedens-dominggu/) · [GitHub](https://github.com/TitoDominggu)
