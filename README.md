# UTS DATA WRANGLING

## Dari Data Mentah ke Dataset Siap Analisis: Harga Pangan Jawa Timur 2024

### 1. Identitas Proyek

- **Nama:** Adel Phonsa Jeanne Valencya Sihombing
- **NIM:** 25031554073
- **Kelas:** 2025G
- **Mata Kuliah:** Data Wrangling
- **Tahun Data yang Digunakan:** 2024
- **Wilayah Analisis:** Jawa Timur

### 2. Deskripsi Proyek

Proyek ini bertujuan untuk melakukan proses data wrangling terhadap data harga pangan, cuaca, dan karakteristik wilayah di Provinsi Jawa Timur. Data mentah yang diperoleh dari beberapa sumber diolah melalui proses pemeriksaan, pembersihan, transformasi, dan penggabungan agar dapat digunakan untuk analisis.

Analisis difokuskan pada lima komoditas Paket C, yaitu beras medium I, cabai rawit merah, bawang putih, gula pasir lokal, dan daging ayam ras.

Pertanyaan utama yang dianalisis adalah wilayah kabupaten/kota yang mengalami kenaikan harga terbesar dari Januari hingga Desember 2024 serta gambaran perubahan harga berdasarkan karakteristik wilayah.

### 3. Sumber Data

Data yang digunakan berasal dari tiga sumber:

1. **PIHPS (Pusat Informasi Harga Pangan Strategis):** Data harga pangan harian pasar tradisional di Jawa Timur selama tahun 2024.
2. **NOAA (National Oceanic and Atmospheric Administration):** Data pengamatan cuaca harian dari empat stasiun pengamatan di Jawa Timur.
3. **Kepmendagri:** Data kode wilayah, luas wilayah, jumlah penduduk, kecamatan, kelurahan, dan desa di Jawa Timur.

### 4. Tahapan Pengolahan Data

Pengolahan data dilakukan melalui tujuh tahapan sebagai berikut:

1. **Plan Wrangling:** Menentukan tujuan, ruang lingkup, kebutuhan data, dan rencana pengolahan data.
2. **Discovery:** Memeriksa dan memahami struktur, isi, serta kondisi awal dataset dari setiap sumber.
3. **Read and Structuring:** Membaca dataset, memilih data yang relevan, dan mengubah format data harga dari wide menjadi long.
4. **Enriching Data:** Menggabungkan data harga pangan dengan data cuaca dan referensi karakteristik wilayah.
5. **Profiling and Cleaning Data:** Memeriksa kualitas data, menangani nilai kosong, memeriksa outlier, dan melakukan transformasi serta normalisasi data.
6. **Exploratory Data Analysis (EDA):** Melakukan eksplorasi dan analisis data menggunakan agregasi, groupby, pivot table, serta perhitungan perubahan harga.
7. **Publishing:** Menyimpan dataset hasil pengolahan dan menyajikan hasil analisis dalam bentuk tabel, visualisasi, laporan, serta kamus data.

### 5. Struktur Folder

```text
04_25031554073_Adel Phonsa JeanneV S_UTS_DW/
│
├── data_processed/
│   ├── dataset_integrasi_jatim_2024.csv
│   └── dataset_terintegrasi_mingguan.csv
│
├── data_raw/
│   ├── 1_harga_pasar_tradisional/
│   ├── 2_cuaca_stasiun/
│   ├── 3_wilayah/
│   ├── petunjuk.md
│   └── sumber_data.md
│
├── notebook/
│   └── UTS_Data_Wrangling.ipynb
│
├── diagram_wrangling.png
├── kamus_data.md
└── README.md
```

### 6. Hasil Pengolahan

Hasil pengolahan menghasilkan dataset harga pangan yang telah melalui proses integrasi serta dataset harga pangan mingguan yang telah digabungkan dengan data cuaca dan karakteristik wilayah. Selain itu, dilakukan analisis perubahan harga dari Januari hingga Desember 2024 pada sembilan kabupaten/kota yang tersedia dalam data PIHPS.

Hasil analisis menunjukkan bahwa kenaikan persentase terbesar untuk satu komoditas terjadi pada bawang putih di Kabupaten Sumenep sebesar **14,74%**. Sementara itu, Kota Blitar memiliki rata-rata persentase perubahan harga tertinggi jika dilihat dari kelima komoditas, yaitu sebesar **5,16%**.

### 7. Keterbatasan Data

Beberapa keterbatasan dalam proyek ini adalah:

1. Data harga PIHPS hanya mencakup sembilan dari 38 kabupaten/kota di Jawa Timur.
2. Data cuaca hanya tersedia untuk sebagian wilayah, sehingga tidak semua data harga memiliki pasangan data cuaca.
3. Terdapat nilai kosong pada data harga dan cuaca. Nilai kosong pada harga ditangani menggunakan interpolasi linear, sedangkan nilai kosong pada data cuaca dipertahankan.
4. Data outlier tetap dipertahankan karena belum ditemukan bukti bahwa nilai tersebut merupakan kesalahan pencatatan.
5. Perbandingan karakteristik wilayah, khususnya jumlah desa dan kelurahan, memiliki keterbatasan karena perbedaan struktur administrasi wilayah.

### 8. Cara Menjalankan Notebook

1. Buka folder utama proyek menggunakan Visual Studio Code.
2. Pastikan Python dan ekstensi Python serta Jupyter pada Visual Studio Code sudah tersedia.
3. Buka folder `notebook`.
4. Jalankan file `UTS_Data_Wrangling.ipynb`.
5. Pilih kernel Python yang sesuai dengan lingkungan kerja.
6. Pastikan seluruh folder dan file dataset tetap berada pada struktur folder proyek seperti yang tercantum di atas.
7. Jalankan setiap cell secara berurutan dari awal hingga akhir atau gunakan fitur **Run All** untuk menjalankan seluruh cell secara otomatis sesuai urutannya.