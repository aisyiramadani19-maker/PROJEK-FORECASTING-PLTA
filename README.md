# PROJEK-FORECASTING-PLTA

README
PROGRAM FORECASTING POTENSI PLTA


Nama Program   : Aplikasi Forecasting Potensi PLTA
Bahasa         : Python
Framework      : Streamlit
Bidang Kajian  : Energi Terbarukan (PLTA)
Mata Kuliah    : Algoritma Data dan Pemrograman

--------------------------------------------------
1. DESKRIPSI PROGRAM
--------------------------------------------------

Program ini merupakan aplikasi berbasis Python yang digunakan
untuk melakukan forecasting potensi Pembangkit Listrik Tenaga Air (PLTA).
Forecasting dilakukan dengan mempertimbangkan debit sungai yang dipengaruhi
oleh faktor iklim, yaitu:

- Curah hujan
- Suhu udara
- Kelembaban udara

Aplikasi ini dibuat dalam bentuk web app menggunakan Streamlit
sehingga pengguna dapat memasukkan data secara interaktif dan
melihat hasil analisis dalam bentuk tabel dan grafik.

--------------------------------------------------
2. TUJUAN PROGRAM
--------------------------------------------------

Tujuan dari pembuatan program ini adalah:

1. Menerapkan konsep energi terbarukan (PLTA) ke dalam program komputer.
2. Melakukan forecasting debit sungai berdasarkan faktor iklim.
3. Menghitung potensi daya listrik PLTA.
4. Menentukan kelayakan sungai sebagai PLTA mikro atau mini.
5. Menyajikan hasil dalam bentuk visualisasi grafik.

--------------------------------------------------
3. INPUT PROGRAM
--------------------------------------------------

Input yang dimasukkan oleh pengguna meliputi:

A. Data Sungai
- Nama sungai
- Debit rata-rata sungai (m3/s)
- Head / tinggi jatuh air (m)

B. Data Iklim Bulanan
Untuk setiap bulan yang dipilih:
- Curah hujan (mm)
- Suhu rata-rata (°C)
- Kelembaban udara (%)

Pengguna dapat memilih bulan tertentu saja
(tidak harus satu tahun penuh).

--------------------------------------------------
4. METODE FORECASTING
--------------------------------------------------

Debit sungai hasil forecasting dihitung menggunakan pendekatan empiris
berdasarkan pengaruh faktor iklim:

Q_forecast = Q_dasar × (1 + k_r × R − k_t × T + k_h × H)

Keterangan:
- Q_forecast : debit hasil forecasting (m3/s)
- Q_dasar    : debit rata-rata sungai
- R          : curah hujan (mm)
- T          : suhu udara (°C)
- H          : kelembaban udara (fraksi)

Pengaruh faktor:
- Curah hujan meningkatkan debit
- Suhu menurunkan debit akibat evaporasi
- Kelembaban meningkatkan debit

--------------------------------------------------
5. PERHITUNGAN DAYA PLTA
--------------------------------------------------

Daya PLTA dihitung menggunakan persamaan dasar:

P = ρ × g × Q × H

Dengan:
- ρ = 1000 kg/m3 (massa jenis air)
- g = 9.81 m/s2
- Q = debit sungai (m3/s)
- H = head (m)

Hasil daya ditampilkan dalam satuan kiloWatt (kW).

--------------------------------------------------
6. KELAYAKAN PLTA
--------------------------------------------------

Kelayakan PLTA ditentukan berdasarkan debit rata-rata hasil forecasting:

- Debit ≥ 5 m3/s   → Sangat Layak (PLTA Mini)
- 1 ≤ Debit < 5    → Layak (PLTA Mikro)
- Debit < 1 m3/s   → Kurang Layak

--------------------------------------------------
7. OUTPUT PROGRAM
--------------------------------------------------

Output yang dihasilkan program meliputi:

1. Tabel hasil forecasting debit dan daya PLTA per bulan
2. Grafik batang (Bar Chart) debit sungai hasil forecasting
3. Grafik batang (Bar Chart) daya PLTA per bulan
4. Informasi status kelayakan PLTA

Visualisasi digunakan untuk mempermudah analisis data.

--------------------------------------------------
8. CARA MENJALANKAN PROGRAM
--------------------------------------------------

1. Pastikan Python sudah terinstal.
2. Install library yang dibutuhkan:
   - streamlit
   - numpy
   - pandas
   - matplotlib

3. Jalankan program dengan perintah:
   streamlit run app.py

4. Aplikasi akan terbuka di browser secara otomatis.

--------------------------------------------------
9. KESIMPULAN
--------------------------------------------------

Program ini dapat digunakan sebagai alat bantu analisis awal
untuk mengetahui potensi sungai sebagai sumber energi listrik
tenaga air. Dengan mempertimbangkan faktor iklim, hasil forecasting
memberikan gambaran realistis mengenai debit sungai dan daya PLTA,
sehingga dapat membantu perencanaan energi terbarukan.

==================================================
