# Decision Tree untuk Kelayakan Panen Tanaman

Proyek ini mengimplementasikan algoritma Decision Tree dengan metode ID3 (Iterative Dichotomiser 3) untuk menentukan kelayakan panen tanaman berdasarkan berbagai parameter pertanian.

## 👥 Tim Pengembang

- Muhammad Wildan Hatami
- Imam Ar-Roghib Al-Ashfahani
- M. Reyhan Hermawan
- Muhammad Ghanim Mukafih
- M. Althaf Faiz Rafianto

## 📋 Deskripsi Proyek

Sistem ini menggunakan algoritma Decision Tree ID3 untuk mengklasifikasikan apakah tanaman siap dipanen atau belum berdasarkan fitur-fitur berikut:

- **plant_age_days**: Umur tanaman dalam hari
- **height_cm**: Tinggi tanaman dalam sentimeter
- **leaf_color**: Warna daun (dark_green, light_green, green, yellow)
- **rainfall**: Tingkat curah hujan (low, medium, high)
- **soil_moisture**: Kelembaban tanah (low, medium, high)
- **ready**: Status kelayakan panen (yes/no) - target klasifikasi

## 🎯 Fitur Utama

- **Implementasi ID3 dari Nol**: Algoritma Decision Tree dibangun dari dasar tanpa menggunakan library machine learning tingkat tinggi
- **Perhitungan Entropy dan Information Gain**: Menggunakan konsep teori informasi untuk memilih atribut terbaik
- **Visualisasi Pohon Keputusan**: Menampilkan struktur pohon keputusan secara visual menggunakan NetworkX dan Matplotlib
- **Evaluasi Model**: Mengukur akurasi model pada data training dan testing
- **Dataset Sintetis**: Menggunakan dataset sintetis dengan 500 baris data

## 📊 Dataset

Dataset yang digunakan adalah **dataset sintetis** yang dirancang khusus untuk proyek ini. Dataset berisi 500 baris data dengan 6 kolom (5 fitur + 1 target).

File dataset: `dataset_500_baris(1).csv`

### Struktur Data:
```
plant_age_days,height_cm,leaf_color,rainfall,soil_moisture,ready
64,58,dark_green,medium,high,no
76,113,yellow,low,medium,yes
85,50,light_green,medium,high,no
...
```

## 🛠️ Teknologi yang Digunakan

- **Python 3.x**
- **Pandas**: Manipulasi dan analisis data
- **NumPy**: Komputasi numerik
- **Matplotlib**: Visualisasi data
- **NetworkX**: Visualisasi struktur pohon keputusan
- **Scikit-learn**: Evaluasi metrik (accuracy_score)

> **⚠️ Disclaimer**: Library yang digunakan dalam proyek ini hanya untuk keperluan visualisasi. Algoritma Decision Tree ID3 diimplementasikan dari awal tanpa menggunakan library machine learning tingkat tinggi.

## 📦 Instalasi

1. Clone repository ini:
```bash
git clone https://github.com/bianglalametro/decision-tree-crop-yield.git
cd decision-tree-crop-yield
```

2. Install dependensi yang diperlukan:
```bash
pip install pandas numpy matplotlib networkx scikit-learn
```

## 🚀 Cara Penggunaan

1. Buka notebook `Decision_Tree_kelayakan_panen.ipynb` menggunakan Jupyter Notebook atau Google Colab

2. Jalankan sel-sel kode secara berurutan untuk:
   - Memuat dan mengeksplorasi dataset
   - Melatih model Decision Tree dengan algoritma ID3
   - Memvisualisasikan pohon keputusan
   - Mengevaluasi akurasi model

3. Alternatif: Buka langsung di Google Colab dengan mengklik badge di bagian atas notebook

## 📈 Cara Kerja Algoritma ID3

1. **Hitung Entropy Dataset**: Mengukur tingkat ketidakpastian dalam dataset
2. **Hitung Information Gain**: Untuk setiap atribut, hitung seberapa banyak informasi yang diperoleh jika kita membagi data berdasarkan atribut tersebut
3. **Pilih Atribut Terbaik**: Pilih atribut dengan Information Gain tertinggi sebagai node
4. **Bagi Dataset**: Bagi dataset berdasarkan nilai atribut yang dipilih
5. **Rekursi**: Ulangi proses untuk setiap subset hingga:
   - Semua data dalam subset memiliki label yang sama, atau
   - Tidak ada lagi atribut yang dapat digunakan untuk membagi data

## 📝 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

## 🙏 Acknowledgments

Proyek ini dibuat sebagai bagian dari pembelajaran AI - Project Based Learning (PBL).
