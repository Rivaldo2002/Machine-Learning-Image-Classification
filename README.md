Klasifikasi Citra Hasil Endoskopi Gastrointestinal dengan Transfer Learning
Deskripsi Proyek
Proyek ini bertujuan untuk mengembangkan model klasifikasi citra medis hasil endoskopi dengan memanfaatkan metode Transfer Learning berbasis Convolutional Neural Network (CNN). Sistem gastrointestinal sering menjadi perhatian utama karena berbagai gangguan seperti polip dan kolitis ulseratif yang dapat berkembang menjadi kondisi serius jika tidak segera ditangani.

Model ini dirancang untuk secara otomatis membedakan citra ke dalam tiga kategori utama: Polip, Kolitis Ulseratif, dan Mukosa Normal. Dengan menerapkan pendekatan deep learning, proyek ini diharapkan dapat mendukung deteksi dini penyakit secara lebih cepat dan efisien dalam proses diagnosis medis.

Dataset
Data citra yang digunakan dikumpulkan dari dua dataset publik berskala besar:


HyperKvasir: Digunakan untuk kelas Polip (1.028 gambar) dan Kolitis Ulseratif (851 gambar).


GastroVision: Digunakan untuk kelas Mukosa Normal (1.467 gambar).

Total keseluruhan dataset berjumlah 3.346 gambar, yang kemudian dipisah menjadi 2.140 data latih, 535 data validasi, dan 671 data uji.

Teknologi & Alat yang Digunakan

Framework Utama: TensorFlow & Keras.


Prapemrosesan & Augmentasi Data: Albumentations (termasuk Horizontal Flip, Rotate, Random Brightness Contrast, CLAHE, Gaussian Blur, Gauss Noise, dan Hue Saturation Value).


Analisis Data: Python, Pandas, NumPy.


Lingkungan Eksekusi: Google Colab (GPU didukung).

Metodologi
Proyek ini mengimplementasikan metode Transfer Learning dengan teknik fine-tuning untuk mengekstraksi fitur visual secara optimal. Tiga arsitektur model pre-trained dievaluasi dalam pengujian ini:


VGG19 


Inception V3 


ResNet101V2 

Setiap model dikalibrasi menggunakan modifikasi pada Fully Connected Layer, fungsi aktivasi (ReLU, Leaky ReLU, Swish), serta optimizer (Adam & SGD).

Hasil Performa Terbaik
Berdasarkan uji coba dan evaluasi secara keseluruhan, ResNet101V2 terbukti menjadi model pre-trained yang memberikan hasil paling optimal.

Konfigurasi Model Terbaik:


Arsitektur: ResNet101V2 


Dense Awal: 512 Unit 


Fungsi Aktivasi: Leaky ReLU 


Optimizer: Adam (Learning Rate = 0.0001) 

Metrik Evaluasi (Data Uji):


Akurasi: 98.66% 


Precision: 98.66% 


Recall: 98.65% 


F1-Score: 98.65% 


Loss: 0.0573 

Secara spesifik, model sangat andal dalam membedakan anomali, sehingga meminimalisir kesalahan deteksi (False Negatives) pada prediksi pasien polip atau kolitis ulseratif yang dianggap normal.
