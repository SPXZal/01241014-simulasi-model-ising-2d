# ⚛️ Fisika Komputasi: Simulasi Model Ising 2D via Algoritma Metropolis

Selamat datang di repositori proyek studi kasus komprehensif mengenai **Model Ising 2 Dimensi (2D) dan Transisi Fasa**. Repositori ini berisi implementasi mandiri algoritma Monte Carlo Metropolis untuk mensimulasikan sistem kisi magnetik dua dimensi dan mengamati bagaimana perilaku kolektif partikel memicu terjadinya magnetisasi spontan serta transisi fasa makroskopis.

> 🌐 **Tautan Web Laporan (GitHub Pages):** [KLIK DI SINI UNTUK MELIHAT DASHBOARD SIMULASI](???)

---

## 🎯 Tujuan Proyek
Membangun program simulasi, melakukan analisis matematis serta komputasional terhadap Model Ising 2D pada tiga rentang suhu yang berbeda di dalam ekosistem *Jupyter Notebook*, kemudian memublikasikan hasil temuan tersebut sebagai portofolio web publik menggunakan *GitHub Pages*.

## 📂 Struktur Repositori
- `notebooks/` : Berisi berkas *source code* asli berbasis Jupyter Notebook (`.ipynb`) yang memuat komputasi Monte Carlo dan visualisasi menggunakan matplotlib.
- `docs/` : Berisi hasil kompilasi dokumen dari *Notebook* ke format HTML statis beserta halaman antarmuka utama (`index.html`) untuk keperluan publikasi web/deployment.

---

## 🔬 Studi Kasus & Analisis Termodinamika
Simulasi dijalankan pada kisi berukuran $20 \times 20$ yang diinisialisasi dengan konfigurasi acak (*Hot Start*) untuk merepresentasikan entropi maksimum sistem. Simulasi menempuh minimal 200.000 langkah Monte Carlo untuk mencapai kesetimbangan termal. 

Analisis dibagi ke dalam tiga studi kasus berdasarkan kondisi termodinamika sistem:

1. **Kasus 1: Fase Feromagnetik ($T = 1.0$)**
   Simulasi sistem di bawah suhu kritis ($T < T_c$). Mengamati bagaimana spin individu berorientasi searah secara spontan untuk membentuk domain magnetik yang seragam, sehingga nilai mutlak magnetisasi rata-rata mendekati satu ($|M| \approx 1$).

2. **Kasus 2: Transisi Fasa & Kritikalitas ($T = 2.27$)**
   Mengamati perilaku sistem pada titik suhu kritis teoritis ($T_c \approx 2.27$). Analisis difokuskan pada fluktuasi kritis yang terjadi, pembentukan pola domain fraktal, dan runtuhnya keteraturan jarak jauh.

3. **Kasus 3: Fase Paramagnetik ($T = 4.0$)**
   Meneliti sistem pada rentang suhu tinggi ($T > T_c$). Membuktikan bagaimana energi termal mendominasi interaksi antar-spin sehingga arah spin menjadi acak dan nilai magnetisasi rata-rata jatuh mendekati nol ($M \approx 0$).

---

## 📝 Kriteria Evaluasi Proyek
Pengerjaan tugas dan simulasi di dalam repositori ini telah dirancang untuk memenuhi kriteria evaluasi berikut:

* **Akurasi Matematis dan Fisis:** Ketepatan formulasi matematis dalam menghitung selisih energi lokal $\Delta E = 2s_{i,j} \sum s_{\text{tetangga}}$ dengan menerapkan kondisi batas periodik (*periodic boundary conditions*) menggunakan operasi modulo, serta kebenaran implementasi probabilitas penerimaan Metropolis $\mathcal{R} = e^{-\Delta E / T}$.
* **Efisiensi Komputasi:** Kebersihan struktur kode Python, penulisan dokumentasi/komentar yang informatif, serta optimalisasi algoritma dengan memanfaatkan perhitungan energi lokal alih-alih menghitung ulang energi total seluruh kisi pada setiap iterasi.
* **Komunikasi Ilmiah:** Kejelasan visualisasi data yang disajikan (kelengkapan label sumbu, judul grafik, dan skala yang tepat) serta kedalaman analisis teoretis fisis yang dituliskan pada penjelasan teks.

---

## 🛠️ Metodologi & Atribusi Proyek

### 🤖 Penggunaan AI
Pada pengerjaan *case-based* ini, saya menggunakan:
* **Gemini 1.5 Pro** untuk mendesain struktur UI/UX dokumen web (HTML/CSS), menyuntikkan *styling* premium pada hasil kompilasi *Jupyter Notebook*, serta memperbaiki (*debugging*) struktur tag *Markdown* yang rusak pada dokumen statis HTML.

### 💻 Penggunaan Aplikasi Lain
* **Jupyter Software / Lab** untuk menyediakan lingkungan eksekusi kode secara interaktif, penulisan analisis berbasis teks formal, dan penampilan visualisasi kurva magnetisasi serta peta biner secara *inline*.
* **Visual Studio Code / Notepad** untuk mengedit susunan kode antarmuka HTML dan CSS secara manual pada langkah finalisasi *deployment*.

### 📚 Referensi dan Sumber Data
1.  Landau, D. P., dkk. *A Guide to Monte Carlo Simulations in Statistical Physics* (Bab 17.2: Aturan Implementasi).
2.  Rifani, Agus. *Modul Pembelajaran: Simulasi Model Magnet dan Transisi Fasa*.

---
*Disusun oleh **Muhammad Afrizal** (Kelompok SPX) untuk memenuhi evaluasi Praktikum Fisika Komputasi 2026.*
