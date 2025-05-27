# Sentiment Analysis
## Deskripsi Proyek
Proyek ini mengimplementasikan analisis sentimen berbasis bahasa indonesia terhadap ulasan aplikasi WhatsApp. Data ulasan diambil melalui Google Playstore. Proyek ini mengkasifikasikan sentimen user aplikasi menjadi postif, netral, dan negatif. Proyek ini juga menggunakan berbagai pendekatan representasi teks dan algoritma klasifikasi untuk membandingkan performa model.

## Dataset
*   Sumber Data: Scraping ulasan user aplikasi WhatsApp menggunakan `google-play-scraper` 
*   Jumlah Data: 500.000
*   Jumlah Sample Untuk Model: 20.000
*   Label Sentimen: Positif, Netral, dan Negatif'
*   File Dataset:
  1. `WhatsApp_review.csv` -> Jumlah Data total
  2. `WhatsApp_review_sample.csv` -> Jumlah Data sample yang digunakan untuk training dan testing
  3. `slangwords.txt` -> Kamus kata gaul atau slang
  4. `data_bersih.csv` -> `WhatsApp_review_sample.csv` setelah dilakukan Text Preprocessing
  5. `data_bersih_berlabel.csv` -> `data_bersih.csv` setelah dilakukan pelabelan
  6. `positive.csv` -> Kamus kata-kata postif
  7. `negative.csv` -> Kamus kata-kata Negatif

## Skema Pelatihan & Metode
### Teknik Representasi Teks
1. N-Gram
Metode: Ekstraksi fitur berbasis n-gram
2. Bag of Words (BoW)
Representasi vektor frekuensi kata
3. TF-IDF
Total fitur: 10000
Pembobotan frekuensi dan kepentingan kata

### Model Klasifikasi
1. Support Vector Machine (SVM)
Variasi:
*   SVM N-Gram
*   SVM BoW
*   SVM TF-IDF (2 varian: 80-20 dan 60-40 split)
2. Random Forest
Variasi TF-IDF:
*   RF 80-20
*   RF 70-30
3. Long Short-Term Memory (LSTM)
Jaringan neural berbasis sequential

## Preprocessing
1. Tokenisasi
2. Pembersihan teks
3. Padding sequence

## Ringkasan Evaluasi Model
Metrik Evaluasi
1. Akurasi
2. Presisi
3. Recall
4. F1-Score

