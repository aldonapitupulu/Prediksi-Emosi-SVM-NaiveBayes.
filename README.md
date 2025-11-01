# Predikis Emosi Berbasis Teks Menggunakan Algoritma SVM dan Naive Bayes

## 📝 Deskripsi Proyek

Proyek ini bertujuan untuk membangun dan membandingkan kinerja dua model *Machine Learning* klasik, yaitu **Linear Support Vector Classifier (LinearSVC)** dan **Multinomial Naive Bayes (MNB)**, dalam tugas klasifikasi emosi berbasis teks.

Teks diubah menjadi fitur numerik menggunakan metode **Term Frequency-Inverse Document Frequency (TF-IDF)** sebelum diumpankan ke masing-masing model.

## ⚙️ Metode yang Digunakan

| Tahap | Deskripsi |
| :--- | :--- |
| **Data Source** | Menggunakan dataset **`text.csv`**, yang bersumber dari **Kaggle: Emotions Dataset** ([https://www.kaggle.com/datasets/nelgiriyewithana/emotions](https://www.kaggle.com/datasets/nelgiriyewithana/emotions)). Dataset ini berisi lebih dari 416 ribu teks dan label emosi. |
| **Kelas Emosi** | Terdapat enam (5) kelas emosi yang menjadi target klasifikasi: `Sadness`, `Joy`, `Love`, `Anger`, `Fear`, dan `Surprise`. |
| **Preprocessing & Vectorization** | Data dibagi menjadi set pelatihan (80%) dan pengujian (20%). Teks diubah menggunakan **TfidfVectorizer** dengan batasan **5000 fitur** teratas (`max_features=5000`). |
| **Model 1** | **Linear Support Vector Classifier (LinearSVC)** dengan parameter regularisasi `C=0.1`. |
| **Model 2** | **Multinomial Naive Bayes (MNB)**, yang cocok untuk data fitur yang terhitung seperti TF-IDF. |

## 📊 Hasil dan Perbandingan

Kedua model dilatih dan dievaluasi menggunakan set data pengujian (20%).

| Model Klasifikasi | Akurasi (Accuracy) |
| :--- | :--- |
| **Multinomial Naive Bayes** | **0.87 (87%)** |
| **LinearSVC (SVM)** | **0.90 (90%)** |

**Kesimpulan Hasil:**
Model **LinearSVC (SVM)** memberikan kinerja yang sedikit lebih unggul (3% lebih tinggi) dibandingkan dengan Multinomial Naive Bayes dalam memprediksi emosi pada dataset yang digunakan.
