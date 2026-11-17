# Komputasi-Numerik
Tugas 1
Komputasi Numerik

Repositori ini berisi tugas mata kuliah Komputasi Numerik: penyelesaian sistem persamaan linear dengan Eliminasi Gauss dan persamaan non linear dengan Metode Bisection, dikerjakan dengan Python di Google Colab.

Nama: Farel Rahmanda
NIM: 202511420108
Kelas: C
Daftar Isi
Struktur Repositori
Bagian 1: Eliminasi Gauss
Bagian 2: Metode Bisection
Cara Menjalankan
Video Penjelasan
Penggunaan AI
Tautan Akun
Struktur Repositori
Komputasi-Numerik/
├── README.md
├── link_akun.txt                    # Link GitHub, Google Colab, LinkedIn
├── no5_algoritma_gauss.txt          # Algoritma Eliminasi Gauss
├── no6-7_gauss_3_variabel.ipynb     # Kode Python (Colab) + komentar tiap baris
├── no9_prompt_AI.txt                # Seluruh prompt AI yang digunakan
├── video_gauss.mp4                  # Video penjelasan Gauss
├── no12_algoritma_bisection.txt     # Algoritma Bisection
├── no12_bisection.ipynb             # Kode Python (Colab) Bisection
└── video_bisection.mp4              # Video penjelasan Bisection

Sesuaikan daftar ini dengan nama file yang benar-benar ada di repositori Anda.

Bagian 1: Eliminasi Gauss (Sistem Persamaan Linear 3 Variabel)

Ide dasar: ubah sistem persamaan menjadi bentuk segitiga atas (eliminasi maju), lalu hitung variabel dari bawah ke atas (substitusi mundur). Program memakai partial pivoting agar hasil lebih akurat.

Contoh soal:

 2x +  y -  z =   8
-3x -  y + 2z = -11
-2x +  y + 2z =  -3

Hasil: x = 2, y = 3, z = -1

Langkah algoritma:

Gabungkan koefisien dan konstanta menjadi matriks augmented [A | b].
Eliminasi maju: cari pivot terbesar, tukar baris bila perlu, lalu nolkan elemen di bawah pivot.
Substitusi mundur: hitung z, lalu y, lalu x.
Bagian 2: Metode Bisection (Persamaan Non Linear)

Ide dasar: jika f(a) dan f(b) berbeda tanda, ada akar di antara a dan b. Interval dibagi dua berulang kali sampai cukup kecil.

Contoh soal: f(x) = x³ − x − 2 = 0 pada interval [1, 2]

Hasil: akar ≈ 1.521380 (20 iterasi, toleransi 10⁻⁶)

Langkah algoritma:

Pastikan f(a) · f(b) < 0.
Hitung titik tengah c = (a + b) / 2.
Jika f(a) · f(c) < 0, maka b = c. Jika tidak, a = c.
Ulangi sampai (b − a) / 2 lebih kecil dari toleransi.
Cara Menjalankan
Buka Google Colab.
Pilih File → Upload notebook, lalu pilih file .ipynb dari repositori ini.
Klik Runtime → Run all, atau jalankan cell satu per satu.

Library yang dipakai: numpy dan matplotlib (sudah tersedia di Colab).

Video Penjelasan
Eliminasi Gauss: video_gauss.mp4
