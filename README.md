# Green Finance Analysis

---

![ilustrasi green finance](https://github.com/Agus-Iskandar-D/Green-Finance-Analysis/blob/main/ilustrasi%20green%20finance%20analysis.png)

## 📝Pendahuluan

Green Finance atau dalam bahasa Indonesia keuangan hijau merupakan aktivitas keuangan yang memastikan proyek menghasilkan dampak positif bagi lingkungan atau membuat lingkungan lebih baik.
Empat nilai yang dicari dalam menganalisis keuangan hijau, yakni Green Net Present Value (GNPV), Carbon Return in Invesment (CROI), Social Return in Invesment (SROI), Economic Risk Adjustment Factor (ERAF), dan Geospatial Risk Factor (GRI).

## 🍀GNPV

GNPV merupakan modifikasi dari Net Present Value (NPV) standar yang memasukkan faktor lingkungan, yakni emisi, untuk mengevaluasi kelayakan finansial proyek hijau. Data yang digunakan adalah dataset finansial yang berisi field sebagai berikut:
| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Invesment_Cost`  | Dana yang diinvestasikan yang juga disebut `Invesment_Amount'  |
| `Revenue_Stream` | Arus Pendapatan, yakni jumlah pendapatan |
| `Debt_Ration`  | Rasio Utang, yakni perbandingan total leabilities (kewajiban) dengan total aset.  |
| `Payment_Delay` | Penundaan Pembayaran, yakni pembayaran mengalamai penundaan dibayar dari jatuh tempo|

Yang dibutuhkan untuk menghitung GNPV, rumus yang digunakan:

$$GNPV = \sum_{t=0}^{n} \frac{CF_t+E_t}{(1+r)^t}\-1$$

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
