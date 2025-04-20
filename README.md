# 🍎🍊🍌 Klasifikasi Buah dengan CNN dan TensorFlow 🍎🍊🍌

Proyek ini menggunakan Convolutional Neural Network (CNN) berbasis TensorFlow untuk mengklasifikasikan gambar buah menjadi tiga kelas: **Apel**, **Jeruk**, dan **Pisang**. Model yang dilatih kemudian diekspor ke tiga format: **SavedModel**, **TensorFlow Lite (TFLite)**, dan **TensorFlow.js (TFJS)** agar bisa digunakan di berbagai platform.

## 📁 Struktur Direktori
submission
├───tfjs_model
| ├───group1-shard1of1.bin
| └───model.json
├───tflite
| ├───model.tflite
| └───label.txt
├───saved_model
| ├───saved_model.pb
| └───variables
├───notebook.ipynb
├───README.md
└───requirements.txt
## 🧠 Model

Model CNN dibangun menggunakan Keras Sequential API dengan beberapa Conv2D dan MaxPooling2D, kemudian dilatih selama 5 epoch menggunakan dataset gambar buah. Callback **EarlyStopping** juga digunakan untuk menghentikan pelatihan jika validasi tidak meningkat.

## 🔄 Format Model yang Didukung

- **SavedModel**: Format standar TensorFlow untuk digunakan di backend Python.
- **TFLite**: Format ringan untuk aplikasi mobile/embedded.
- **TFJS**: Format yang dapat dijalankan langsung di browser menggunakan JavaScript.

## 🧪 Inferensi

Gambar bisa di-*upload*, lalu diprediksi menggunakan model pada colab:
from google.colab import files
uploaded = files.upload()

## 📌 Requirements
Beberapa library yang digunakan:
TensorFlow
NumPy
Matplotlib
Pillow
Semua kebutuhan pustaka ada di file requirements.txt.
