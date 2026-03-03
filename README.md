# Klasifikasi Citra Endoskopi Sistem Gastrointestinal Bawah Menggunakan Transfer Learning CNN

Repository ini berisi kode sumber dan dokumentasi untuk proyek Tugas Akhir mengenai klasifikasi citra medis hasil endoskopi. Proyek ini memfokuskan pada deteksi dini tiga kategori utama pada saluran pencernaan bagian bawah: **Polip**, **Kolitis Ulseratif**, dan **Mukosa Normal**.

## 📌 Ringkasan Proyek

Penelitian ini bertujuan untuk mengembangkan model klasifikasi yang cepat dan akurat untuk membantu tenaga medis dalam mendiagnosis penyakit gastrointestinal. Dengan memanfaatkan metode **Transfer Learning**, model dapat mengenali fitur-fitur kompleks pada citra medis meskipun dengan dataset yang terbatas.

## 🚀 Fitur Utama

* **Multi-class Classification**: Mengklasifikasikan citra ke dalam 3 kelas (Polip, Kolitis Ulseratif, Mukosa Normal).


* **Transfer Learning**: Menggunakan model pre-trained ternama seperti **VGG19**, **ResNet101V2**, dan **Inception V3**.


* **Advanced Data Augmentation**: Implementasi library `Albumentations` untuk teknik seperti *Horizontal Flip, Rotate, CLAHE, Gaussian Blur,* dan *Hue Saturation Value* untuk meningkatkan kekokohan model.


* **Fine-tuning**: Optimalisasi model dengan membekukan lapisan awal dan melatih ulang lapisan akhir untuk spesifikasi dataset medis.



## 📊 Dataset

Data yang digunakan dalam proyek ini bersumber dari dataset publik:

1. **HyperKvasir**: Digunakan untuk kelas Polip dan Kolitis Ulseratif.


2. **GastroVision**: Digunakan untuk kelas Mukosa Normal.



Total dataset terdiri dari **3.346 citra** dengan rasio pembagian 80% data latih dan 20% data uji.

## 🛠️ Teknologi yang Digunakan

* **Bahasa**: Python 


* **Framework**: TensorFlow & Keras 


* **Library**: Albumentations (Augmentasi), Pandas, NumPy, Matplotlib/Seaborn 


* **Lingkungan**: Google Colab 



## 📈 Hasil Eksperimen Terbaik

Berdasarkan pengujian beberapa skenario, model **ResNet101V2** memberikan performa paling optimal dengan konfigurasi:

* **Akurasi**: 98,66% 


* **Optimizer**: Adam (Learning Rate: 0.0001) 


* **Fungsi Aktivasi**: Leaky ReLU 


* **Fully Connected Layer**: Diawali dengan 512 unit 



## 📁 Struktur Folder

```text
├── notebooks/           # File .ipynb (Google Colab)
└── README.md

```

## ✍️ Penulis

**Rivaldo Panangian Tambunan**

* NRP: 5025201134 


* Departemen Teknik Informatika, Institut Teknologi Sepuluh Nopember (ITS) 
