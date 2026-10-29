# Tugas Alpro Pertemuan 12: File I/O dan Error Handling

## Identitas

- Nama: Hana Karimah Ghoziyah
- Kelas: 3B
- Mata Kuliah: Algoritma dan Pemrograman
- Pertemuan: 12
- Topik: File I/O dan Error Handling

## Deskripsi Program

Program ini dibuat untuk mempelajari cara membaca, menulis, dan menambahkan data ke dalam file menggunakan Python. Program juga menerapkan penanganan kesalahan (*error handling*) menggunakan `try-except` agar dapat menangani file yang tidak ditemukan dan data yang tidak valid.

Tugas utama berupa program rekap nilai mahasiswa yang membaca data dari `data/nilai.txt`, memproses nilai yang valid, menghitung statistik nilai, kemudian menyimpan hasilnya ke `data/hasil_rekap.txt`.

## Struktur Folder

```text
Pertemuan-12-file-io-2225250165/
├── latihan/
│   ├── 01_tulis_file.py
│   ├── 02_baca_file.py
│   ├── 03_append_file.py
│   ├── 04_proses_baris.py
│   ├── 05_file_not_found.py
│   └── 06_value_error.py
├── tugas/
│   └── rekap_nilai_file.py
├── data/
│   ├── catatan.txt
│   ├── nilai.txt
│   └── hasil_rekap.txt
├── .gitignore
└── README.md
```

## Format Data Nilai

Data nilai disimpan dalam file `data/nilai.txt` dengan format `NIM,nilai`. Setiap baris berisi kode mahasiswa dan nilai yang dipisahkan dengan tanda koma.

Contoh isi file:

```text
A001,85
A002,78
A003,92
A004,abc
A005,74
A006,88
```

Baris dengan nilai yang tidak valid, seperti `A004,abc`, dilewati oleh program. Baris kosong juga tidak ikut diproses.

## Cara Menjalankan Program

1. Buka folder proyek di Visual Studio Code.
2. Buka terminal melalui menu **Terminal → New Terminal**.
3. Jalankan salah satu file latihan, misalnya:

```bash
python latihan/01_tulis_file.py
```

4. Untuk menjalankan program utama, gunakan perintah:

```bash
python tugas/rekap_nilai_file.py
```

5. Periksa hasil rekap yang tersimpan di `data/hasil_rekap.txt`.

Jika perintah `python` tidak bisa digunakan, coba jalankan dengan `python3`.

## Hasil Rekap Nilai

Berdasarkan data pada file `data/nilai.txt`, program menghasilkan rekap berikut:

```text
Jumlah data valid: 5
Rata-rata: 83.40
Minimum: 74.00
Maksimum: 92.00
Jumlah lulus: 5
```

Jumlah data valid adalah 5 karena satu baris memiliki nilai yang tidak valid. Mahasiswa dinyatakan lulus jika memperoleh nilai minimal 60.

## Penanganan Kesalahan

Program menerapkan beberapa penanganan kesalahan berikut:

- `FileNotFoundError`: menangani kondisi ketika file yang akan dibaca tidak ditemukan.
- `ValueError`: menangani nilai yang tidak dapat dikonversi menjadi angka.
- Baris kosong: dilewati agar tidak mengganggu proses pengolahan data.
- Data tidak valid: dilewati sehingga data lain yang valid tetap dapat diproses.

## Hasil Pengujian

| No. | Kasus Pengujian | Hasil yang Diharapkan |
|---|---|---|
| 1 | Data nilai normal | Rekap berhasil dibuat. |
| 2 | Nilai berupa teks, misalnya `abc` | Baris tidak valid dilewati. |
| 3 | Terdapat baris kosong | Baris kosong dilewati. |
| 4 | File input tidak ditemukan | Pesan kesalahan ditampilkan. |
| 5 | Nilai tepat 60 | Nilai dihitung sebagai lulus. |
| 6 | Nilai kurang dari 60 | Nilai tidak dihitung sebagai lulus. |

## Refleksi

Melalui tugas ini, saya belajar menggunakan operasi file untuk menulis, membaca, dan menambahkan data. Saya juga belajar mengolah data dari file teks, menghitung rekap nilai, serta menggunakan `try-except` untuk menangani kesalahan seperti `FileNotFoundError` dan `ValueError`.

Selain itu, saya memahami bahwa penanganan kesalahan membantu program tetap berjalan dengan baik ketika terdapat data yang tidak valid atau file yang tidak ditemukan.

## Kesimpulan

Program rekap nilai berhasil memproses data yang valid, melewati data yang tidak sesuai, menghitung statistik nilai, dan menyimpan hasil rekap ke dalam file. Tugas ini membantu saya memahami penerapan File I/O dan Error Handling dalam pemrograman.