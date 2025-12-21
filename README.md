# Data_Wrangling
Ini adalah Projek data wrangling kami dari anak UNESA dan UNJ

## 💾 Penjelasan Dataset

Proyek ini berfokus pada analisis **Dinamika Harga Padi dan Beras** serta hubungannya dengan **Volume Produksi**. Dataset utama (`data_cleaned.csv`) mencakup variabel kunci seperti Tahun, Produksi (ton), Kategori Mutu Beras, Harga Beras, dan Harga Gabah.

Folder `data_publishing` berisi berbagai format data hasil transformasi untuk memudahkan analisis spesifik:

### 1. Data Utama
* **`data_cleaned.csv`**: Dataset master yang bersih.
    * *Kolom*: `Tahun`, `Produksi (ton)`, `Kategori` (Mutu Beras: Bawah, Medium, Super), `Harga Beras (Rp/Kg)`, `Harga Gabah (Rp/Kg)`.
    * *Fungsi*: Sumber kebenaran tunggal (Single Source of Truth) untuk seluruh analisis.

### 2. Analisis Margin Keuntungan (Beras vs Gabah)
Analisis ini menghitung selisih antara harga jual (Beras) dan harga bahan baku (Gabah).
* **`dataset_margin_detail.csv`**: Data lengkap perhitungan margin untuk setiap baris data.
* **`pivot_margin_absolut.csv`**: Tabel pivot yang menunjukkan nominal keuntungan (Rupiah/Kg) per Kategori dan Tahun.
    * *Rumus*: `Harga Beras - Harga Gabah`.
* **`pivot_margin_persentase.csv`**: Tabel pivot persentase keuntungan relatif terhadap harga gabah.
    * *Rumus*: `(Margin / Harga Gabah) * 100`.

### 3. Transformasi Struktur Data
* **`data_long_format.csv`**: Format data memanjang (*Unpivoted*). Cocok untuk visualisasi time-series di library seperti Altair/Seaborn.
* **`data_wide_format.csv`**: Format data melebar. Biasanya memisahkan metrik (Produksi, Harga) atau Kategori menjadi kolom tersendiri untuk perbandingan berdampingan.
* **`pivot_harga_beras.csv`**: Matriks harga beras yang disederhanakan (Baris: Tahun, Kolom: Kategori) untuk melihat tren harga antar kualitas dengan cepat.

### 4. Analisis Statistik & Agregasi
* **`dataset_yearly_aggregate.csv` / `yearly_aggregation.csv`**: Rata-rata harga dan total produksi yang dikelompokkan per Tahun (mengabaikan perbedaan kategori mutu).
* **`dataset_category_comparison.csv`**: Ringkasan performa (Rata-rata Harga/Margin) dikelompokkan per `Kategori` mutu beras (Bawah vs Medium vs Super).
* **`correlation_dataset.csv`**: Matriks korelasi untuk menguji hipotesis.
    * *Contoh*: Apakah `Produksi (ton)` yang tinggi berkorelasi negatif dengan `Harga Beras`? (Hukum Permintaan/Penawaran).
* **`sensitivity_analysis.csv`**: Analisis simulasi sensitivitas harga/margin terhadap perubahan variabel input tertentu.
* **`summary_statistics_univariate.csv`**: Statistik deskriptif dasar (Mean, Median, Min, Max) untuk variabel numerik (`Harga`, `Produksi`).
