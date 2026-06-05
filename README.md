# 🧠 Proyek Analisis Data Tabungan Progresif

Proyek Analisis Data Tabungan Progresif adalah proyek analisis dan visualisasi data komprehensif yang bertujuan untuk memberikan wawasan tentang perilaku menabung pengguna, pencapaian target, dan tren transaksi. Proyek ini memanfaatkan pembersihan data, analisis data eksploratif (EDA), dan teknik visualisasi untuk mengungkap pola menabung, interval antar setoran, dan wawasan tabungan berbasis kategori.

Proyek ini berfokus pada transformasi data transaksi mentah yang kotor menjadi informasi yang bermakna melalui pembersihan data, preprocessing, rekayasa fitur, dan visualisasi menggunakan pustaka Python yang populer.

## 🚀 Apa yang Dilakukan Proyek Ini?

* Pembersihan dan prapemrosesan data (membersihkan string numerik, simbol mata uang, dan menstandardisasi tanggal menggunakan Pandas dan NumPy)
* Penanganan outlier dan imputasi nilai kosong menggunakan statistik global pada target nominal
* Analisis Data Eksploratif (EDA) pada frekuensi menabung dan metrik pencapaian target
* Visualisasi data (distribusi, garis tren, dan tingkat penyelesaian target menggunakan Matplotlib dan Seaborn)
* Transformasi data dan rekayasa fitur (menghitung interval tanggal antar setoran, total akumulasi, dan persentase kemajuan)
* Analisis mendalam tentang tujuan tabungan yang belum selesai dan interval transaksi
* Analisis tren berdasarkan tanggal transaksi, kategori tabungan, dan tujuan target

---

## 📊 Tinjauan Dataset

Proyek ini menggunakan dataset transaksi tabungan progresif yang telah dibersihkan yang dikumpulkan antara Januari 2020 dan Januari 2026.

### Statistik Dataset

| Metrik         | Nilai                       |
| -------------- | --------------------------- |
| Total Catatan  | 32.759                      |
| Total Fitur    | 11                          |
| Rentang Tanggal| Januari 2020 – Januari 2026 |
| Tujuan Tabungan Unik | 2.162                 |
| Format Berkas  | CSV                         |

### Fitur Dataset

| Kolom              | Deskripsi                                   |
| ------------------- | --------------------------------------------- |
| `id_tabungan`         | ID unik untuk setiap tujuan tabungan |
| `counter_tabungan`    | Indeks urutan setoran untuk tujuan tabungan tertentu |
| `tanggal_nabung`      | Tanggal transaksi setoran dilakukan |
| `nama_goal`           | Kategori atau nama tujuan menabung |
| `target_nominal`      | Total nominal target yang ingin ditabung |
| `nominal_nabung`      | Nominal setoran tabungan pada transaksi saat ini |
| `total_terkumpul`     | Akumulasi tabungan terkumpul hingga transaksi saat ini |
| `sisa_target`         | Sisa target nominal yang belum terkumpul |
| `status`              | Status pencapaian tabungan (Selesai/Belum Selesai) |
| `jarak_hari_nabung`   | Jumlah selisih hari sejak setoran terakhir |
| `persentase_terkumpul`| Persentase kemajuan tabungan terhadap target nominal |

### Kategori Tujuan Menabung

Dataset ini mencakup beberapa kategori tujuan menabung seperti:

* Modal Nikah/Tunangan
* Tanpa Nama (Tujuan tanpa nama kategori)
* Beli Ipad/Tablet Nugas
* Beli Motor Bekas
* Liburan Ke Bali/Jogja
* Dana Darurat
* Rakit PC Gaming
* Bayar Kosan Tahunan
* Beli Kamera Analog/Mirrorless
* Beli Emas Antam
* Modal Usaha Thrift/F&B
* Dan banyak tujuan personal serta gaya hidup lainnya...

### Sampel Data

| id_tabungan | counter_tabungan | tanggal_nabung | nama_goal | target_nominal | nominal_nabung | total_terkumpul | sisa_target | status | jarak_hari_nabung | persentase_terkumpul |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| TAB-0001 | 1 | 2021-06-12 | Dana Darurat | 9720000 | 1134942 | 1134942 | 8585058 | Belum Selesai | 0 | 11.68 |
| TAB-0001 | 2 | 2021-06-26 | Dana Darurat | 9720000 | 948640 | 2083582 | 7636418 | Belum Selesai | 14 | 21.44 |
| TAB-0001 | 3 | 2021-07-15 | Dana Darurat | 9720000 | 1056415 | 3139997 | 6580003 | Belum Selesai | 19 | 32.3 |

### Tujuan Dataset

Dataset yang telah dibersihkan ini ditujukan untuk:

* Analisis konsistensi dan perilaku menabung
* Pelacakan kemajuan dan estimasi waktu penyelesaian target
* Pemprofilan interval penyetoran (studi tentang `jarak_hari_nabung`)
* Analisis tingkat keberhasilan tujuan menabung berdasarkan kategori
* Pemodelan prediktif untuk keterlambatan atau kelalaian pola menabung
* Visualisasi data dan pelaporan dasbor finansial

---

## 🛠️ Pustaka Teknologi

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Jupyter Notebook

---

# 📦 Instalasi

Direkomendasikan untuk menggunakan lingkungan virtual (virtual environment) sebelum menjalankan proyek agar dependensi tetap terisolasi.

## 1. Klon Repositori

```bash
git clone https://github.com/Capstone-Catatanku/Data-Science-Tabungan.git
cd Data-Science-Tabungan
```

## 2. Buat Lingkungan Virtual

### Windows

```bash
python -m venv venv
```

### Linux/macOS

```bash
python3 -m venv venv
```

## 3. Aktifkan Lingkungan Virtual

### Windows (Command Prompt)

```bash
venv\Scripts\activate
```

### Windows (PowerShell)

```bash
venv\Scripts\Activate.ps1
```

### Linux/macOS

```bash
source venv/bin/activate
```

## 4. Instal Pustaka yang Diperlukan

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

---

# 💻 Penggunaan

## 1. Jalankan Jupyter Notebook

```bash
jupyter notebook
```

## 2. Buka Notebook

Jalankan notebook preprocessing untuk membersihkan data mentah:
```text
PreProcessing.ipynb
```

Kemudian buka notebook analisis untuk melakukan EDA dan visualisasi:
```text
analysis.ipynb
```

## 3. Jalankan Analisis

Eksekusi semua sel notebook untuk melakukan:
* Pembersihan dan normalisasi data
* Penanganan nilai kosong dan outlier target nominal
* Analisis statistik pada nominal target dan frekuensi setoran
* Analisis Data Eksploratif (EDA) pada tingkat penyelesaian target
* Pembuatan wawasan (insight) dan visualisasi pola menabung

---

## 📂 Struktur Proyek

```text
.
├── Clean-data/
│   └── Data_Progressive_Clean.csv
├── Raw-data/
│   └── Sintesis_Progressive_.csv
├── Data_Dictionary_tabungan.xlsx
├── PreProcessing.ipynb
├── analysis.ipynb
└── README.md
```

---

## 📈 Tujuan Analisis

Proyek ini bertujuan untuk menjawab beberapa pertanyaan seperti:
- Dari 10 `nama_goal` dengan frekuensi tertinggi, mana yang memiliki rata-rata persentase pencapaian terendah untuk tabungan 'Belum Selesai' yang sudah berjalan lebih dari 180 hari? (Jawaban: Dana Darurat, dengan rata-rata persentase pencapaian hanya 55.04%)
- Bagaimana pola dan statistik jarak hari menabung (`jarak_hari_nabung`) bagi pengguna yang berhasil menyelesaikan tabungannya (`status = Selesai`)? (Jawaban: Rata-rata 21.6 hari, median 19.0 hari, standar deviasi 19.9 hari)
- Bagaimana karakteristik deskriptif target nominal dan jumlah setoran pengguna dalam mendeteksi outliers? (Jawaban: Target nominal median sebesar Rp 7.030.000, sedangkan rata-ratanya Rp 16.832.386, dan median setoran nominal menabung sebesar Rp 163.668)

---

## 💖 Penghargaan

Terima kasih yang sebesar-besarnya kepada semua pihak yang telah berkontribusi dalam proyek ini. Dukungan, umpan balik, dan kontribusi Anda telah membantu meningkatkan kualitas dan dampak dari proyek ini.

Terima kasih khusus kepada semua anggota tim yang terlibat dalam pengumpulan data, prapemrosesan, analisis, dan pengembangan proyek.
