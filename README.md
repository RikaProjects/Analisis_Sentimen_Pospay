# Analisis Sentimen & Topik Ulasan Pospay

Proyek ini merupakan **inisiatif pribadi** untuk menganalisis sentimen
dan topik utama pada ulasan pengguna aplikasi **Pospay** yang diambil
dari **Google Play Store**. Tujuan proyek ini adalah untuk memahami
persepsi pengguna serta mengidentifikasi isu yang paling sering
dikeluhkan menggunakan pendekatan **Natural Language Processing (NLP)**.

---

## Dataset
Dataset terdiri dari ulasan pengguna aplikasi Pospay yang mencakup:
- Teks ulasan
- Rating pengguna (1–5)
- Tanggal ulasan
- Informasi versi aplikasi

Total ulasan yang dianalisis: **118 ulasan**.

---

## Metodologi
Tahapan analisis dalam proyek ini meliputi:
1. **Pengambilan Data**  
   Mengambil ulasan aplikasi Pospay dari Google Play Store.
2. **Preprocessing Teks**  
   Pembersihan teks, normalisasi huruf, dan penghapusan kata tidak relevan.
3. **Analisis Sentimen**  
   Klasifikasi ulasan ke dalam sentimen *positive*, *neutral*, dan *negative*
   menggunakan model Transformer bahasa Indonesia.
4. **Validasi Sentimen**  
   Perbandingan hasil analisis sentimen dengan rating pengguna.
5. **Topic Modeling**  
   Identifikasi topik utama ulasan menggunakan metode **BERTopic**.

---

## Insight Utama
- Sentimen negatif mendominasi ulasan pengguna, yang menunjukkan banyaknya
  keluhan terhadap aspek teknis aplikasi.
- Ditemukan bahwa pengguna tetap memberikan kritik meskipun memberikan
  rating tinggi, sehingga analisis berbasis teks mampu menangkap keluhan
  secara lebih detail dibandingkan penilaian rating numerik.
- Topik keluhan utama berkaitan dengan **login dan verifikasi**,
  **kendala transaksi**, serta **poin dan reward**, sementara ulasan
  positif umumnya bersifat umum dan singkat.

---

## Tools & Library
- Python
- Pandas
- Google Play Scraper
- Transformers (IndoBERT / RoBERTa)
- BERTopic
- Matplotlib

---

## Output
- Notebook analisis lengkap (`Analisis_Sentimen_Pospay.ipynb`)
- Visualisasi distribusi sentimen
- Hasil pemodelan topik dan interpretasinya

---

## Catatan
Proyek ini dibuat sebagai **personal project** untuk eksplorasi analisis
data dan NLP pada ulasan aplikasi mobile. Hasil analisis bergantung pada
kualitas data dan model yang digunakan.
