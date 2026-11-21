# Evaluasi Model Klasifikasi: Deteksi Fraud Pembayaran Digital

Repositori ini berisi kode dan laporan praktikum **Data Mining** yang berfokus pada evaluasi performa model klasifikasi menggunakan algoritma **Decision Tree** pada dataset tidak seimbang (*imbalanced dataset*)[cite: 1]. Studi kasus yang diangkat adalah simulasi deteksi penipuan (*fraud*) pada transaksi pembayaran digital[cite: 1].

## 📌 Tujuan & Cakupan Praktikum
* **Pembangkitan Dataset Sintetis:** Simulasi 500 data transaksi digital (`amount`, `hour`, `new_device`, `foreign_ip`, dan label target `isFraud`) dengan distribusi kelas tidak seimbang (484 Normal, 16 Fraud)[cite: 1].
* **Pemodelan Klasifikasi:** Pelatihan model `DecisionTreeClassifier` (`max_depth=4`, `class_weight='balanced'`) dengan rasio pembagian data latih dan uji sebesar 70:30[cite: 1].
* **Evaluasi & Verifikasi Metrik:** Perhitungan komponen **Confusion Matrix** (TP, TN, FP, FN) serta metrik **Accuracy, Precision, Recall, dan F1-Score** secara manual maupun menggunakan `scikit-learn`[cite: 1].
* **Analisis Data Tidak Seimbang (*Imbalanced Data*):** Perbandingan performa model Decision Tree dengan *baseline model* (prediksi semua normal) untuk melihat keterbatasan metrik *Accuracy*[cite: 1].
* **Eksperimen *Threshold Tuning*:** Analisis pengaruh perubahan ambang batas probabilitas (`0.2`, `0.4`, `0.5`, dan `0.7`) terhadap nilai *Precision* dan *Recall* berdasarkan risiko kesalahan prediksi (FP vs FN)[cite: 1].

## 🛠️ Teknologi & Library
* **Bahasa Pemrograman:** Python 3[cite: 1]
* **Library:** NumPy, Pandas, Scikit-learn, Matplotlib[cite: 1]

## 📊 Ringkasan Hasil Evaluasi
| Model / Skenario | Accuracy | Precision (Fraud) | Recall (Fraud) | F1-Score (Fraud) |
| :--- | :---: | :---: | :---: | :---: |
| **Baseline (Semua Normal)** | 0.967 | 0.000 | 0.000 | 0.000 |
| **Decision Tree (Default)** | 0.767 | 0.059 | 0.400 | 0.103 |

## 👤 Identitas Penulis
* **Nama:** Ridho Dwi Putra Zendy
* **NIM:** 24343106
* **Program Studi:** Informatika — Universitas Negeri Padang
