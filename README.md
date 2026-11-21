# Evaluasi Model Klasifikasi: Deteksi Fraud Pembayaran Digital

Repositori ini berisi kode dan laporan praktikum **Data Mining** yang berfokus pada evaluasi performa model klasifikasi menggunakan algoritma **Decision Tree** pada dataset tidak seimbang (*imbalanced dataset*). Studi kasus yang diangkat adalah simulasi deteksi penipuan (*fraud*) pada transaksi pembayaran digital.

## 📌 Tujuan & Cakupan Praktikum
* **Pembangkitan Dataset Sintetis:** Simulasi 500 data transaksi digital (`amount`, `hour`, `new_device`, `foreign_ip`, dan label target `isFraud`) dengan distribusi kelas tidak seimbang (484 Normal, 16 Fraud).
* **Pemodelan Klasifikasi:** Pelatihan model `DecisionTreeClassifier` (`max_depth=4`, `class_weight='balanced'`) dengan rasio pembagian data latih dan uji sebesar 70:30.
* **Evaluasi & Verifikasi Metrik:** Perhitungan komponen **Confusion Matrix** (TP, TN, FP, FN) serta metrik **Accuracy, Precision, Recall, dan F1-Score** secara manual maupun menggunakan `scikit-learn`.
* **Analisis Data Tidak Seimbang (*Imbalanced Data*):** Perbandingan performa model Decision Tree dengan *baseline model* (prediksi semua normal) untuk melihat keterbatasan metrik *Accuracy*.
* **Eksperimen *Threshold Tuning*:** Analisis pengaruh perubahan ambang batas probabilitas (`0.2`, `0.4`, `0.5`, dan `0.7`) terhadap nilai *Precision* dan *Recall* berdasarkan risiko kesalahan prediksi (FP vs FN).

## 🛠️ Teknologi & Library
* **Bahasa Pemrograman:** Python 3
* **Library:** NumPy, Pandas, Scikit-learn, Matplotlib

## 📊 Ringkasan Hasil Evaluasi
| Model / Skenario | Accuracy | Precision (Fraud) | Recall (Fraud) | F1-Score (Fraud) |
| :--- | :---: | :---: | :---: | :---: |
| **Baseline (Semua Normal)** | 0.967 | 0.000 | 0.000 | 0.000 |
| **Decision Tree (Default)** | 0.767 | 0.059 | 0.400 | 0.103 |

## 👤 Identitas Penulis
* **Nama:** Ridho Dwi Putra Zendy
* **NIM:** 24343106
* **Program Studi:** Informatika — Universitas Negeri Padang
