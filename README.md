# Financial Fraud Detection: Hybrid Machine Learning Approach

## 📌 1. Problem Statement
Di industri finansial, mendeteksi transaksi palsu (*fraud*) atau aktivitas mencurigakan secara cepat adalah tantangan besar. Masalah utamanya adalah **ketiadaan label awal** pada data untuk menentukan mana transaksi yang aman dan mana yang merupakan kecurangan. Selain itu, pola fraud sering kali tersembunyi di balik tingginya frekuensi percobaan login (`LoginAttempts`) atau lonjakan nilai transaksi (`TransactionAmount`) yang tidak wajar.

## 🎯 2. Project Goal
Proyek ini bertujuan untuk membangun sistem deteksi anomali finansial *end-to-end* menggunakan pendekatan **Hybrid Machine Learning**:
1. **Mengidentifikasi pola anomali** secara mandiri menggunakan teknik *Unsupervised Learning (Clustering)* untuk menghasilkan label *fraud* / *not fraud*.
2. **Membangun model prediktif** berbasis *Supervised Learning (Classification)* menggunakan label hasil klasterisasi untuk menyaring transaksi mencurigakan di masa depan secara otomatis.

## 🛠️ 3. Tech Stack & Tools
* **Language:** Python
* **Data Manipulation & Analisis:** Pandas, NumPy
* **Machine Learning Pipelining:** Scikit-Learn
* **Imbalanced Data Handling:** Imbalanced-learn (SMOTE)
* **Visualisasi Data:** Matplotlib, Seaborn

## 💡 4. Key Insights & Expected Outcomes
* **Deteksi Pola Tersembunyi:** Melalui *Clustering*, kita bisa memetakan profil transaksi ekstrem (misal: kombinasi `LoginAttempts` tinggi, durasi transaksi singkat, dan perubahan `IP Address` yang cepat) sebagai indikator kuat anomali.
* **Solusi Data Tidak Seimbang:** Kasus fraud secara alami berjumlah sangat sedikit dibanding transaksi normal. Penggunaan **SMOTE** di tahap klasifikasi memastikan model tidak bias dan tetap sensitif dalam mendeteksi fraud.
* **Metrik Keamanan Finansial:** Evaluasi model berfokus pada **Recall** tinggi untuk meminimalkan lolosnya transaksi fraud (*False Negative*), demi menjaga keamanan dana nasabah.
