# Deteksi Emosi Wajah Menggunakan Transfer Learning (VGG16)

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk mengklasifikasikan ekspresi wajah manusia ke dalam kategori emosi menggunakan pendekatan **transfer learning dengan arsitektur VGG16**. Model dilatih berdasarkan dataset **CK+48** dan beberapa dataset tambahan dari **FER2013**, yang berisi gambar wajah dengan berbagai ekspresi seperti marah, sedih, takut, bahagia, dan netral.
Dengan menggunakan teknik ekstraksi fitur dari model VGG16 dan pelatihan ulang pada layer klasifikasi akhir, model ini dapat mendeteksi emosi wajah secara otomatis dan akurat.


## 🛠️ Teknologi yang Digunakan
- Python
- TensorFlow & Keras
- cv2
- Transfer Learning (VGG16)
- LabelEncoder
- scikit-learn
- streamlit
- Matplotlib & Seaborn


## 🔍 Langkah Kerja

1. **Import Library**  
   Mengimpor semua library yang dibutuhkan untuk preprocessing gambar, membangun model, pelatihan, dan evaluasi.

2. **Persiapan Dataset**
   - Dataset: CK+ (Cohn-Kanade Extended) versi 48x48 piksel grayscale
   - Karena dataset CK+ kurang bervariasi, saya menambahkan beberapa gambar dari dataset **FER2013**
   - Mengelompokkan gambar berdasarkan label emosi
   - Melakukan pengecekan distribusi kelas dan visualisasi sampel

3. **Data Preprocessing**
   - Resize gambar menjadi 224x224 agar sesuai dengan input VGG16
   - Normalisasi nilai piksel
   - Label encoding dan pembagian data menjadi training dan testing set (80:20)

4. **Model Transfer Learning**
   - Menggunakan **VGG16** (tanpa top layer) sebagai feature extractor
   - Menambahkan beberapa Dense layers di atas output VGG16
   - Kompilasi model dengan optimizer Adam dan loss categorical crossentropy

5. **Training Model**
   - Training dilakukan selama 20 epoch dan early stopping
   - Visualisasi training loss dan accuracy per epoch

6. **Evaluasi Model**
   - Menggunakan confusion matrix dan classification report
   - Menampilkan hasil prediksi terhadap beberapa gambar uji


## 📊 Hasil Model
- Akurasi model pada data uji: **91%**
- Model mampu mengenali ekspresi wajah dengan sangat baik
- Performa tertinggi pada kelas emosi "anger" dan "contempt"

📈 Confusion Matrix:  
![Confusion Matrix](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/Confusion-Matrix-Emosi.png)

📈 Plot Akurasi dan Loss:  
![Plot Akurasi dan Loss](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/PlotAkurasidanLoss-Emosi.png)

🖼️ Contoh Hasil Prediksi:  
![Prediksi](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/HasilPrediksiEmosi.png)

---

## 🚀 Demo Aplikasi
Model ini dapat dideploy menggunakan Streamlit sebagai antarmuka sederhana bagi pengguna untuk mengunggah gambar dan mendapatkan prediksi ekspresi wajah secara langsung.

🔗 [Streamlit Demo (opsional link)](https://putriyahnda-emosi.streamlit.app)

---

## 📂 Notebook
- [Notebook](./face-emotion-detection.ipynb)


## 👩‍💻 Tentang Saya
Putri Yahnda Alha Zhalianti  
Mahasiswa Informatika | AI & Machine Learning Enthusiast  
📫 palhazhalianti@gmail.com | 🌐 [LinkedIn](https://linkedin.com/in/putriyahnda)

