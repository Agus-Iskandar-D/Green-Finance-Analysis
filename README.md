# Green Finance Analysis

---

![ilustrasi green finance](https://github.com/Agus-Iskandar-D/Green-Finance-Analysis/blob/main/ilustrasi%20green%20finance%20analysis.png)

## 📝Pendahuluan

Green Finance atau dalam bahasa Indonesia keuangan hijau merupakan aktivitas keuangan yang memastikan proyek menghasilkan dampak positif bagi lingkungan atau membuat lingkungan lebih baik.
Empat nilai yang dicari dalam menganalisis keuangan hijau, yakni Green Net Present Value (GNPV), Carbon Return in Invesment (CROI), Social Return of Invesment (SROI), Economic Risk Adjustment Factor (ERAF), dan Geospatial Risk Factor (GRI).

## 🍀GNPV

GNPV merupakan modifikasi dari Net Present Value (NPV) standar yang memasukkan faktor lingkungan, yakni emisi, untuk mengevaluasi kelayakan finansial proyek hijau. Data yang digunakan adalah dataset finansial yang berisi field sebagai berikut:
| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Invesment_Cost`  | Dana yang diinvestasikan yang juga disebut `Invesment_Amount'  |
| `Revenue_Stream` | Arus Pendapatan, yakni jumlah pendapatan |
| `Debt_Ration`  | Rasio Utang, yakni perbandingan total leabilities (kewajiban) dengan total aset.  |
| `Payment_Delay` | Penundaan Pembayaran, yakni pembayaran mengalamai penundaan dibayar dari jatuh tempo|

Yang dibutuhkan untuk menghitung GNPV, rumus yang digunakan:

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

$$SROI = \frac{\sum{NV_sosial}}{I_0}$$

- $NV_sosial$ : nilai sekarang dari dampak sosial yang diuangkan.Bisa dalam bentuk nilai lapangan pekerjaan yang diciptakan atau biaya penghematan energi yang didapatkan.

Jika $SROI$ > 1, makan proyek tersebut memberikan dampak sosial yang besar. Makin tinggi nilainya, artinya makin besar pula dampak sosial yang dihasilkan.

## 🍀ERAF

Economic Risk Adjustment Factor (ERAF) merupakan tingkat penyesuaian faktor risiko ekonomi. ERAF digunakan sebagai alat ukur untuk menilai besaran faktor risiko yang dipengaruhi kondisi ekonomi makro. Rumusnya sebagai berikut:

$$ERAF = 1 + w_1({\frac{I_r - I_r,base}{I_r,base}}) + w_2({\frac{U_r - U_r,base}{U_r,base}}) - w_3({\frac{G_g - G_g,base}{G_g,base}})$$

- $I_r$ : tingkat inflasi saat ini
- $I_r,base$ : tingkat inflasi dasar, yakni tingkat inflasi yang ditetapkan, misalnya tingkat inflasi yang ditetapkan oleh BI
- $U_r$ : tingkat penganguran yang terjadi saat ini
- $U_r,base$: tingkat penganguran dasar, yang diambil dari rata-rata data historis
- $G_g$ : Pertumbuhan PDB saat ini
- $G_g,base$ : Pertumbuha PDB dasar, yang diambil dari rata-rata data historis
- $w_1, w_2, w_3$: bobor relatif dimana jika digabungkan nilainya menjadi bilang bulat 1

  Jika $ERAF$ > 1 artinya meningkatkan risiko, jika $ERAF$ < 1, artinya menurunkan risiko

## 🍀GRI


