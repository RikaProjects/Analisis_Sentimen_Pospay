# Analisis Sentimen & Topik Ulasan Pospay

Proyek ini merupakan **inisiatif pribadi** untuk menganalisis sentimen
dan topik utama dari ulasan pengguna aplikasi **Pospay** yang tersedia
secara publik di **Google Play Store**. Analisis dilakukan menggunakan
pendekatan **Natural Language Processing (NLP)** untuk memahami persepsi
pengguna serta mengidentifikasi isu yang sering muncul dalam ulasan.

---

## Dataset
Dataset diperoleh dari ulasan pengguna aplikasi Pospay di Google Play Store
menggunakan library `google-play-scraper`. Data yang digunakan meliputi:
- Teks ulasan
- Rating pengguna (1–5)
- Tanggal ulasan
- Informasi versi aplikasi

Meskipun aplikasi Pospay memiliki puluhan ribu ulasan di Google Play Store,
pada proyek ini jumlah data yang dianalisis **dibatasi pada 118 ulasan**
untuk keperluan eksplorasi dan efisiensi proses analisis.

Seluruh dataset hasil scraping dan preprocessing disertakan di dalam
folder `data/` agar analisis dapat direplikasi.

---

## Metodologi
Tahapan analisis yang dilakukan meliputi:
1. **Pengambilan Data**  
   Scraping ulasan pengguna aplikasi Pospay dari Google Play Store.
2. **Preprocessing Teks**  
   Pembersihan dan normalisasi teks ulasan.
3. **Analisis Sentimen**  
   Klasifikasi sentimen ulasan ke dalam kategori *positive*, *neutral*,
   dan *negative* menggunakan model Transformer bahasa Indonesia.
4. **Validasi Sentimen**  
   Perbandingan hasil analisis sentimen dengan rating pengguna.
5. **Topic Modeling**  
   Identifikasi topik utama ulasan menggunakan metode **BERTopic**.

---

## Insight Utama
- Sentimen negatif mendominasi ulasan pengguna, yang menunjukkan masih
  banyaknya keluhan terhadap stabilitas dan fitur aplikasi.
- Beberapa ulasan dengan rating tinggi tetap mengandung sentimen negatif,
  menandakan bahwa rating numerik tidak selalu merepresentasikan isi ulasan.
- Topik utama keluhan berkaitan dengan **kendala login dan verifikasi**,
  **masalah transaksi**, serta **poin dan reward**, sementara ulasan positif
  umumnya bersifat singkat dan umum.

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
- File CSV hasil scraping dan preprocessing (folder `data/`)
- Visualisasi distribusi sentimen dan topik ulasan

---

## Catatan
Proyek ini dibuat sebagai **personal project** untuk eksplorasi analisis
data dan NLP. Hasil analisis bersifat eksploratif dan tidak dimaksudkan
untuk generalisasi terhadap seluruh populasi pengguna aplikasi Pospay.
