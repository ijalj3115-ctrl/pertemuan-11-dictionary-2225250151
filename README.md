# Pertemuan 11 - Dictionary/Map

Nama: Rijal Munawarudin
NIM: 2225250151
Kelas: 3F
## Tujuan
Memodelkan data pendidikan menggunakan dictionary dan pasangan key-value.

## Struktur Data
Jelaskan key utama dan value yang digunakan.
- Key Utama: NIM (Nomor Induk Mahasiswa) bertipe data string (contoh: "A001", "A002").
- Value: Sub-dictionary bertipe data dict yang memuat detail informasi mahasiswa berupa pasang key-value yaitu 'nama' (string), 'kelas' (string), dan 'nilai' (integer).

## Cara Menjalankan
python3 praktik/data_mahasiswa.py

## Test Case
Catat input/aksi, hasil yang diharapkan, hasil aktual, dan status.

| Kasus | Input/Aksi | Hasil yang Diharapkan | Hasil Aktual | Status |
| :--- | :--- | :--- | :--- | :--- |
| Pencarian tersedia | A003 | Data Citra ditampilkan | `{'nama': 'Citra', 'kelas': 'B', 'nilai': 92}` | Sukses |
| Pencarian tidak tersedia | A999 | Pesan 'Data tidak ditemukan' | `Data tidak ditemukan` | Sukses |
| Pembaruan nilai | A002 menjadi 82 | Nilai A002 berubah menjadi 82 | Nilai A002 sukses diperbarui dalam rekap | Sukses |
| Penambahan data | A006 | Key A006 tersedia setelah ditambahkan | Key A006 sukses muncul pada akhir rekap | Sukses |
| Rekap | items() | Semua NIM dan data tampil | Semua data dari NIM A001 sampai A006 serta nilai rata-rata (85.17) berhasil dicetak ke terminal | Sukses |

## Refleksi
Jelaskan satu kesalahan akses key yang ditemukan dan cara memperbaikinya.
- Masalah: Mengakses data dengan format `data["key"]` langsung tanpa memeriksa keberadaan key tersebut dapat memicu error fatal `KeyError` apabila key yang dicari tidak terdaftar atau tidak ada dalam dictionary (seperti saat mencari NIM "A999").
- Cara Memperbaiki: Menggunakan metode bawaan dictionary yaitu `.get(key, default_value)`. Metode ini lebih aman karena jika key tidak ditemukan, program tidak akan *crash* melainkan mengembalikan nilai alternatif atau pesan teks default yang sudah kita tentukan, misalnya pesan `"Data tidak ditemukan"`.
ketika NIM tidak ditemukan.
