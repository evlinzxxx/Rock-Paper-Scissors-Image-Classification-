## ✊✋✌️ Klasifikasi Gambar Rock, Paper, Scissors

#### 1. **Pengambilan dan Persiapan Dataset**
- Dataset  [Rock, Paper, Scissors](https://github.com/dicodingacademy/assets/releases/download/release/rockpaperscissors.zip)
- Dataset berisi **gambar tangan dalam posisi rock, paper, dan scissors**.
- Dataset dipisah menjadi:
  - **Training set:** 1312 gambar (60%)
  - **Validation set:** 876 gambar (40%)
- Pembagian dilakukan menggunakan `splitfolders`

#### 2. **Augmentasi Gambar**
- Augmentasi dilakukan menggunakan `ImageDataGenerator` dengan teknik:
  - Rotasi
  - Flip vertikal
  - Shearing
  - Rescale pixel

#### 3. **Arsitektur Model**
- Model dibangun dengan arsitektur **Sequential**:
  - 4 buah **Conv2D + MaxPooling2D**
  - **Dropout layer** untuk menghindari overfitting
  - **Dense layer** sebagai classifier
- Output layer menggunakan **softmax** untuk klasifikasi 3 kelas

#### 4. **Proses Pelatihan**
- Model dilatih menggunakan `Adam` optimizer dan `categorical_crossentropy`
- Callback digunakan untuk menghentikan training saat **akurasi training > 90%**
- Training selesai hanya dalam **3 epoch**, dengan hasil:
  - **Akurasi training:** 94.2%
  - **Akurasi validasi:** 92.9%

#### 5. **Pengujian Model**
- Model diuji dengan gambar yang diunggah langsung ke Colab
- Hasil prediksi ditampilkan sesuai dengan gambar yang diunggah (rock/paper/scissors)
- Model mampu mengenali gambar secara akurat

### Kesimpulan
Model CNN yang dibangun mampu mengklasifikasikan gambar Rock, Paper, dan Scissors dengan **akurasi tinggi dan waktu pelatihan yang cepat**. Proyek ini menunjukkan penerapan Computer Vision dasar dengan hasil yang memuaskan.

##### Proyek Final Belajar Machine Learning untuk Pemula
