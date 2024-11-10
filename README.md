# Proyek Natural Language Processing: Representasi Teks Ulasan Game "Honor of King"

Repositori ini berisi kode untuk proyek **Natural Language Processing (NLP)** yang bertujuan untuk merepresentasikan teks ulasan dari game **Honor of King** di Play Store menggunakan teknik **TF-IDF (Term Frequency - Inverse Document Frequency)**. Proyek ini merupakan bagian dari tugas kuliah **Natural Language Programming** pada program studi **Teknik Informatika** di **Universitas Muhammadiyah Riau**.

## Deskripsi Proyek

Proyek ini berfokus pada analisis teks ulasan yang diambil dari Play Store untuk game "Honor of King". Menggunakan teknik TF-IDF, kita dapat menilai seberapa penting suatu kata dalam satu ulasan dibandingkan dengan keseluruhan kumpulan ulasan. Representasi ini sangat berguna untuk memahami kata atau frasa yang sering muncul dan signifikan dalam feedback pengguna terhadap game tersebut.

### Komponen Utama

1. **Prapemrosesan Data**: 
   - Teks ulasan diproses agar siap untuk dianalisis. Tahap ini meliputi pembersihan teks, tokenisasi, dan penghapusan kata umum (stopwords).
   - Stemming menggunakan `Sastrawi` membantu mengurangi kata ke bentuk dasar, penting untuk Bahasa Indonesia.

2. **Perhitungan TF-IDF**:
   - Menggunakan `TfidfVectorizer` dan `CountVectorizer` dari `sklearn`, kode ini menghasilkan:
     - **TF (Term Frequency)**: Frekuensi kata dalam ulasan yang dinormalisasi.
     - **IDF (Inverse Document Frequency)**: Ukuran pentingnya suatu kata di seluruh kumpulan ulasan.
     - **Matriks TF-IDF**: Matriks gabungan dari TF dan IDF yang memberi bobot pada kata berdasarkan frekuensi dan signifikansi dalam seluruh dataset ulasan.

3. **Analisis N-gram**:
   - Kode mendukung analisis unigram, bigram, dan trigram untuk menangkap hubungan kata serta konteks dalam ulasan pengguna.

### File

- **representasi-text-honor-of-king-2.ipynb**: Notebook Jupyter yang berisi kode lengkap dan penjelasan.
- **README.md**: File dokumentasi ini.

## Prasyarat
- Python 3.12.0
- Pustaka yang dibutuhkan:
  - `pandas` - untuk manipulasi data dalam bentuk DataFrame.
  - `scikit-learn` - untuk perhitungan TF-IDF, vektorisasi, dan normalisasi.
  - `nltk` - untuk pemrosesan bahasa alami tambahan, seperti stopwords.
  - `Sastrawi` - untuk stemming Bahasa Indonesia.
