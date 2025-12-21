# Data_Wrangling
Ini adalah Projek data wrangling kami dari anak UNESA dan UNJ

## 💾 Penjelasan Dataset

Proyek ini menghasilkan beberapa dataset olahan yang tersimpan dalam folder `data_publishing` untuk keperluan analisis lebih lanjut dan visualisasi. Berikut adalah rincian isi dari setiap file:

### 1. Data Utama
* **`data_cleaned.csv`**: Dataset master yang telah melalui proses *cleaning* (pembersihan *missing values*, duplikat, dan penyesuaian tipe data). Dataset ini menjadi sumber utama untuk semua analisis selanjutnya.

### 2. Transformasi Data
* **`data_long_format.csv`**: Versi dataset dalam format *long* (memanjang ke bawah), cocok untuk visualisasi deret waktu atau analisis menggunakan library tertentu (seperti Altair/Seaborn).
* **`data_wide_format.csv`**: Versi dataset dalam format *wide* (melebar ke samping), di mana setiap kategori/variabel menjadi kolom tersendiri.

### 3. Analisis Harga & Margin (Beras vs Gabah)
* **`pivot_harga_beras.csv`**: Tabel pivot yang memfokuskan pada pergerakan harga beras (rata-rata per periode/lokasi).
* **`dataset_margin_detail.csv`**: Data rinci mengenai selisih (margin) antara harga pembelian (gabah) dan harga penjualan (beras).
* **`pivot_margin_absolut.csv`**: Pivot table yang menunjukkan nilai margin keuntungan secara nominal (Rupiah).
* **`pivot_margin_persentase.csv`**: Pivot table yang menunjukkan persentase margin keuntungan relatif terhadap harga modal.

### 4. Analisis Statistik & Agregasi
* **`dataset_yearly_aggregate.csv` / `yearly_aggregation.csv`**: Ringkasan data yang dikelompokkan per tahun untuk melihat tren jangka panjang.
* **`dataset_category_comparison.csv`**: Data komparasi antar kategori (misalnya perbandingan antar kualitas beras atau antar provinsi).
* **`summary_statistics_univariate.csv`**: Statistik deskriptif (Mean, Median, Std Dev) untuk setiap variabel tunggal.
* **`correlation_dataset.csv`**: Matriks korelasi untuk melihat hubungan antar variabel (misal: apakah kenaikan harga gabah berkorelasi kuat dengan harga beras?).
* **`sensitivity_analysis.csv`**: Hasil analisis sensitivitas untuk melihat seberapa besar perubahan satu variabel mempengaruhi variabel hasil (misal: dampak kenaikan biaya produksi terhadap harga jual).
