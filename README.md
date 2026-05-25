# Praktikum Machine Learning - K-Means Clustering

## Deskripsi Singkat
Repositori ini berisi dokumentasi praktikum Machine Learning mengenai implementasi algoritma **K-Means Clustering** menggunakan Python. Model ini digunakan untuk mengelompokkan data lintasan (`go_track_tracks.csv`) berdasarkan fitur kecepatan (`speed`) dan jenis kendaraan.

## Tools & Library
* **Python 3**
* **Pandas & NumPy** (Manipulasi data)
* **Matplotlib & Seaborn** (Visualisasi data)
* **Scikit-Learn** (Pemodelan K-Means, MinMaxScaler, dan metrik evaluasi)

## Alur Kerja Program
1. **Import Dataset:** Membaca data `go_track_tracks.csv` menggunakan Pandas.
2. **Data Cleaning:** Menghapus kolom `linha` karena banyak data yang kosong (NaN).
3. **Seleksi Fitur:** Memilih kolom `id_android` dan `speed` untuk diklusterkan.
4. **Data Scaling:** Mengubah skala data menggunakan `MinMaxScaler` agar tidak ada fitur yang mendominasi jarak (karena perbedaan satuan).
5. **Pemodelan K-Means:** Menjalankan algoritma K-Means dengan target `n_clusters=3`.
6. **Evaluasi:** Mengukur kualitas kluster menggunakan nilai *Silhouette Score*.
7. **Visualisasi:** Menampilkan hasil kluster dan titik pusatnya (*centroid*) ke dalam grafik *scatter plot*.

## Hasil Evaluasi
* Model berhasil membagi data ke dalam 3 kelompok utama.
* **Silhouette Score:** -0.098. Nilai yang minus ini menunjukkan bahwa batas antar kluster (berdasarkan fitur yang dipilih) masih cenderung tumpang tindih (*overlapping*), sehingga pengelompokan yang dihasilkan belum sepenuhnya optimal.

> **Note:** Pada grafik plot visualisasi, sumbu X mewakili *ID Android* dan sumbu Y mewakili *Speed*.