# 📊 Klasifikasi Kemiskinan Berdasarkan Data Sosial Ekonomi

## 📌 Deskripsi
Proyek ini bertujuan untuk mengklasifikasikan status kemiskinan rumah tangga menggunakan data sosial ekonomi. Dua model machine learning dibandingkan: **Linear Regression** dan **Decision Tree Classifier** untuk melihat mana yang lebih akurat dalam memahami pola data.


## 🛠️ Teknologi
- Python
- scikit-learn
- Smote
- pandas, matplotlib, seaborn
- Google Colab


## 🔍 Langkah Kerja
- Pengambilan Dataset<br>
  Saya mengambil dataset dari platform kaggle milik Ermila
- Data Understanding<br>
  Kumpulan data ini berisi 13 atribut. Atribut “Klasifikasi Kemiskinan” mengacu pada keadaan miskin atau tidak miskin. Bernilai bilangan bulat 0 = tidak miskin dan 1 = miskin.
- EDA dan Preprocessing<br>
  - Missing values: melakukan pemeriksaan apakah ada nilai yang hilang dalam dataset. Berdasarkan hasil pemeriksaan tidak ditemukan nilai yang hilang dalam dataset, sehingga dapat dipastikan data lengkap dan siap digunakan.
  -  Data duplikat: melihat apakah ada baris data yang terduplikasi. Setelah dilakukan pemeriksaan, tidak ditemukan adanya data duplikat dalam dataset ini, sehingga proses ini tidak memerlukan tindakan tambahan.
  - Encoding: Beberapa kolom dalam dataset memiliki tipe data bertipe objek.  Tipe data ini tidak cocok untuk analisis numerik, sehingga diubah menjadi float dan integer agar dapat digunakan dalam perhitungan atau pemodelan.
- Balancing Data<br>
  Dataset tingkat kemiskinan ini memiliki label dengan distribusi kelas yang tidak seimbang, di mana terdapat kelas mayoritas dan kelas minoritas. Ketidakseimbangan ini dapat menyebabkan hasil klasifikasi menjadi kurang optimal. Untuk mengatasi masalah tersebut, penelitian ini menerapkan metode Synthetic Minority Over-Sampling Technique (SMOTE).<br>
  Berikut adalah visualisasi dari proses hasil SMOTE
  ![Visualisasi Balancing Data](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/Balance-Data_KKI.png?raw=true)
- Model building<br>
  Linear Regression dan Decision Tree
- Evaluasi model<br>
  akurasi, precision, recall, confusion matrix
- Perbandingan performa kedua model


## 📊 Hasil
- Decision Tree memiliki akurasi lebih tinggi (92%) dibanding Linear Regression (90%)
- Decision Tree lebih mampu menangani pola pada data sosial ekonomi
- Decision Tree tidak hanya menawarkan akurasi yang lebih tinggi dibandingkan Logistic Regression, tetapi juga mampu menangani ketidakseimbangan kelas dengan efektif. Dengan precision dan recall yang lebih tinggi pada kelas minoritas.
- Decision Tree membuktikan dirinya sebagai alat prediktif yang andal untuk diterapkan dalam kasus serupa.

📈 Visualisasi Hasil: 
- Hasil Evaluasi dari kedua Model
  - Confusion Matrix<br>
![Confusion Matrix](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/Confusion-Matrix-KKI.png?raw=true)
  - Matrix Evaluasi Decision Tree<br>
    ![Matrix Evaluasi Decision Tree](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/DecissionTree.png?raw=true)
  - Matrix Evaluasi Logistic Regression<br>
    ![Matrix Evaluasi Logistic Regression](https://github.com/PutriZhalianti/Portfolio/blob/main/Gambar/LogisticRegression.png?raw=true)


## 🔗 Akses
- [Notebook](./KlasifikasiKemiskinan_Putri.ipynb)
- [Link Dataset](https://www.kaggle.com/datasets/ermila/klasifikasi-tingkat-kemiskinan-di-indonesia)


## 📌 Insight
Model Decision Tree sangat cocok untuk klasifikasi berbasis data demografis dan sosial. Decision Tree membuktikan dirinya sebagai alat prediktif yang andal untuk diterapkan dalam kasus serupa. Proyek ini dapat dikembangkan lebih lanjut untuk rekomendasi kebijakan atau targeting bantuan sosial.
