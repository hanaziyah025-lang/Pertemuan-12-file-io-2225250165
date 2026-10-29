# Pertemuan 12 - File I/O dan Error Handling

**Nama:** Hana Karimah Ghoziyah  
**NIM:** 2225250165  
**Kelas:** 3B

## Tujuan

Mempelajari cara membaca, menulis, menambahkan, dan mengolah data dari file serta menangani kesalahan menggunakan exception handling.

## Struktur Proyek

```text
Pertemuan-12-file-io-2225250165/
├── data/
│   ├── catatan.txt
│   ├── nilai.txt
│   └── hasil_rekap.txt
├── latihan/
│   ├── 01_tulis_file.py
│   ├── 02_baca_file.py
│   ├── 03_append_file.py
│   ├── 04_proses_baris.py
│   ├── 05_file_not_found.py
│   └── 06_value_error.py
├── tugas/
│   └── rekap_nilai_file.py
├── .gitignore
└── README.md
```

## Format File Input

Program membaca data dari file `data/nilai.txt`. Setiap baris berisi NIM dan nilai yang dipisahkan dengan tanda koma.

Contoh isi file:

```text
A001,85
A002,78
A003,92
A004,abc
A005,74
A006,88
```

Data dengan nilai yang tidak dapat dikonversi menjadi angka akan dilewati, sedangkan data valid tetap diproses.

## Cara