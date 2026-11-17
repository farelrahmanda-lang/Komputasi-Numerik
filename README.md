Komputasi Numerik

Tugas mata kuliah Komputasi Numerik: penyelesaian sistem persamaan linear dengan Eliminasi Gauss dan persamaan non linear dengan Metode Bisection menggunakan Python di Google Colab.

	
Nama	[Farel Rahmanda]
NIM	[202511420108]
Kelas	[C]

Daftar Isi
Deskripsi Tugas
Permasalahan
Metode Penyelesaian
Struktur Repository
Cara Menjalankan Program
Hasil Penyelesaian
Validasi Hasil
Penutup

**[Tonton Video Demonstrasi Komputasi Numerik](https://drive.google.com/drive/folders/1DaNE66qGuJuspil8-J6YtoQKhbX4ejn3)**

1. Deskripsi Tugas
Tugas ini terdiri dari dua bagian:

Sistem Persamaan Linear 3 variabel: membuat algoritma dan kode Python, lengkap dengan keterangan pada setiap baris kode.
Persamaan Non Linear dengan Metode Bisection: langkah yang sama seperti bagian pertama.

Untuk setiap bagian, dikumpulkan juga algoritma, kode Python di Google Colab (dapat dijalankan per cell), daftar prompt AI yang digunakan, dan video penjelasan berdurasi maksimal 5 menit.

2. Permasalahan
2.1 Sistem Persamaan Linear 3 Variabel

Tentukan nilai x, y, dan z dari sistem berikut:

 2x +  y -  z =   8
-3x -  y + 2z = -11
-2x +  y + 2z =  -3
2.2 Persamaan Non Linear

Tentukan akar dari persamaan berikut pada interval [1, 2]:

f(x) = x³ - x - 2 = 0
3. Metode Penyelesaian
3.1 Eliminasi Gauss (dengan Partial Pivoting)

Sistem persamaan diubah menjadi bentuk segitiga atas, lalu solusinya dihitung dari bawah ke atas.

Gabungkan koefisien dan konstanta menjadi matriks augmented [A | b].
Eliminasi maju: untuk setiap kolom pivot, cari baris dengan nilai mutlak terbesar, tukar baris bila perlu, lalu nolkan elemen di bawah pivot dengan Bi = Bi - faktor × Bk.
Substitusi mundur: hitung z, lalu y, lalu x.
3.2 Metode Bisection

Jika f(a) dan f(b) berlawanan tanda, terdapat akar di antara a dan b. Interval dibagi dua berulang kali sampai cukup kecil.

Pastikan f(a) · f(b) < 0.
Hitung titik tengah c = (a + b) / 2.
Jika f(a) · f(c) < 0, maka b = c. Jika tidak, maka a = c.
Ulangi sampai (b − a) / 2 lebih kecil dari toleransi (10⁻⁶).

4. Struktur Repository
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

Sesuaikan dengan nama file yang benar-benar ada di repository.

5. Cara Menjalankan Program
Buka Google Colab.
Pilih File → Upload notebook, lalu pilih file .ipynb dari repository ini.
Jalankan cell satu per satu secara berurutan, atau klik Runtime → Run all.

Library yang digunakan: numpy dan matplotlib (sudah tersedia di Google Colab, tidak perlu instalasi).

6. Hasil Penyelesaian
6.1 Eliminasi Gauss

Matriks augmented setelah eliminasi maju (bentuk segitiga atas):

[[-3.0000  -1.0000   2.0000  -11.0000]
 [ 0.0000   1.6667   0.6667    4.3333]
 [ 0.0000   0.0000   0.2000   -0.2000]]

Solusi setelah substitusi mundur:

Variabel	Nilai
x	2.0000
y	3.0000
z	-1.0000
6.2 Metode Bisection

Beberapa iterasi pertama dan terakhir:

Iterasi	a	b	c	f(c)	Error
1	1.000000	2.000000	1.500000	-0.125000	0.500000
2	1.500000	2.000000	1.750000	1.609375	0.250000
3	1.500000	1.750000	1.625000	0.666016	0.125000
...	...	...	...	...	...
20	1.521379	1.521381	1.521380	0.000004	0.000001

Akar pendekatan: x ≈ 1.521380 (konvergen pada iterasi ke-20).

7. Validasi Hasil
7.1 Eliminasi Gauss
Substitusi balik: hasil kali A @ x = [8, -11, -3], sama dengan vektor b.
Pembanding: hasil dicocokkan dengan fungsi numpy.linalg.solve, dan keduanya sama (np.allclose bernilai True).
7.2 Metode Bisection
Nilai fungsi di akar: f(1.521380) ≈ 4.27 × 10⁻⁶, sangat dekat dengan nol.
Grafik: kurva f(x) memotong sumbu x di sekitar x ≈ 1.5214, sesuai hasil perhitungan.
8. Penutup

Eliminasi Gauss berhasil menyelesaikan sistem persamaan linear 3 variabel dengan solusi x = 2, y = 3, z = -1. Metode Bisection berhasil menemukan akar f(x) = x³ − x − 2 pada x ≈ 1.521380. Kedua hasil telah divalidasi sehingga program dapat dinyatakan benar.

Penggunaan AI: sebagian tugas dikerjakan dengan bantuan platform AI sesuai ketentuan dosen. Seluruh prompt yang digunakan tersimpan di no9_prompt_AI.txt, dan hasilnya sudah dipelajari serta disesuaikan sendiri.
