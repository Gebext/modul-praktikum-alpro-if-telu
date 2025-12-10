## Soal 1 — Validasi Input & Rata-rata Dinamis

**(Medium–Hard | I/O + do-while-loop + validasi)**

**Deskripsi**

Buat program Go yang membaca bilangan bulat satu per satu hingga pengguna memasukkan -1.
Program hanya menghitung bilangan positif (>0) dan mengabaikan bilangan negatif (selain -1 sebagai sentinel).

Setelah loop berhenti, tampilkan:

1. Jumlah bilangan valid

2. Rata-rata bilangan valid (2 angka di belakang koma)

**Aturan**

- Gunakan do-while-loop

- Lakukan validasi input

- Jika tidak ada bilangan valid, tampilkan 0 0.00

**Contoh Input**

```diff
5
-3
10
0
7
-1
```

**Contoh Output**

```diff
3 7.33

```

## Soal 2 — Simulasi Saldo & Loop Bersyarat

**(Hard | I/O + do-while-loop + logika kondisi)**

**Deskripsi**

Buatlah program yang digunakan untuk menghitung banyaknya digit dari suatu
bilangan

**Masukan** berupa bilangan bulat positif.

**Keluaran** berupa bilangan bulat yang menyatakan banyaknya digit dari bilangan yang
diberikan pada masukan

**Contoh masukkan dan keluaran**

| No  | Masukan | Keluaran |
| --- | ------- | -------- |
| 1   | 5       | 1        |
| 2   | 234     | 3        |
| 3   | 78787   | 5        |
| 4   | 1894256 | 7        |

## Soal 3 — Aproksimasi Akar Kuadrat (Formula Matematis)

**(Hard | do-while-loop + numerik + matematika)**

**Deskripsi**
Buat program Go yang menghitung akar kuadrat dari bilangan positif n menggunakan metode Newton-Raphson.

Rumus Iterasi

![alt text]({B5911E72-CDFA-41F6-A797-375EFCBE246F}.png)

Iterasi dihentikan ketika:

![alt text]({E64892AE-23A2-4228-AEB4-09D32DF6889C}.png)

**Aturan**

- Input: bilangan real n

- Gunakan do-while-loop

- Jangan gunakan math.Sqrt()

- Output dibulatkan ke 5 angka desimal

**Contoh Input**

```diff
10
```

**Contoh Output**

```diff
3.16228

```
