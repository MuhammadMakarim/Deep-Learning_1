# 🌟 Sentiment Analysis
## 🚀 Deskripsi Proyek
Proyek ini mengimplementasikan analisis sentimen berbasis bahasa indonesia terhadap ulasan aplikasi WhatsApp. Data ulasan diambil melalui Google Playstore. Proyek ini mengkasifikasikan sentimen user aplikasi menjadi postif, netral, dan negatif. Proyek ini juga menggunakan berbagai pendekatan representasi teks dan algoritma klasifikasi untuk membandingkan performa model.

## 📊Dataset
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

## 💡 Skema Pelatihan & Metode
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

## 🔍 Preprocessing
1. Tokenisasi
2. Pembersihan teks
3. Padding sequence

## 🔬 Ringkasan Evaluasi Model
Metrik Evaluasi
1. Akurasi
2. Presisi
3. Recall
4. F1-Score

## 🧠 Performa Model
**📈 SVM dengan TF-IDF (80/20)**
1. Akurasi Training: 0.9806 (98.06%)
2. Akurasi Testing: 0.9375 (93.75%)
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.91 | 0.74 | 0.82 |  
| Netral | 0.86 | 0.84 | 0.90 |  
| Positif | 0.98 | 0.97 | 0.98 |  

**📈 SVM dengan TF-IDF (60/40)**
1. Akurasi Training: 0.9777 (97.77%)
2. Akurasi Testing: 0.9587 (95.87%)
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.94 | 0.83 | 0.88 |  
| Netral | 0.91 | 0.95 | 0.93 |  
| Positif | 0.99 | 0.98 | 0.98 |

**📈 Random Forest dengan TF-IDF (70/30)**
1. Akurasi Training: 0.8888 (88.88%)
2. Akurasi Testing: 0.8681 (86.81%)
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.91 | 0.62 | 0.74 |  
| Netral | 0.85 | 0.80 | 0.82 |  
| Positif | 0.90 | 0.97 | 0.94 |

**📈 Random Forest dengan TF-IDF (80/20**)
1. Akurasi Training: 0.8924 (89.24%)
2. Akurasi Testing: 0.8672 (86.72%)
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.90 | 0.64 | 0.75|  
| Netral | 0.86 | 0.80| 0.83 |  
| Positif | 0.90 | 0.98 | 0.94 |

**📈 LSTM dengan TF-IDF (70/20/10)**
1. Akurasi Training: 0.99
2. Akurasi Validasi: 0.96
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.94 | 0.87 | 0.90|  
| Netral | 0.91 | 0.94| 0.93 |  
| Positif | 0.98 | 0.98 | 0.98|

**📈 SVM dengan BoW (80/20)**
1. Akurasi Training: 0.99
2. Akurasi Validasi: 0.96
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.90 | 0.92 | 0.91|  
| Netral | 0.93 | 0.94| 0.93 |  
| Positif | 0.99 | 0.98 | 0.98|

**📈 SVM dengan N-Gram (80/20**)
1. Akurasi Training: 0.96
2. Akurasi Testing: 0.93
3. Metrik per Kelas:

| Kelas | Precision | Recall | F1-Score |  
|-------|---------|---------|--------|  
| Negatif | 0.81 | 0.87 | 0.84|  
| Netral |0.87 | 0.91|0.89 |  
| Positif | 0.98 | 0.95 | 0.97|

## 🔑 Kesimpulan
*   LSTM dan SVM dengan TF-IDF menunjukkan performa terbaik
*   Semua model memiliki akurasi di atas 90%
*   Kelas Positif konsisten memiliki performa tertinggi

## 📝 Catatan
1. Dataset lengkap bisa diakses pada link: https://drive.google.com/drive/folders/1jZWJBYjiz7sV5a8Xz2Uv8XS8nfkCOsuc?usp=sharing
2. Models lengkap bisa diakses pada link: https://drive.google.com/drive/folders/10ZVid-v4oLQrOV5A86jqSfRujdYxG-xq?usp=sharing
