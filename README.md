# Green Finance Analysis

---

![ilustrasi green finance](https://github.com/Agus-Iskandar-D/Green-Finance-Analysis/blob/main/ilustrasi%20green%20finance%20analysis.png)

## 📝Pendahuluan

Green Finance atau dalam bahasa Indonesia keuangan hijau merupakan aktivitas keuangan yang memastikan proyek menghasilkan dampak positif bagi lingkungan atau membuat lingkungan lebih baik. Green finance analisis berarti analisis keuangan untuk menilai dampak sebuah proyek terhadap lingkungan. Empat nilai yang dicari dalam menganalisis keuangan hijau, yakni Green Net Present Value (GNPV), Carbon Return in Invesment (CROI), Social Return of Invesment (SROI), Economic Risk Adjustment Factor (ERAF), dan Geospatial Risk Factor (GRI). 

## 🍀GNPV

GNPV merupakan modifikasi dari Net Present Value (NPV) standar yang memasukkan faktor lingkungan, yakni emisi, untuk mengevaluasi kelayakan finansial proyek hijau.
Rumus yang dibutuhkan untuk menghitung GNPV adalah:

$$GNPV = \sum_{t=0}^{n} \frac{CF_t+E_t}{(1+r)^t}\-I_0$$

- $CF_t$ : Arus kas konvensional pada periode $t$ (dalam rupiah), yakni pendapatan operasional dikurangi biaya operasional dan pajak.
- $E_t$ : Nilai moneter eskstenalitas lingkungan dalam periode $t$ (dalam rupiah), misal pengurangan Emisi CO2 atau penghematan air
- $r$ : tingkat diskonto, yakni tingkat pengembalian uang di masa depan.
- $t$ : Waktu dalam tahun
- $N$ : usia proyek
- $I$ : Investasi awal dalam rupian

  Jika $GNPV$ > 0 maka proyek dianggap layak secara finansial dan lingkungan. Semkain besar nilai GNVP, maka proyek semakin menarik

## 🍀 CROI

Carbon Return of Investment (CROI) merupakan perhitungan pengembalian investasi yang ditambahkan nilai pengurangan carbon dalam rupiah. CROI digunakan untuk menilai investasi proyek hijau. Rumus yang digunakan untuk menghitungnya adalah sebagai berikut:

$$CROI= \frac{\sum_{t=1}^{N}{(R_t*P_c)}}{I_0}$$

- $R_t$ : Pengurangan emisi tahunan pada periode (dalam ton CO2e)
- $P_c$ : Harga karbon per ton CO2e
- $N$ : Umur proyek dalam tahun

Jika $CROI$ > 1, maka proyek menghasilkan pengurangan karbon lebih besar daripada biayanya.

## 🍀SROI

Social Return of Investment (SROI) merupakan pengembalian investasi dengan tambahan variabel dampak sosial, bisa berupa tercipatanya lapangan kerja atau penghematan biaya kesehatan. SROI digunakan untuk mengukur nilai lingkungan sosial, lingkungan, dan ekonomi dari investasi sebuah proyek. Berikut rumua perhitungannya:

$$SROI = \frac{\sum{NV_{sosial}}}{I_0}$$

- $NV_{sosial}$ : nilai sekarang dari dampak sosial yang diuangkan.Bisa dalam bentuk nilai lapangan pekerjaan yang diciptakan atau biaya penghematan energi yang didapatkan.

Jika $SROI$ > 1, makan proyek tersebut memberikan dampak sosial yang besar. Makin tinggi nilainya, artinya makin besar pula dampak sosial yang dihasilkan.

## 🍀ERAF

Economic Risk Adjustment Factor (ERAF) merupakan tingkat penyesuaian faktor risiko ekonomi. ERAF digunakan sebagai alat ukur untuk menilai besaran faktor risiko yang dipengaruhi kondisi ekonomi makro. Rumusnya sebagai berikut:

$$ERAF = 1 + w_1({\frac{I_r - I_{r,base}}{I_{r,base}}}) + w_2({\frac{U_r - U_{r,base}}{U_{r,base}}}) - w_3({\frac{G_g - G_{g,base}}{G_{g,base}}})$$

- $I_r$ : tingkat inflasi saat ini
- $I_{r,base}$ : tingkat inflasi dasar, yakni tingkat inflasi yang ditetapkan, misalnya tingkat inflasi yang ditetapkan oleh BI
- $U_r$ : tingkat penganguran yang terjadi saat ini
- $U_{r,base}$: tingkat penganguran dasar, yang diambil dari rata-rata data historis
- $G_g$ : Pertumbuhan PDB saat ini
- $G_{g,base}$ : Pertumbuha PDB dasar, yang diambil dari rata-rata data historis
- $w_1, w_2, w_3$: bobot relatif dimana jika digabungkan nilainya menjadi bilang bulat 1

  Jika $ERAF$ > 1 artinya meningkatkan risiko, jika $ERAF$ < 1, artinya menurunkan risiko

## 🍀GRI

Geospatial Riks Index (GRI) merupakan skor tingkat risiko berbasis lokasi untuk mengukur risiko berbasis lokasi dengan menggabungkan faktor-faktor spasial. GRI dihitung dengan rumus sebagai berikut:

$$GRI = w_1S_{hazard} + w_2S_{proximity} + w_3S_{landuse}$$

- $S_{hazard}$ : Skor normalisasi bencana alam berdasarkan data histori atau peta risiko BNPB/BMKG. Nilainya 0-1
- $S_{proximity}$ : Skor normalisasi kedekatan dengan kawasan lindung dengan skala 0-1.
- $S_{landuse}$ : Skor dampak normalisasi perubahan lahan dengan skala 0-1.
- $w_1, w_2, w_3$ : bobot relatif dengan menggunakan analisis Analytical Hierarchy Process

Jika GRI > 0.7, maka proyek memerlukan enhance due diligence, yakni investigasi lebih lanjut dan kemungkinan proyek ditolak.

## 🗂️Dataset

Untuk melakukan green finance analysis disediakan lima dataset, yakni fincancial dataset, environmental dataset, social dataset, economic dataset, dan geospatial dataset

### 💸Financial Dataset

Financial dataset berisi:

| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Project_ID`  | identitas unik dari proyek  |
| `Invesment_Cost`  | Dana yang diinvestasikan yang juga disebut `Invesment_Amount'  |
| `Revenue_Stream` | Arus Pendapatan, yakni jumlah pendapatan |
| `Debt_Ration`  | Rasio Utang, yakni perbandingan total leabilities (kewajiban) dengan total aset.  |
| `Payment_Delay` | Penundaan Pembayaran, yakni pembayaran mengalamai penundaan dibayar dari jatuh tempo|
| `Konteks_Proyek`  | Penjelasan dan kondisi proyek berkaitan dengan pendaan dan operasional  |
| `Status_Rank`  | Peringkat proyek berdasarkan kondisi keuangannya  |

Adapun variabel-variabel yang menjadi indikator dari kesehatan finansial sebuah proyek yang menunjukan hijau:

| Nama Variabel  | Deskripsi Detail |
| ------------- | ------------- |
| `Investment_Amount`  | Jumlah dana yang diinvestasikan.  |
| `Loan_Intereset_Rate`  | Suku bunga pinjaman (dalam persen per tahun). Suku bunga rendah sering kali mengindikasikan proyek dengan risiko rendah atau adanya insentif keuangan hijau. |
| `Default_Risk_Score` | Skor kredit atau gagar membayar pinjaman dalam skala 1-100, makin tinggi berarti makin berisiko.  |
| `Green_Spread_Bond`  | Selisih imbal hasil (dalam basis poin) antara obligasi hijau dan obligasi konvensional dengan profil risiko serupa. Nilai negatif menunjukkan "greenium", yaitu preferensi investor untuk aset hijau. |



### 🌱Environmental Dataset

Environmental dataset beisi:

| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Project_ID`  | identitas unik dari proyek  |
| `CO2_Reduction`  | Pengurangan emisi karbon dalam ton  |
| `Energy_Output` | Energi yang dihasilkan |
| `Environmental_Risk_Index`  | indek risiko terhadap lingkungan  |
| `Konteks_Lingkungaa`  | Penjelasan dan kondisi proyek terhadap lingkungan  |
| `Peringkat_Dampak`  | Peringkat proyek berdasarkan dampaknya terhadap lingkungan  |


### 👥Social Dataset

Social Dataset berisi:

| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Project_ID`  | identitas unik dari proyek  |
| `Land_Status`  | Status lahan proyek  |
| `Community_Support` | Tingkat keterlibatan proyek dalam mendukun masyrakat sekitar |
| `Population_Density`  | Tingkat kepadatan penduduk, yakni jumlah penduduk per luas wilayan  |
| `Konteks_Sosial`  | Penjelasan dan kondisi proyek terkait kondisi sosial sekitar proyek  |
| `Tingkat_Konflik`  | Peringkat proyek berdasarkan potensi konflik yang terjadi dengan masyarakat |


### 💵Economic Dataset

Economic Dataset berisi:

| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Project_ID`  | identitas unik dari proyek  |
| `GDP_Growth`  | Pertumbuhan GDP yang dihasilkan oleh proyek |
| `Interest_Rate` | Tingkat suku bunga |
| `Bond_Yield`  | Imbal hasil obligasi  |
| `Konteks_Ekonomi`  | Penjelasan dan kondisi proyek terkait konteks ekonomi  |
| `Daya_Tarik_Investasi`  | Peringkat proyek berdasarkan tikngat investasi |


### 🌏Geospatial Dataset

Geospatial Dataset berisi:

| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Project_ID`  | identitas unik dari proyek  |
| `Solar Irradiance`  | seberapa banyak "sinar" matahari yang jatuh pada suatu area tertentu pada waktu tertentu, biasanya diukur dalam watt per meter persegi (W/m²) |
| `Water_Flow` | Aliran air yang ada |
| `Distance_to_Grid`  | Jarak proyek kepada jaringan listrik yang sudah ada  |
| `Konteks_Geospasial`  | Penjelasan dan kondisi proyek terkait geospasial  |
| `Efisiensi_Lahan`  | Peringkat proyek efisiensi penggunaan lahan |


## 📊Analisis

Dataset yang tersedia tidak langsung memberikan vaariabel data yang bisa menghitung GNPV, CROI<, SROI, ERAF, dan GRI. Untuk itu diperlukan perhitungan untuk mencari variabel-variabel yang dibutuhkan. Proses analisis menggunakan Python dengan library Pandas dan Numpy.

### Query 1: Mencari nilai GNVP

Tujuan: Mencari nilai GNVP
Konsep: loop for untuk menghitung berulang setiap row, pandas dan numpy untuk melakukan perhitungan
Output: Menampilkan nilan GNVP

Dataset utama yang digunakan adalah Financial Dataset. Pada dataset tersebut sudah tersedian `Investasi_Cost`. Untuk nilai pengurangan emisi, data diambil dari Environmental Dataset. Untuk mencari nilai $CF_t$ $r$, kita menggunakan asumsi bahwa $C_t$ adalah `Revenue_Stream` dan $r$ adalah suku bunga atau BI rate.

## 📶 Visualisasi Data

Proses visualisasi menggunakan library matpotlib dan seaborn.


## 💡Hasil dan Kesimpulan

Dari proses analisis dan visualisasi dapat dilihat hasilnnya berdasarkan dataset yang tersedia. Kesimpulan yang dapat diambil:

- Proyek dengan potensi dampak lingkungan yang baik dan kesehatan keuangannya adalah....
- ...


