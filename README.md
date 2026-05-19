# H1D024098_Talitha Maharani Nashier_ShiftC

# Praktikum Kecerdasan Buatan - Pertemuan 7
**Implementasi Jaringan Saraf Tiruan (JST) untuk Klasifikasi Dataset Iris**

Repositori ini dibuat untuk memenuhi tugas praktikum mata kuliah Kecerdasan Buatan pada Pertemuan 7. Fokus utama pada modul ini adalah memahami penerapan arsitektur *Artificial Neural Network* (ANN) / Jaringan Saraf Tiruan menggunakan pustaka TensorFlow dan Keras di Python untuk mengklasifikasikan spesies bunga Iris.

## Identitas Mahasiswa
* **Nama:** [Isi Nama Kamu di Sini]
* **NIM:** H1D024098
* **Kelas Praktikum:** Kecerdasan Buatan

---

## Deskripsi Tugas & Dataset
Tugas ini menerapkan model JST Multi-Layer Perceptron (MLP) untuk memprediksi 3 kelas spesies bunga Iris (*Iris-setosa*, *Iris-versicolor*, dan *Iris-virginica*) berdasarkan 4 fitur utama:
1. Sepal Length (Panjang Kelopak)
2. Sepal Width (Lebar Kelopak)
3. Petal Length (Panjang Mahkota)
4. Petal Width (Lebar Mahkota)

Dataset diambil secara otomatis melalui URL publik resmi dari *UCI Machine Learning Repository*.

---

## Arsitektur Model JST
Model dibangun secara `Sequential` memanfaatkan API tingkat tinggi dari Keras dengan konfigurasi lapisan (layer) sebagai berikut:

* **Input Layer:** Menampung 4 bentuk fitur masukan.
* **Hidden Layer 1:** `Dense` layer dengan **1000 neuron**, fungsi aktivasi `ReLU`.
* **Hidden Layer 2:** `Dense` layer dengan **500 neuron**, fungsi aktivasi `ReLU`.
* **Hidden Layer 3:** `Dense` layer dengan **300 neuron**, fungsi aktivasi `ReLU`.
* **Output Layer:** `Dense` layer dengan **3 neuron** (merepresentasikan 3 kelas spesies) menggunakan fungsi aktivasi `Softmax` untuk menghasilkan probabilitas prediksi.

### Parameter Kompilasi
* **Optimizer:** `Adam Optimizer` (pembelajaran adaptif yang efisien).
* **Loss Function:** `Sparse Categorical Crossentropy` (cocok untuk label bernilai integer/numerik banyak kelas).
* **Metrics:** `Accuracy`.
* **Jumlah Epochs:** 50.
* **Rasio Data Latih & Uji:** 80% Training Data : 20% Validation/Test Data.

---

## Hasil Evaluasi Model
Berdasarkan proses pelatihan (*training*) sebanyak 50 epoch yang dilakukan pada Google Colab, diperoleh performa akhir model sebagai berikut:

* **Loss Akhir:** 0.1981
* **Akurasi Akhir (*Validation Accuracy*):** **90.00% (0.9000)**

Model berhasil memprediksi sebagian besar sampel pada data uji dengan sangat baik, dibuktikan melalui visualisasi *Confusion Matrix* yang menunjukkan tingkat kesalahan klasifikasi yang sangat minim antar-spesies bunga Iris.

---

## Pustaka (Libraries) yang Digunakan
* `tensorflow` & `keras` (untuk membangun dan melatih model neural network)
* `pandas` & `numpy` (untuk manipulasi data tabel dan array)
* `scikit-learn` (untuk LabelEncoder dan Train-Test Split data)
* `matplotlib` & `seaborn` (untuk visualisasi grafik performa dan confusion matrix)

---
*Praktikum Kecerdasan Buatan 2026*
