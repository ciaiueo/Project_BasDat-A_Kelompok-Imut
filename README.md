# PRODUCT REQUIREMENTS DOCUMENT (PRD)

## Sistem Basis Data Toko Penjualan Retail

### Kelompok Imut

| No | Nama                       | NPM        |
| -- | -------------------------- | ---------- |
| 1  | Nazwa Aulia Hanifa         | 4525210053 |
| 2  | Nevilla Ghilar Apryanti    | 4525210054 |
| 3  | Nuristya Putri Agustina    | 4525210055 |
| 4  | Ratu Annisaa Nabila Meysun | 4525210063 |
| 5  | Tazkia Putri Arsyad        | 4525210073 |
| 6  | Septia Fitri Rahmadhani    | 4525210097 |

### Link ERD

[ERD](https://drive.google.com/file/d/15H7NKOZa1VQpePpmL8VbLYjteFEjeh94/view?usp=sharing)

---

## 1. Latar Belakang

Toko penjualan retail membutuhkan data yang teratur agar kegiatan penjualan dapat dicatat dengan baik. Data yang perlu dikelola antara lain data barang, pelanggan, pegawai, supplier, dan transaksi penjualan.

Oleh karena itu, dibuat sistem basis data toko penjualan retail untuk membantu menyimpan dan mengelola data tersebut. Dengan adanya sistem ini, data transaksi juga dapat lebih mudah dicatat dan digunakan untuk membuat laporan.

## 2. Tujuan Proyek

Tujuan dari pembuatan sistem basis data ini yaitu:

* Mengelola data barang.
* Mengelola data pelanggan.
* Mengelola data pegawai.
* Mencatat transaksi penjualan.
* Mencatat barang yang dibeli dalam setiap transaksi.
* Membantu pengelolaan stok barang.
* Membantu menghasilkan laporan penjualan.

## 3. Deskripsi Produk

Sistem ini merupakan basis data untuk toko penjualan retail. Data dalam sistem dibagi menjadi beberapa tabel yang saling berhubungan.

Tabel yang digunakan yaitu:

* Barang
* Pelanggan
* Pegawai
* Supplier
* Penjualan
* Detail Penjualan

Tabel Penjualan digunakan untuk menyimpan data transaksi, sedangkan Detail Penjualan digunakan untuk menyimpan barang-barang yang terdapat dalam setiap transaksi.

## 4. Kebutuhan Pengguna

Pengguna sistem membutuhkan beberapa data dan informasi berikut:

| Pengguna       | Kebutuhan                                               |
| -------------- | ------------------------------------------------------- |
| Pegawai        | Mencatat transaksi penjualan dan data pelanggan         |
| Pengelola toko | Mengelola data barang, pegawai, supplier, dan transaksi |
| Pemilik toko   | Melihat informasi dan laporan penjualan                 |

## 5. User Story

Beberapa contoh kebutuhan pengguna dalam sistem:

* Sebagai pegawai, saya ingin mencatat transaksi penjualan agar data penjualan tersimpan.
* Sebagai pegawai, saya ingin mencatat barang yang dibeli pelanggan dalam satu transaksi.
* Sebagai pengelola toko, saya ingin menyimpan data barang agar stok dan harga barang dapat dikelola.
* Sebagai pengelola toko, saya ingin menyimpan data pelanggan dan pegawai.
* Sebagai pemilik toko, saya ingin melihat data penjualan untuk mengetahui transaksi yang sudah dilakukan.

## 6. Ruang Lingkup

### Yang termasuk dalam sistem

* Data barang
* Data pelanggan
* Data pegawai
* Data supplier
* Data penjualan
* Detail penjualan
* Relasi antar tabel
* Data stok barang
* Data harga barang
* Informasi transaksi penjualan

### Yang tidak dibahas dalam sistem

* Pembayaran online
* Aplikasi mobile
* Pengiriman barang
* Sistem promo atau voucher
* Marketplace

## 7. Persyaratan Fungsional

| Kode  | Persyaratan                                                  |
| ----- | ------------------------------------------------------------ |
| FR-01 | Sistem dapat menyimpan data barang.                          |
| FR-02 | Sistem dapat menyimpan data pelanggan.                       |
| FR-03 | Sistem dapat menyimpan data pegawai.                         |
| FR-04 | Sistem dapat menyimpan data supplier.                        |
| FR-05 | Sistem dapat mencatat transaksi penjualan.                   |
| FR-06 | Sistem dapat mencatat detail barang dalam transaksi.         |
| FR-07 | Sistem dapat menyimpan jumlah dan harga barang yang terjual. |
| FR-08 | Sistem dapat menghitung subtotal pada detail penjualan.      |
| FR-09 | Sistem dapat menyimpan total pembayaran transaksi.           |

## 8. Struktur Data

### Barang

* Kode Barang sebagai Primary Key
* Nama Barang
* Kategori
* Satuan
* Harga Jual
* Stok

### Pelanggan

* Kode Pelanggan sebagai Primary Key
* Nama Pelanggan
* Alamat
* No. Telepon

### Pegawai

* Kode Pegawai sebagai Primary Key
* Nama Pegawai
* Jabatan
* No. Telepon

### Penjualan

* No. Faktur sebagai Primary Key
* Tanggal Transaksi
* Kode Pelanggan sebagai Foreign Key
* Kode Pegawai sebagai Foreign Key
* Total Bayar

### Detail Penjualan

* No. Faktur sebagai Foreign Key
* Kode Barang sebagai Foreign Key
* Jumlah
* Harga Satuan
* Sub Total

No. Faktur dan Kode Barang digunakan sebagai Primary Key pada Detail Penjualan.

## 9. Relasi Antar Data

Relasi antar tabel pada sistem yaitu:

* Pelanggan berhubungan dengan Penjualan.
* Pegawai berhubungan dengan Penjualan.
* Penjualan berhubungan dengan Detail Penjualan.
* Detail Penjualan berhubungan dengan Barang.

Satu transaksi penjualan dapat memiliki beberapa barang. Karena itu, data barang yang dibeli disimpan pada tabel Detail Penjualan.

## 10. Alur Proses Sistem

Alur proses pada sistem secara sederhana yaitu:

**Pelanggan datang → dilayani Pegawai → transaksi dicatat → barang yang dibeli dicatat pada Detail Penjualan → data barang digunakan → total pembayaran dicatat.**

Dengan cara tersebut, satu nomor faktur dapat memiliki beberapa barang yang berbeda.

## 11. Persyaratan Non-Fungsional

Beberapa hal yang diharapkan dari sistem:

* Data tersimpan dengan rapi.
* Hubungan antar tabel jelas.
* Data dapat digunakan untuk membuat laporan penjualan.
* Sistem dapat digunakan untuk mengelola data transaksi dengan lebih mudah.
* Data yang disimpan harus sesuai dengan struktur tabel yang sudah dibuat.

## 12. Technical Design

Perancangan sistem dibuat berdasarkan model relasional, diagram skema, dan ERD yang sudah dibuat sebelumnya.

ERD dapat dilihat melalui link berikut:

[ERD](https://drive.google.com/file/d/15H7NKOZa1VQpePpmL8VbLYjteFEjeh94/view?usp=sharing)

Struktur utama sistem terdiri dari tabel Barang, Pelanggan, Pegawai, Penjualan, dan Detail Penjualan. Tabel-tabel tersebut memiliki hubungan melalui Primary Key dan Foreign Key.

## 13. Jadwal dan Timeline

| Tahap | Kegiatan                             |
| ----- | ------------------------------------ |
| 1     | Menentukan kebutuhan sistem          |
| 2     | Menentukan tabel dan atribut         |
| 3     | Membuat model relasional             |
| 4     | Membuat diagram skema dan ERD        |
| 5     | Membuat PRD                          |
| 6     | Menyelesaikan dan mengumpulkan tugas |

## 14. Risiko dan Asumsi

### Risiko

* Kesalahan dalam menentukan relasi antar tabel.
* Kesalahan dalam menentukan Primary Key dan Foreign Key.
* Data yang dimasukkan tidak sesuai dengan struktur tabel.

### Asumsi

* Data yang digunakan sesuai dengan kebutuhan toko.
* Setiap transaksi memiliki nomor faktur.
* Satu transaksi dapat memiliki lebih dari satu barang.
* Data pelanggan dan pegawai sudah tersedia saat transaksi dilakukan.

## 15. Kriteria Keberhasilan

Sistem dianggap sesuai apabila:

* Semua tabel yang dibutuhkan sudah dibuat.
* Primary Key dan Foreign Key sudah ditentukan.
* Relasi antar tabel sesuai dengan kebutuhan sistem.
* Data transaksi dapat disimpan.
* Detail barang dalam transaksi dapat dicatat.
* Struktur database sesuai dengan model relasional dan ERD.

## 16. Persetujuan Pemangku Kepentingan

PRD ini dibuat sebagai rancangan kebutuhan untuk sistem basis data toko penjualan retail dan digunakan sebagai dasar dalam proses perancangan database.

## 17. Kesimpulan

Sistem basis data toko penjualan retail dibuat untuk membantu mengelola data barang, pelanggan, pegawai, supplier, dan transaksi penjualan. Dengan adanya hubungan antar tabel, data transaksi dapat disimpan dengan lebih terstruktur dan dapat digunakan untuk kebutuhan pengelolaan serta laporan penjualan.
