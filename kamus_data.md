# KAMUS DATA

Kamus data ini menjelaskan nama variabel, tipe data, dan keterangan dari dua dataset hasil pengolahan yang terdapat dalam folder `data_processed`.

## 1. Dataset Integrasi Harian

**Nama file:** `dataset_integrasi_jatim_2024.csv`  
**Ukuran dataset:** 11.790 baris × 17 kolom.

| No. | Nama Variabel | Tipe Data | Keterangan |
|---:|---|---|---|
| 1 | `kode` | Float64 | Kode administratif kabupaten/kota di Jawa Timur. |
| 2 | `wilayah` | String | Nama wilayah kabupaten/kota. |
| 3 | `nama` | String | Nama lengkap kabupaten/kota. |
| 4 | `name` | String | Nama komoditas pangan. |
| 5 | `tanggal` | String | Tanggal pencatatan harga pangan. |
| 6 | `harga` | Float64 | Harga komoditas pangan pada tanggal tertentu. |
| 7 | `luas` | Float64 | Luas wilayah kabupaten/kota dalam km². |
| 8 | `pria` | Int64 | Jumlah penduduk laki-laki. |
| 9 | `wanita` | Int64 | Jumlah penduduk perempuan. |
| 10 | `total` | Int64 | Jumlah keseluruhan penduduk. |
| 11 | `kepadatan_penduduk` | Float64 | Kepadatan penduduk per km². |
| 12 | `jumlah_kecamatan` | Float64 | Jumlah kecamatan pada setiap kabupaten/kota. |
| 13 | `jumlah_desa_kelurahan` | Float64 | Jumlah desa dan kelurahan pada setiap kabupaten/kota. |
| 14 | `suhu_rata_rata` | Float64 | Rata-rata suhu udara berdasarkan data cuaca. |
| 15 | `curah_hujan` | Float64 | Curah hujan berdasarkan data cuaca. |
| 16 | `kecepatan_angin` | Float64 | Kecepatan angin berdasarkan data cuaca. |
| 17 | `jumlah_stasiun` | Float64 | Jumlah stasiun cuaca yang terhubung dengan wilayah dalam proses penggabungan data. |

## 2. Dataset Integrasi Mingguan

**Nama file:** `dataset_terintegrasi_mingguan.csv`  
**Ukuran dataset:** 2.385 baris × 21 kolom.

| No. | Nama Variabel | Tipe Data | Keterangan |
|---:|---|---|---|
| 1 | `kode` | Float64 | Kode administratif kabupaten/kota di Jawa Timur. |
| 2 | `wilayah` | String | Nama wilayah kabupaten/kota. |
| 3 | `komoditas` | String | Nama komoditas pangan. |
| 4 | `minggu` | String | Tanggal awal periode pengelompokan mingguan. |
| 5 | `harga_rata_rata` | Float64 | Rata-rata harga komoditas pangan dalam satu periode minggu. |
| 6 | `TEMP_C` | Float64 | Rata-rata suhu udara dalam derajat Celsius. |
| 7 | `DEWP_C` | Float64 | Rata-rata suhu titik embun dalam derajat Celsius. |
| 8 | `MAX_C` | Float64 | Suhu udara maksimum dalam derajat Celsius. |
| 9 | `MIN_C` | Float64 | Suhu udara minimum dalam derajat Celsius. |
| 10 | `SLP` | Float64 | Tekanan udara pada permukaan laut berdasarkan data cuaca. |
| 11 | `STP` | Float64 | Tekanan udara pada stasiun pengamatan berdasarkan data cuaca. |
| 12 | `VISIB` | Float64 | Jarak pandang berdasarkan data cuaca. |
| 13 | `WDSP` | Float64 | Kecepatan angin berdasarkan data cuaca. |
| 14 | `PRCP_mm` | Float64 | Curah hujan dalam milimeter. |
| 15 | `nama_resmi` | String | Nama resmi kabupaten/kota berdasarkan data administrasi wilayah. |
| 16 | `luas` | Float64 | Luas wilayah kabupaten/kota dalam km². |
| 17 | `total` | Int64 | Jumlah keseluruhan penduduk. |
| 18 | `kepadatan_penduduk` | Float64 | Kepadatan penduduk per km². |
| 19 | `jumlah_kecamatan` | Int64 | Jumlah kecamatan pada setiap kabupaten/kota. |
| 20 | `jumlah_kelurahan` | Int64 | Jumlah kelurahan pada setiap kabupaten/kota. |
| 21 | `jumlah_desa` | Float64 | Jumlah desa pada setiap kabupaten/kota. |

## Catatan

1. Tipe data pada tabel mengikuti tipe data yang terbaca ketika file CSV dimuat menggunakan Pandas.
2. Nilai kosong (*missing values*) dapat ditemukan pada beberapa variabel, terutama variabel cuaca, apabila data pendukung tidak tersedia.
3. Dataset integrasi harian menyimpan data harga berdasarkan tanggal, sedangkan dataset integrasi mingguan menyimpan harga rata-rata berdasarkan periode minggu.
4. Kedua dataset memuat informasi harga pangan dan karakteristik wilayah. Dataset mingguan juga memuat variabel cuaca yang digunakan untuk mendukung analisis kondisi wilayah di Jawa Timur.