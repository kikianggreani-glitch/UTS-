# UTS Data Mining

# Nama :Kiki Anggreani
NIM : 2304020001
Rombel : Rombel 1 Pendidikan Matematika 2023

Proyek ini bertujuan untuk melakukan prediksi **Wine Quality Classification** menggunakan beberapa metode machine learning klasifikasi. Pada penelitian ini dilakukan perbandingan performa tiga algoritma klasifikasi, yaitu **K-Nearest Neighbors (KNN)**, **Support Vector Machine (SVM)**, dan **Random Forest** untuk menentukan metode dengan tingkat akurasi terbaik dalam memprediksi variabel `quality` pada data testing.

Tahapan yang dilakukan meliputi eksplorasi data, preprocessing, pelatihan model, evaluasi menggunakan cross validation, hyperparameter tuning, hingga prediksi data testing. Berdasarkan hasil evaluasi, metode **Random Forest** memberikan performa dan akurasi terbaik sehingga dipilih sebagai model final untuk prediksi kualitas wine.
---
# Langkah Pengerjaan — Metode KNN
### 1. Import Library
Tahap awal dilakukan import library yang dibutuhkan seperti:
* `pandas`
* `numpy`
* `matplotlib`
* `KNeighborsClassifier`
* `StandardScaler`
* library evaluasi dari `sklearn`
### 2. Load Dataset
Dataset training dan testing dimuat menggunakan `pandas.read_csv()`.
### 3. Eksplorasi Data (EDA)
Dilakukan eksplorasi data berupa:
* menampilkan data awal,
* statistik deskriptif,
* pengecekan missing value,
* dan distribusi label `quality`.
### 4. Persiapan Fitur dan Target
Menentukan variabel fitur dan target (`quality`).
### 5. Normalisasi Data
Dilakukan normalisasi menggunakan `StandardScaler` karena KNN sensitif terhadap skala data.
### 6. Mencari Nilai K Optimal
Dilakukan pengujian beberapa nilai K menggunakan `cross validation` untuk mendapatkan jumlah tetangga terbaik.
### 7. Training Model KNN
Model KNN dilatih menggunakan parameter terbaik hasil pengujian.
### 8. Evaluasi Model
Evaluasi dilakukan menggunakan:
* Accuracy Score
* Confusion Matrix
* Classification Report
* Cross Validation
### 9. Hyperparameter Tuning
Menggunakan `GridSearchCV` untuk memperoleh kombinasi parameter terbaik.
### 10. Prediksi Data Testing
Model digunakan untuk memprediksi kualitas wine pada data testing.
### 11. Hasil Akurasi
Hasil evaluasi menunjukkan bahwa metode **KNN** memperoleh:
* **CV Accuracy : 63.59%**

---

# Langkah Pengerjaan — Metode SVM
### 1. Import Library
Mengimpor library yang diperlukan seperti:
* `SVC`
* `StandardScaler`
* `GridSearchCV`
* library evaluasi dan visualisasi
### 2. Load Dataset
Dataset training dan testing dimuat menggunakan `pandas.read_csv()`.
### 3. Eksplorasi Data
Melakukan pengecekan struktur data, statistik deskriptif, dan missing value.
### 4. Persiapan Fitur dan Target
Menentukan fitur input dan target `quality`.
### 5. Normalisasi Data
Data dinormalisasi menggunakan `StandardScaler` karena SVM sensitif terhadap skala data.
### 6. Training Model SVM
Model SVM dilatih menggunakan kernel `rbf`.
### 7. Evaluasi Model
Evaluasi dilakukan menggunakan:
* Accuracy Score
* Confusion Matrix
* Classification Report
* Cross Validation
### 8. Hyperparameter Tuning
Menggunakan `GridSearchCV` untuk mencari parameter terbaik.
### 9. Prediksi Data Testing
Model terbaik digunakan untuk memprediksi kualitas wine pada data testing.
### 10. Hasil Akurasi
Hasil evaluasi menunjukkan bahwa metode **SVM** memperoleh:
* **CV Accuracy : 60.56%**

---

# Langkah Pengerjaan — Metode Random Forest
### 1. Import Library
Mengimpor library seperti:
* `RandomForestClassifier`
* `pandas`
* `numpy`
* library evaluasi dan visualisasi
### 2. Load Dataset
Dataset training dan testing dimuat menggunakan `pandas.read_csv()`.
### 3. Eksplorasi Data
Melakukan eksplorasi data berupa:
* statistik deskriptif,
* distribusi data,
* dan pengecekan missing value.
### 4. Persiapan Fitur dan Target
Menentukan fitur input dan target `quality`.
### 5. Training Model Random Forest
Model Random Forest dilatih menggunakan parameter terbaik.
### 6. Evaluasi Model
Evaluasi model dilakukan menggunakan:
* Accuracy Score
* Confusion Matrix
* Classification Report
* Cross Validation
### 7. Feature Importance
Melihat tingkat kepentingan masing-masing fitur terhadap prediksi kualitas wine.
### 8. Hyperparameter Tuning
Menggunakan `GridSearchCV` untuk mendapatkan parameter terbaik.
### 9. Prediksi Data Testing
Model terbaik digunakan untuk memprediksi variabel `quality` pada data testing.
### 10. Hasil Akurasi
Hasil evaluasi menunjukkan bahwa metode **Random Forest** memperoleh:
* **CV Accuracy : 65.10%**

---

# Perbandingan Akurasi Model
| Metode        | Akurasi Cross Validation |
| ------------- | ------------------------ |
| KNN           | 63.59%                   |
| SVM           | 60.56%                   |
| Random Forest | 65.10%                   |
---
# Kesimpulan
Berdasarkan hasil perbandingan tiga metode klasifikasi yang digunakan, yaitu **KNN**, **SVM**, dan **Random Forest**, diperoleh bahwa metode **Random Forest** memberikan performa terbaik dengan tingkat akurasi tertinggi sebesar **65.10%** dalam memprediksi kualitas wine pada data testing.

Oleh karena itu, metode Random Forest dipilih sebagai model final dalam proses klasifikasi **Wine Quality Prediction**.
