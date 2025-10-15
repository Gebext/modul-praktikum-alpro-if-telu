## 🧩 5.5 Soal Latihan Modul 5 (Versi Revisi)

Latihan berikut digunakan untuk menguji pemahaman konsep **perulangan (for-loop)**, serta penggunaan **variabel, tipe data, input/output**, dan **konversi tipe data** di bahasa Go.

---

### 🔹 1. Jumlah Deret Bilangan Ganjil

Buatlah program untuk menghitung jumlah semua **bilangan ganjil** dari `1` sampai dengan `n`.

**Masukan:**  
Sebuah bilangan bulat positif `n`.

**Keluaran:**  
Sebuah bilangan bulat yang merupakan hasil penjumlahan bilangan ganjil dari `1` hingga `n`.

| No  | Masukan | Keluaran |
| --- | ------- | -------- |
| 1   | 3       | 4        |
| 2   | 10      | 25       |
| 3   | 1       | 1        |

💡 _Petunjuk:_ gunakan operator `%` untuk mengecek apakah suatu bilangan ganjil.

---

### 🔹 2. Hitung Total Biaya Belanja

Buatlah program untuk menghitung total harga dari `n` barang yang dibeli.  
Setiap barang memiliki **harga satuan** dan **jumlah unit**.

**Masukan:**

- Baris pertama berisi bilangan bulat `n` (jumlah barang).
- `n` baris berikutnya berisi dua bilangan bulat `harga_satuan` dan `jumlah_unit`.

**Keluaran:**  
Satu bilangan bulat yang menyatakan total biaya seluruh barang.

| No  | Masukan                                | Keluaran |
| --- | -------------------------------------- | -------- |
| 1   | 3 <br> 10000 2 <br> 5000 4 <br> 2000 1 | 34000    |
| 2   | 2 <br> 15000 1 <br> 7500 3             | 37500    |

💡 _Petunjuk:_ hasil tiap baris = harga_satuan × jumlah_unit, lalu dijumlahkan menggunakan for-loop.

---

### 🔹 3. Tabel Pangkat Dua

Buatlah program untuk menampilkan tabel **pangkat dua** dari `1` sampai `n`.

**Masukan:**  
Sebuah bilangan bulat positif `n`.

**Keluaran:**  
Menampilkan setiap bilangan dari `1` hingga `n` beserta hasil pangkat duanya.

| No  | Masukan | Keluaran                                            |
| --- | ------- | --------------------------------------------------- |
| 1   | 4       | 1 1 <br> 2 4 <br> 3 9 <br> 4 16                     |
| 2   | 6       | 1 1 <br> 2 4 <br> 3 9 <br> 4 16 <br> 5 25 <br> 6 36 |

💡 _Petunjuk:_ gunakan `fmt.Println(i, i*i)` di dalam perulangan.

---

### 🔹 4. Hitung Rata-Rata Nilai

Buatlah program untuk menghitung rata-rata dari `n` nilai mahasiswa.

**Masukan:**

- Baris pertama adalah bilangan bulat `n`.
- `n` baris berikutnya masing-masing berisi satu nilai bertipe **float**.

**Keluaran:**  
Sebuah bilangan desimal yang menunjukkan rata-rata nilai.

| No  | Masukan                           | Keluaran |
| --- | --------------------------------- | -------- |
| 1   | 4 <br> 80 <br> 70 <br> 90 <br> 60 | 75       |
| 2   | 3 <br> 100 <br> 100 <br> 80       | 93.33    |

💡 _Petunjuk:_ jumlahkan semua nilai, lalu bagi dengan `float64(n)` untuk hasil rata-rata bertipe float.

---

### 🔹 5. Hitung Banyak Digit

Buatlah program untuk menghitung berapa banyak digit (angka) dari suatu bilangan bulat positif.

**Masukan:**  
Sebuah bilangan bulat positif `n`.

**Keluaran:**  
Sebuah bilangan bulat yang menunjukkan jumlah digit.

| No  | Masukan | Keluaran |
| --- | ------- | -------- |
| 1   | 5       | 1        |
| 2   | 123     | 3        |
| 3   | 10000   | 5        |

💡 _Petunjuk:_ gunakan perulangan dengan operasi pembagian (`n = n / 10`) untuk menghitung jumlah digitnya.

---

### 🧠 Catatan

- Semua soal dapat diselesaikan **hanya dengan materi hingga Modul 5**: input/output, variabel, tipe data, casting, dan for-loop.
- Hindari penggunaan array, slice, atau fungsi-fungsi bawaan yang belum diajarkan.

---
