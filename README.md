🔬 Klasifikasi Citra Hasil Endoskopi Gastrointestinal
📖 Deskripsi Proyek
Proyek ini bertujuan untuk mengembangkan model klasifikasi citra medis hasil endoskopi dengan memanfaatkan metode Transfer Learning berbasis Convolutional Neural Network (CNN).

Sistem gastrointestinal sering menjadi perhatian utama karena berbagai gangguan seperti polip dan kolitis ulseratif yang dapat berkembang menjadi kondisi serius jika tidak segera ditangani. Model ini dirancang untuk secara otomatis membedakan citra ke dalam tiga kategori utama:

Polip

Kolitis Ulseratif

Mukosa Normal

Dengan menerapkan pendekatan deep learning, proyek ini diharapkan dapat mendukung deteksi dini penyakit secara lebih cepat dan efisien dalam proses diagnosis medis.

🗂️ Dataset
Data citra yang digunakan dikumpulkan dari dua dataset publik berskala besar:

HyperKvasir: Digunakan untuk kelas Polip (1.028 gambar) dan Kolitis Ulseratif (851 gambar).

GastroVision: Digunakan untuk kelas Mukosa Normal (1.467 gambar).

Total keseluruhan dataset berjumlah 3.346 gambar, yang dipisah menjadi:

2.140 Data Latih

535 Data Validasi

671 Data Uji

🛠️ Teknologi & Alat yang Digunakan
Framework Utama: TensorFlow & Keras

Prapemrosesan & Augmentasi Data: Albumentations (Horizontal Flip, Rotate, Random Brightness Contrast, CLAHE, Gaussian Blur, Gauss Noise, Hue Saturation Value)

Analisis Data: Python, Pandas, NumPy

Lingkungan Eksekusi: Google Colab (GPU didukung)

💻 Highlight Implementasi Kode
Berikut adalah beberapa bagian penting dari implementasi kode dalam proyek ini yang menunjukkan penggunaan clean code dan optimasi model:

1. Augmentasi Data Tingkat Lanjut (Albumentations)
Untuk mencegah overfitting dan meningkatkan ketahanan model terhadap variasi gambar medis, diterapkan teknik augmentasi data yang ekstensif:

2. Arsitektur Model (Transfer Learning dengan ResNet101V2)
Model ini menggunakan arsitektur ResNet101V2 sebagai ekstraktor fitur (feature extractor), dipadukan dengan Custom Fully Connected Layer menggunakan Batch Normalization dan aktivasi Leaky ReLU.

3. Kompilasi & Evaluasi Model
Model dikompilasi menggunakan optimizer Adam dan dievaluasi dengan berbagai metrik untuk memastikan performa klasifikasi yang seimbang.

📊 Hasil Performa Terbaik
⚙️ Konfigurasi Model Terbaik
Arsitektur: ResNet101V2

Fungsi Aktivasi : Leaky ReLU

Optimizer : Adam (Learning Rate = 0.0001)

📈 Metrik Evaluasi (Data Uji)
💡 Insight: Secara spesifik, model ini sangat andal dalam membedakan anomali, sehingga meminimalisir kesalahan deteksi (False Negatives) pada prediksi pasien polip atau kolitis ulseratif yang mungkin dianggap normal.
