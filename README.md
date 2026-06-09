# 🧠 Student Depression Classification

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-yellow?style=for-the-badge&logo=scikit-learn)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient_Boosting-green?style=for-the-badge)

## 📖 Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis tren kesehatan mental dan memprediksi indikasi depresi di kalangan pelajar/mahasiswa. Dengan memanfaatkan dataset profil pelajar, proyek ini menggunakan berbagai algoritma *Machine Learning* untuk mengidentifikasi faktor-faktor penentu yang berkontribusi terhadap depresi. Harapannya, hasil analisis ini dapat membantu merancang strategi intervensi dini yang lebih baik.

## 📊 Dataset
Dataset yang digunakan dalam proyek ini dapat diakses secara publik di Kaggle: 
[Student Depression Dataset](https://www.kaggle.com/datasets/hopesb/student-depression-dataset?resource=download)

**Fitur utama dalam dataset meliputi:**
- **Demografi:** Usia, Jenis Kelamin, Kota Asal, Pendidikan/Gelar (*Degree*).
- **Akademik & Pekerjaan:** Tekanan Akademik, Tekanan Kerja, Nilai (CGPA), Jam Kerja/Belajar, Kepuasan Belajar, Kepuasan Kerja.
- **Gaya Hidup & Kesehatan Mental:** Durasi Tidur, Kebiasaan Makan, Stres Finansial, Riwayat Penyakit Mental Keluarga, Pemikiran Bunuh Diri (*Suicidal Thoughts*).
- **Target Variabel:** `Depression` (0 = Tidak Depresi, 1 = Depresi).

## 🖼️ Kerangka Konsep
Berikut adalah gambaran kerangka konsep dari penelitian/proyek ini:

![Kerangka Konsep](Kerangka%20Konsep.png)

## 🛠️ Langkah-Langkah Proyek
1. **Data Preprocessing:**
   - Pembersihan data dan penanganan *Missing Values* (khususnya pada fitur `Financial Stress`).
   - Penghapusan kolom yang tidak relevan (`id`).
   - **Label Encoding** pada fitur biner dan ordinal (*Gender, Suicidal Thoughts, Family History*).
   - **One-Hot Encoding** pada fitur kategorikal nominal (*City, Profession, Sleep Duration, Dietary Habits, Degree*).
2. **Data Splitting & Scaling:**
   - Membagi data menjadi *Training Set* (80%) dan *Testing Set* (20%).
   - Standarisasi rentang data menggunakan `StandardScaler`.
3. **Pemodelan (*Model Training*):**
   - Melatih dan membandingkan 9 algoritma klasifikasi: *Logistic Regression, Decision Tree, Random Forest, SVM, Naive Bayes, KNN, Gradient Boosting, AdaBoost, dan XGBoost*.
4. **Evaluasi & Hyperparameter Tuning:**
   - Mengevaluasi setiap model menggunakan metrik *Accuracy, Precision, Recall*, dan *F1-Score*.
   - Melakukan *Hyperparameter Tuning* menggunakan `GridSearchCV` pada 3 model dengan performa terbaik.

## 🏆 Model Terbaik
Berdasarkan hasil evaluasi (F1-Score tertinggi), 3 model terbaik yang dipilih untuk proses tuning adalah:
1. 🥇 **AdaBoost**
2. 🥈 **Gradient Boosting**
3. 🥉 **Logistic Regression**

## 💻 Cara Menjalankan Proyek di Komputer Lokal
1. Pastikan Anda telah menginstal **Python** (versi 3.8 ke atas disarankan).
2. *Clone* atau *Download* repositori ini ke komputer Anda.
3. Buka terminal atau *command prompt*, lalu arahkan ke direktori proyek.
4. Buat dan aktifkan *Virtual Environment* (opsional namun disarankan):
   ```bash
   python -m venv venv
   # Di Windows:
   venv\Scripts\activate
   # Di Mac/Linux:
   source venv/bin/activate
   ```
5. Instal semua dependensi yang dibutuhkan:
   ```bash
   pip install -r requirements.txt
   ```
6. Buka Jupyter Notebook untuk mengeksplorasi kode, proses pemodelan, dan hasil analisis:
   ```bash
   jupyter notebook test.ipynb
   ```

## 📦 Requirements (Dependensi)
Library Python utama yang digunakan dalam pengembangan proyek ini antara lain:
- `pandas`
- `numpy`
- `scikit-learn`
- `xgboost`
- `matplotlib` & `seaborn`
- `plotly`
- `jupyter`

---
*Dibuat untuk keperluan analisis dan prediksi tingkat depresi pada pelajar, sebagai bentuk dukungan terhadap kesadaran pentingnya kesehatan mental.* 💙