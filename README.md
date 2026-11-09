## Project Overview
Proyek ini mengembangkan model Machine Learning untuk memprediksi kecenderungan nasabah berlangganan deposito dan mendukung strategi customer prioritization.

## Business Objective
Meningkatkan efektivitas pemilihan nasabah prioritas dalam kampanye pemasaran deposito dengan mempertimbangkan keterbatasan kapasitas pemasaran.

## Machine Learning Objective
Membangun model binary classification yang mampu menghasilkan skor probabilitas untuk menentukan urutan prioritas nasabah.

## Dataset
Dataset setelah data cleaning terdiri dari 7.805 observasi.
Pembagian data:
- Training: 6.244 observasi
- Testing: 1.561 observasi

Target prediksi:
- 0: Tidak berlangganan deposito
- 1: Berlangganan deposito

## Modeling
Algoritma yang dibandingkan:
- Logistic Regression
- Decision Tree
- Random Forest

Model akhir:
- Random Forest

Metode optimasi:
- RandomizedSearchCV
- Stratified 5-Fold Cross-Validation

## Final Model Performance

Hasil evaluasi Random Forest pada testing set:

| Metrik | Nilai |
|---|---:|
| Accuracy | 0.6957 |
| Precision | 0.7390 |
| Recall | 0.5617 |
| F1-score | 0.6382 |
| ROC-AUC | 0.7375 |

## Customer Ranking Evaluation
Pada kapasitas Top 20%:
- Jumlah nasabah prioritas: 313
- Nasabah positif: 266
- Precision@K: 0.8498
- Recall@K: 0.3566
- Lift@K: 1.7783

## Business Impact
Simulasi membandingkan ML-Based Targeting dengan Random Targeting menggunakan asumsi biaya kontak dan manfaat per nasabah positif.
Hasil simulasi bukan merupakan keuntungan aktual atau bukti peningkatan konversi secara kausal.

## Project Limitations
- Tidak tersedia identitas unik nasabah.
- Evaluasi hanya menggunakan dataset historis.
- Biaya dan manfaat bisnis menggunakan asumsi simulasi.
- Diperlukan validasi tambahan sebelum implementasi operasional.
