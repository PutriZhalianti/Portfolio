# 📊 Klasifikasi Kemiskinan Berdasarkan Data Sosial Ekonomi

## 📌 Deskripsi
Proyek ini bertujuan untuk mengklasifikasikan status kemiskinan rumah tangga menggunakan data sosial ekonomi. Dua model machine learning dibandingkan: **Linear Regression** dan **Decision Tree Classifier** untuk melihat mana yang lebih akurat dalam memahami pola data.


## 🛠️ Teknologi
- Python
- scikit-learn
- pandas, matplotlib
- Goofle Colab


## 🔍 Langkah Kerja
- Preprocessing: handling missing values, encoding
- Model building: Linear Regression dan Decision Tree
- Evaluasi model: akurasi, precision, recall, confusion matrix
- Perbandingan performa kedua model


## 📊 Hasil
- Decision Tree memiliki akurasi lebih tinggi (96%) dibanding Linear Regression (92%)
- Decision Tree lebih mampu menangani pola pada data sosial ekonomi
- Decision Tree tidak hanya menawarkan akurasi yang lebih tinggi dibandingkan Logistic Regression, tetapi juga mampu menangani ketidakseimbangan kelas dengan efektif. Dengan precision dan recall yang lebih tinggi pada kelas minoritas.
- Decision Tree membuktikan dirinya sebagai alat prediktif yang andal untuk diterapkan dalam kasus serupa.

📈 Visualisasi Hasil:  
![Visualisasi Balancing Data](./Gambar/Balance-Data_KKI.png)


## 🔗 Akses
- [Notebook](./klasifikasi-kemiskinan.ipynb)
- [Link Dataset (jika ada)](https://kaggle.com/...)

---

## 📌 Insight
Model Decision Tree sangat cocok untuk klasifikasi berbasis data demografis dan sosial. Proyek ini dapat dikembangkan lebih lanjut untuk rekomendasi kebijakan atau targeting bantuan sosial.
