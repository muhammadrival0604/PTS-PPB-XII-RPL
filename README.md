# PTS-PPB-XII-RPL

PRAKTIKUM REST API – CRUD

Studi Kasus: Sistem Manajemen Produk Elektronik

Mata Pelajaran: Pemrograman Perangkat Lunak
Kelas: XI PPLG
Bentuk Ujian: Praktikum Individu
Waktu: 120 Menit
Tingkat Kesulitan: Sulit
Total Nilai: 100

---

A. STUDI KASUS

Sebuah toko elektronik membutuhkan sistem untuk mengelola data produk melalui REST API.

Sebagai seorang pengembang perangkat lunak, Anda ditugaskan melakukan pengujian API untuk memastikan sistem dapat menampilkan, menambahkan, memperbarui, dan menghapus produk.

Pengujian dilakukan menggunakan MockAPI dan Postman atau ReqBin.

B. PERSIAPAN

1. Buat project baru di MockAPI dengan nama "UTS_TOKO_ELEKTRONIK".
2. Buat resource bernama "produk".
3. Tentukan struktur data berikut:

Field| Tipe Data
id| ID otomatis
nama_produk| String
kategori| String
harga| Number
stok| Number
merek| String

4. Salin endpoint API yang telah dibuat.
5. Gunakan Postman atau ReqBin untuk melakukan pengujian.

---

SOAL 1 – POST: MENAMBAHKAN PRODUK (20 POIN)

Tambahkan tiga produk elektronik menggunakan metode POST.

Endpoint: "/produk"

Produk 1: Laptop

{
  "nama_produk": "Laptop Aspire 5",
  "kategori": "Laptop",
  "harga": 8500000,
  "stok": 10,
  "merek": "Acer"
}

Produk 2: Keyboard

{
  "nama_produk": "Keyboard K120",
  "kategori": "Aksesoris",
  "harga": 150000,
  "stok": 25,
  "merek": "Logitech"
}

Produk 3: Mouse

{
  "nama_produk": "Mouse G102",
  "kategori": "Aksesoris",
  "harga": 250000,
  "stok": 15,
  "merek": "Logitech"
}

Instruksi:

1. Gunakan metode POST.
2. Tambahkan ketiga produk secara terpisah.
3. Pastikan seluruh produk berhasil ditambahkan.
4. Catat ID setiap produk yang diberikan server.
5. Ambil screenshot hasil pengujian.

---

SOAL 2 – GET: MENAMPILKAN PRODUK (15 POIN)

Lakukan pengujian untuk mengambil data produk yang telah ditambahkan.

Endpoint: "/produk"

Instruksi:

1. Gunakan metode GET.
2. Tampilkan seluruh data produk.
3. Lakukan GET berdasarkan ID untuk menampilkan produk Laptop Aspire 5.
4. Catat status code yang diperoleh.
5. Ambil screenshot hasil pengujian.

Pertanyaan:

a. Berapa jumlah produk yang berhasil ditampilkan?

b. Apa perbedaan GET seluruh produk dan GET berdasarkan ID?

---

SOAL 3 – PUT: MEMPERBARUI PRODUK (20 POIN)

Toko elektronik sedang mengadakan promo sehingga harga dan stok Laptop Aspire 5 mengalami perubahan.

Data perubahan:

- Harga awal: Rp8.500.000
- Harga baru: Rp7.500.000
- Stok awal: 10 unit
- Stok baru: 20 unit

Endpoint: "/produk/{id}"

Instruksi:

1. Temukan ID produk Laptop Aspire 5.
2. Gunakan metode PUT.
3. Perbarui harga dan stok sesuai ketentuan.
4. Pertahankan informasi produk lainnya.
5. Lakukan GET untuk memastikan data telah berubah.
6. Ambil screenshot sebelum dan sesudah perubahan.

Pertanyaan:

a. Mengapa metode PUT digunakan dalam pengujian ini?

b. Bagaimana cara memastikan data benar-benar diperbarui?

---

SOAL 4 – DELETE: MENGHAPUS PRODUK (15 POIN)

Produk Keyboard K120 sudah tidak dijual lagi sehingga harus dihapus dari sistem.

Endpoint: "/produk/{id}"

Instruksi:

1. Temukan ID produk Keyboard K120.
2. Gunakan metode DELETE.
3. Hapus produk berdasarkan ID.
4. Lakukan GET untuk memastikan produk tidak tersedia.
5. Ambil screenshot hasil pengujian.

Pertanyaan:

a. Apa fungsi metode DELETE?

b. Berapa jumlah produk yang tersisa setelah penghapusan?

---

SOAL 5 – ANALISIS DAN DEBUGGING API (20 POIN)

Lakukan pengujian terhadap dua kondisi berikut.

Kasus A – Produk Tidak Ditemukan

Lakukan GET menggunakan ID produk yang tidak tersedia.

Contoh endpoint:

"/produk/999999"

Kasus B – Kesalahan Metode HTTP

Lakukan POST ke endpoint produk berdasarkan ID.

Contoh endpoint:

"/produk/1"

Instruksi:

1. Jalankan kedua pengujian.
2. Catat status code dan response yang diperoleh.
3. Jelaskan penyebab kegagalan atau hasil yang tidak sesuai.
4. Tentukan metode HTTP atau endpoint yang seharusnya digunakan.
5. Sertakan screenshot hasil pengujian.

Catatan: Gunakan ID produk yang benar-benar tersedia untuk kasus B. Hasil status code mengikuti respons layanan API yang digunakan.

---

SOAL 6 – LAPORAN PRAKTIKUM (10 POIN)

Buat laporan hasil pengujian menggunakan PowerPoint, Canva, atau Google Slides.

Minimal 7 slide:

Slide| Isi
1| Cover dan identitas
2| Penjelasan API dan endpoint
3| Hasil pengujian POST
4| Hasil pengujian GET
5| Hasil pengujian PUT
6| Hasil pengujian DELETE
7| Debugging dan kesimpulan

Setiap pengujian wajib disertai screenshot yang memperlihatkan endpoint, metode HTTP, status code, dan response.

C. RUBRIK PENILAIAN

No.| Aspek Penilaian| Bobot
1| Keberhasilan POST| 20
2| Keberhasilan GET| 15
3| Keberhasilan PUT| 20
4| Keberhasilan DELETE| 15
5| Analisis dan debugging| 20
6| Laporan praktikum| 10
| TOTAL| 100

D. KETENTUAN PENGUMPULAN

1. Praktikum dikerjakan secara individu.
2. Setiap peserta wajib membuat project MockAPI sendiri.
3. Pengujian harus mencakup GET, POST, PUT, dan DELETE.
4. Setiap pengujian wajib dilengkapi screenshot.
5. Laporan dikumpulkan dalam format PDF.
6. Nama file: "UTS_API_NAMA_KELAS.pdf".

Selamat mengerjakan!
