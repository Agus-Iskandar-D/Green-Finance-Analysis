# Green Finance Analysis

---

![ilustrasi green finance](https://github.com/Agus-Iskandar-D/Green-Finance-Analysis/blob/main/ilustrasi%20green%20finance%20analysis.png)

## 📝Pendahuluan

Green Finance atau dalam bahasa Indonesia keuangan hijau merupakan aktivitas keuangan yang memastikan proyek menghasilkan dampak positif bagi lingkungan atau membuat lingkungan lebih baik.
Empat nilai yang dicari dalam menganalisis keuangan hijau, yakni Green Net Present Value (GNPV), Carbon Return in Invesment (CROI), Social Return in Invesment (SROI), Economic Risk Adjustment Factor (ERAF), dan Geospatial Risk Factor (GRI).

## 🍀GNPV

GNPV merupakan modifikasi dari Net Present Value (NPV) standar yang memasukkan faktor lingkungan untuk mengevaluasi kelayakan finansial proyek hijau. Data yang digunakan adalah dataset finansial yang berisi field sebagai berikut:
| Nama Field  | Deskripsi Detail |
| ------------- | ------------- |
| `Invesment_Cost`  | Dana yang diinvestasikan  |
| `Revenue_Stream` | Arus Pendapatan |
| `Debt_Ration`  | Rasio Utang  |
| `Payment_Delay` | Keterlambatan Pembayaran |

Yang dibutuhkan untuk menghitung GNPV, rumus yang digunakan:

$$GNPV = \sum_{t=0}^{n} \frac{CF_t}{(1+r)^t}$$
