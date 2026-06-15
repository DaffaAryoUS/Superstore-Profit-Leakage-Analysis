# Overcoming Profit Leakage from Aggressive Discounting Strategy 🛒📉

## 📌 Project Overview
Proyek ini bertujuan untuk mendiagnosis fenomena **growth trap** pada Super Store, di mana peningkatan volume penjualan tidak berbanding lurus dengan keuntungan. Analisis difokuskan secara mendalam pada sub-kategori **Machines** yang menjadi titik kebocoran profit (*profit leakage*) terbesar perusahaan akibat strategi pemberian diskon yang agresif dan tidak tepat sasaran.

---

## ⚠️ Problem Statement
Berdasarkan riset dari *McKinsey & Company*, kesalahan dalam penentuan harga dan pemberian diskon yang tidak tepat sasaran dapat menurunkan profitabilitas perusahaan hingga 20-30%, meskipun angka penjualan terlihat meningkat. Di tengah pasar yang kompetitif, Super Store mengalami penurunan margin keuntungan yang signifikan akibat penerapan diskon masif tanpa dasar struktur profitabilitas yang tepat.

---

## 📂 About Data
* **Data File:** Sample-Superstore
* **Format File:** Comma-Separated Values (CSV)
* **Baris:** 9,994
* **Kolom:** 21
* **Tahun Publikasi (Last Update):** 2022
* **Sumber:** [kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data)

---
## 🛠️ Tech Stack & Tools
* **Language:** Python
* **Libraries:** Pandas (Data Preprocessing & Feature Engineering)
* **Environment:** Jupyter Notebook via Visual Studio Code
* **Visualization:** Tableau Dashboard

---

## 💡 Key Insights (Machines Sub-Category)

### 1. Paradoks Penjualan Tinggi vs Profit Rendah
* Sub-kategori **Machines** mencatatkan total penjualan (*Sales*) yang kuat sebesar **$189.24K** dari 112 order.
* Volume ini jauh melampaui sub-kategori *Copiers* ($149.53K dengan 68 order).
* Namun, profit bersih *Machines* hancur di angka **$3.38K**, sementara *Copiers* berhasil meraup profit tertinggi sebesar $55.62K.

### 2. Kebocoran Transaksi yang Masif
* Ditemukan bahwa **47,34% dari total transaksi** pada sub-kategori *Machines* berujung mengalami kerugian.
* Akumulasi nilai kerugian (*Total Loss*) dari transaksi minus tersebut mencapai **$30,118.67**.

### 3. Erosi Margin Akibat Diskon Ekstrem (Korelasi Negatif)
* Hasil analisis pola hubungan menunjukkan bahwa peningkatan persentase diskon berkorelasi langsung dengan penurunan tajam *profit margin*.
* Mayoritas kerugian didorong oleh pemberian diskon agresif di rentang **40% hingga 70%**.
* **Studi Kasus:** Produk *Cubify CubeX 3D Printer* di *State* Ohio yang diberi diskon 70% memicu margin kerugian hingga **-147%** atau setara dengan minus **$9,239.97** hanya dari satu transaksi.

### 4. Red Flag Geografis: State Ohio
* Wilayah **Ohio** menjadi episentrum kerugian bagi sub-kategori *Machines*.
* Terdapat 8 pelanggan di Ohio yang seluruh transaksinya merugi dengan total *loss* mencapai **-$11,770.94** dan rata-rata *profit margin* **-102.50%**.
* Padahal, Ohio masuk dalam *Top 5 AOV (Average Order Value)* tertinggi sebesar $1,12K.

---

## 🚀 Actionable Recommendations

1. **Penerapan Batas Maksimal Diskon (*Discount Capping*):** Mengunci sistem penjualan agar diskon untuk sub-kategori *Machines* tidak melebihi angka 20% dan menghentikan total promo diskon di atas 40%.
2. **Audit Khusus untuk State Ohio:** Mengevaluasi kebijakan *pricing* atau kontrak dengan pelanggan besar di Ohio. Mengubah strategi promo dari "potongan harga langsung" menjadi penawaran nilai tambah (*value-added*) seperti perpanjangan garansi atau paket perawatan *hardware*.
3. **Restrukturisasi Katalog Produk Sensitif:** Melakukan peninjauan kembali terhadap produk dengan sensitivitas diskon tinggi (seperti *Cubify CubeX*, *Cisco*, *Epson*). Jika biaya modal (*unit cost*) terlalu tinggi, pertimbangkan untuk membatasi kuota pemesanan produk tersebut.
