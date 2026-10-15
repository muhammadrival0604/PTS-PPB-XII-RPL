## PRAKTIKUM REST API – CRUD
### Studi Kasus: Sistem Manajemen Produk Elektronik

**Mata Pelajaran:** Pemrograman Perangkat Lunak  
**Kelas:** XII RPL
**Bentuk Ujian:** Praktikum Kelompok
**Waktu:** 120 Menit  
**Tingkat Kesulitan:** HOTS
**Total Nilai:** 100

---

## A. STUDI KASUS

Sebuah toko elektronik membutuhkan sistem untuk mengelola
data produk melalui REST API.

Sebagai seorang pengembang perangkat lunak, Anda ditugaskan
melakukan pengujian REST API untuk memastikan sistem dapat:

1. Menambahkan produk baru.
2. Menampilkan seluruh data produk.
3. Menampilkan produk berdasarkan ID.
4. Memperbarui informasi produk.
5. Menghapus produk.
6. Menganalisis kesalahan pada pengujian API.

Pengujian dilakukan menggunakan **MockAPI** dan
**Postman atau ReqBin**.

---

## B. PERSIAPAN PRAKTIKUM

1. Buka website MockAPI.
2. Buat project baru dengan nama `PTS_TOKO_ELEKTRONIK`.
3. Buat resource bernama `produk`.
4. Buat struktur data berikut:

| No | Field | Tipe Data |
|---|---|---|
| 1 | id | ID Otomatis |
| 2 | nama_produk | String |
| 3 | kategori | String |
| 4 | harga | Number |
| 5 | stok | Number |
| 6 | merek | String |

5. Salin endpoint API yang telah dibuat.
6. Buka Postman atau ReqBin untuk melakukan pengujian.

**Catatan:** Setiap siswa wajib menggunakan project
MockAPI masing-masing.

---

# C. SOAL PRAKTIKUM

## SOAL 1 – POST: MENAMBAHKAN PRODUK
**Bobot: 20 Poin**

Sebuah toko elektronik ingin menambahkan tiga produk
baru ke dalam sistem.

Gunakan metode `POST` untuk memasukkan data berikut.

**Endpoint:**

`/produk`

### Produk 1 – Laptop

```json
{
  "nama_produk": "Laptop Aspire 5",
  "kategori": "Laptop",
  "harga": 8500000,
  "stok": 10,
  "merek": "Acer"
}
```

### Produk 2 – Keyboard

```json
{
  "nama_produk": "Keyboard K120",
  "kategori": "Aksesoris",
  "harga": 150000,
  "stok": 25,
  "merek": "Logitech"
}
```

### Produk 3 – Mouse

```json
{
  "nama_produk": "Mouse G102",
  "kategori": "Aksesoris",
  "harga": 250000,
  "stok": 15,
  "merek": "Logitech"
}
```

### Instruksi Pengerjaan

1. Gunakan metode HTTP `POST`.
2. Masukkan endpoint yang telah dibuat.
3. Pilih Body dengan format JSON.
4. Kirim ketiga data secara terpisah.
5. Catat ID setiap produk yang diberikan server.
6. Pastikan seluruh produk berhasil ditambahkan.
7. Ambil screenshot hasil pengujian.

### Pertanyaan

1. Berapa status code yang diperoleh?
2. Mengapa setiap produk memiliki ID berbeda?

---

## SOAL 2 – GET: MENAMPILKAN PRODUK
**Bobot: 15 Poin**

Setelah produk berhasil ditambahkan, lakukan
pengujian untuk menampilkan data produk.

### Pengujian A – Menampilkan Semua Produk

**Method:** `GET`

**Endpoint:**

`/produk`

### Pengujian B – Menampilkan Produk Berdasarkan ID

**Method:** `GET`

**Endpoint:**

`/produk/{id}`

Gunakan ID produk Laptop Aspire 5.

### Instruksi Pengerjaan

1. Lakukan GET untuk menampilkan seluruh produk.
2. Periksa response JSON yang diterima.
3. Lakukan GET berdasarkan ID Laptop Aspire 5.
4. Catat status code setiap pengujian.
5. Ambil screenshot hasil pengujian.

### Pertanyaan

1. Berapa jumlah produk yang berhasil ditampilkan?
2. Apa perbedaan GET seluruh produk dan GET berdasarkan ID?

---

## SOAL 3 – PUT: MEMPERBARUI PRODUK
**Bobot: 20 Poin**

Toko elektronik sedang mengadakan promo sehingga
harga dan stok Laptop Aspire 5 harus diperbarui.

### Data Perubahan

| Field | Sebelum | Sesudah |
|---|---|---|
| nama_produk | Laptop Aspire 5 | Laptop Aspire 5 |
| kategori | Laptop | Laptop |
| harga | 8500000 | 7500000 |
| stok | 10 | 20 |
| merek | Acer | Acer |

**Method:** `PUT`

**Endpoint:**

`/produk/{id}`

### Instruksi Pengerjaan

1. Temukan ID produk Laptop Aspire 5.
2. Gunakan metode HTTP PUT.
3. Ubah harga menjadi Rp7.500.000.
4. Ubah stok menjadi 20 unit.
5. Pastikan data lainnya tidak berubah.
6. Lakukan GET berdasarkan ID untuk memastikan
   perubahan berhasil.
7. Ambil screenshot sebelum dan sesudah perubahan.

### Pertanyaan

1. Mengapa metode PUT digunakan untuk memperbarui data?
2. Bagaimana cara memastikan perubahan berhasil?

---

## SOAL 4 – DELETE: MENGHAPUS PRODUK
**Bobot: 15 Poin**

Produk Keyboard K120 sudah tidak dijual lagi.

Oleh karena itu, produk tersebut harus dihapus
dari sistem.

**Method:** `DELETE`

**Endpoint:**

`/produk/{id}`

### Instruksi Pengerjaan

1. Temukan ID produk Keyboard K120.
2. Gunakan metode HTTP DELETE.
3. Hapus produk berdasarkan ID.
4. Lakukan GET untuk memastikan produk terhapus.
5. Ambil screenshot hasil pengujian.

### Pertanyaan

1. Apa fungsi metode DELETE?
2. Berapa jumlah produk yang tersisa setelah penghapusan?

---

## SOAL 5 – ANALISIS DAN DEBUGGING API
**Bobot: 20 Poin**

Lakukan pengujian terhadap dua kondisi berikut.

### KASUS A – PRODUK TIDAK DITEMUKAN

Gunakan metode `GET` dengan endpoint:

`/produk/999999`

Pastikan ID tersebut tidak tersedia.

**Tugas:**

1. Jalankan request GET.
2. Catat status code yang diperoleh.
3. Amati response dari server.
4. Jelaskan penyebab kesalahan.
5. Tuliskan cara memperbaiki request tersebut.

### KASUS B – METODE HTTP TIDAK SESUAI

Gunakan metode `POST` dengan endpoint:

`/produk/{id}`

Gunakan ID produk yang masih tersedia.

**Tugas:**

1. Jalankan request POST.
2. Catat status code yang diperoleh.
3. Amati response dari server.
4. Jelaskan penyebab kegagalan atau hasil yang
   tidak sesuai.
5. Tentukan metode HTTP dan endpoint yang tepat
   untuk memperbarui produk tersebut.

**Catatan:**

Status code dan response dapat berbeda sesuai
layanan API yang digunakan. Jelaskan berdasarkan
hasil pengujian sebenarnya.

---

## SOAL 6 – LAPORAN HASIL PRAKTIKUM
**Bobot: 10 Poin**

Buat laporan hasil pengujian REST API menggunakan
PowerPoint, Canva, atau Google Slides.

Presentasi minimal terdiri dari 7 slide.

### Struktur Presentasi

| Slide | Isi Presentasi |
|---|---|
| 1 | Cover, nama, dan kelas |
| 2 | Penjelasan REST API dan endpoint |
| 3 | Screenshot pengujian POST |
| 4 | Screenshot pengujian GET |
| 5 | Screenshot pengujian PUT |
| 6 | Screenshot pengujian DELETE |
| 7 | Hasil debugging dan kesimpulan |

### Ketentuan Laporan

Setiap screenshot pengujian wajib memperlihatkan:

1. Metode HTTP yang digunakan.
2. Endpoint API.
3. Request Body (jika digunakan).
4. Response Body.
5. HTTP Status Code.

---

# D. RUBRIK PENILAIAN

| No | Aspek Penilaian | Bobot |
|---|---|---|
| 1 | Keberhasilan POST | 20 |
| 2 | Keberhasilan GET | 15 |
| 3 | Keberhasilan PUT | 20 |
| 4 | Keberhasilan DELETE | 15 |
| 5 | Analisis dan Debugging API | 20 |
| 6 | Laporan Praktikum | 10 |
| | **TOTAL** | **100** |

---

# E. KETENTUAN PENGUMPULAN

1. Praktikum dikerjakan secara individu.
2. Setiap kelompok wajib membuat project MockAPI sendiri.
3. Pengujian harus mencakup GET, POST, PUT, dan DELETE.
4. Setiap pengujian wajib disertai screenshot.
5. Laporan dikumpulkan dalam format PDF.
6. Gunakan format nama file:

   `PTS_API_NAMA_KELAS.pdf`

---

# F. CATATAN PENTING

- Pastikan koneksi internet stabil.
- Gunakan endpoint API milik sendiri.
- Perhatikan penggunaan metode HTTP.
- Pastikan format JSON yang dikirimkan benar.
- Periksa status code setiap pengujian.
- Jangan menghapus data sebelum menyelesaikan
  pengujian GET dan PUT.
- Screenshot harus berasal dari hasil
  pengujian sendiri.

---

**SELAMAT MENGERJAKAN!**

