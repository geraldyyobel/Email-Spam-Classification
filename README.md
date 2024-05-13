# Submission 1: Email Spam Classification
Nama : Geraldy Yobel Primandaru
username : geraldyyobel
## Overview
Proyek ini adalah tentang pembuatan model klasifikasi email untuk membedakan antara email yang merupakan spam dan yang bukan spam. Model ini dibangun menggunakan TensorFlow Extended (TFX) dan menggunakan dataset yang terdiri dari 83.446 rekaman email yang diberi label.

## Dataset
Dataset yang digunakan dalam proyek ini merupakan gabungan dari 2007 TREC Public Spam Corpus dan Enron-Spam Dataset. Setiap rekaman email memiliki dua atribut:
- `label`: Menunjukkan apakah email tersebut spam (1) atau bukan spam (0).
- `text`: Berisi isi sebenarnya dari email.
Dataset: https://www.kaggle.com/datasets/purusinghvi/email-spam-classification-dataset?resource=download

## Masalah: 
Masalah utama adalah memastikan bahwa model klasifikasi email dapat membedakan dengan tepat antara email yang merupakan spam dan yang bukan spam. Hubungan antara deskripsi masalah dan dataset ini adalah bahwa dataset menyediakan informasi yang diperlukan untuk melatih model klasifikasi yang dapat membedakan antara email yang sah dan email spam. Dengan menggunakan dataset ini, kita dapat membangun model yang memanfaatkan pola-pola dalam teks email untuk mengidentifikasi ciri-ciri yang membedakan antara email spam dan non-spam. Melalui proses ini, kita dapat mengatasi masalah spam dan meningkatkan pengalaman pengguna dalam mengelola kotak masuk email mereka.

## Solusi Machine Learning
 Membangun sebuah machine learning pipeline menggunakan TensorFlow Extended (TFX) untuk melakukan klasifikasi email spam berdasarkan dataset yang diberikan. Dengan melakukan klasifikasi, user dapat menyaring email secara otomatis yang terdeteksi sebagai spam, sehingga dapat meningkatkan produktivitas ketika bekerja. Secara keseluruhan, solusi model Spam-Detection ini memberikan manfaat bagi pengguna dalam hal efisiensi dan keamanan.

## Metode Pengolahan
 Metode normalisasi menjadi huruf kecil menggunakan fungsi tf.strings.lower() dari TensorFlow. Ini dilakukan untuk memastikan konsistensi dalam representasi teks, sehingga kata-kata yang sama dengan huruf besar atau huruf kecil dapat dianggap setara. Kemudian tanda baca dihilangkan dari teks email menggunakan pendekatan sederhana dengan tidak menyertakan tanda baca saat normalisasi.

## Arsitektur Model:

    Normalisasi Teks
    Layer Embedding
    Layer Conv1D
    Dense Layer
    Output Layer

## Metrik Evaluasi:

    ExampleCount: Metrik ini menyajikan jumlah total contoh yang dievaluasi selama proses evaluasi model.
    AUC (Area Under the Curve): Metrik ini mengukur performa model dalam memisahkan kelas positif dan negatif. Nilai AUC berada dalam kisaran 0 hingga 1, di mana nilai yang lebih tinggi menunjukkan performa yang lebih baik.
    False Positives: Ini adalah jumlah contoh yang salah diklasifikasikan sebagai positif (spam) oleh model, padahal sebenarnya bukan spam.
    True Positives: Ini adalah jumlah contoh yang benar diklasifikasikan sebagai positif (spam) oleh model.
    False Negatives: Ini adalah jumlah contoh yang salah diklasifikasikan sebagai negatif (bukan spam) oleh model, padahal sebenarnya spam.
    True Negatives: Ini adalah jumlah contoh yang benar diklasifikasikan sebagai negatif (bukan spam) oleh model.
    Binary Accuracy: Metrik ini mengukur akurasi keseluruhan model dalam mengklasifikasikan contoh sebagai positif (spam) atau negatif (bukan spam). Ini dihitung sebagai rasio dari jumlah prediksi yang benar (True Positives + True Negatives) dibagi dengan jumlah total contoh. Dalam kasus ini, nilai akurasi yang diberikan adalah 0.9018, yang menunjukkan bahwa model memiliki akurasi sebesar 90.18% dalam memprediksi apakah sebuah email adalah spam atau bukan spam.

    ExampleCount: 112
    AUC: 0.97259
    False Positives: 3
    True Positives: 60
    False Negatives: 8
    True Negatives: 41
    Binary Accuracy: 90.18%

## Requirements
- Python 3.x
- TensorFlow
- TensorFlow Extended (TFX)
- Scikit-learn
- Pandas
- Flask
- Joblib

## Cara Penggunaan
1. Instal semua kebutuhan dengan menjalankan perintah `pip install -r requirements.txt`.
2. Jalankan notebook `pipeline.ipynb` untuk membangun dan melatih model.
3. Setelah model dilatih, Anda dapat menggunakan model tersebut untuk memprediksi apakah sebuah email adalah spam atau bukan.


