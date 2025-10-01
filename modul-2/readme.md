# 📝 Modul 2 — I/O, Tipe Data & Variabel

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan modul ini, peserta mampu:

- Memahami konsep dasar **Input** (membaca data dari pengguna) dan **Output** (menampilkan data ke layar)
- Mengenal cara penulisan instruksi I/O dalam bahasa pemrograman Go
- Menggunakan variabel untuk menyimpan data sementara dalam program

---

## 📘 Materi

### 2.1 Input dan Output (I/O)

#### 📥 Input

Input adalah instruksi untuk **membaca data dari pengguna**.  
Data dari pengguna akan disimpan dalam **variabel** untuk diproses.

Perangkat input misalnya: **keyboard, mouse, layar sentuh**.

Notasi umum input vs Go:

| Instruksi Dasar         | Bahasa Go                    | Keterangan                                             |
| ----------------------- | ---------------------------- | ------------------------------------------------------ |
| `input(var_1)`          | `fmt.Scan(&var_1)`           | Membaca input tanpa format khusus                      |
| `input(var_1)`          | `fmt.Scanf("%d", &var_1)`    | Membaca input dengan format (misal `%d` untuk integer) |
| `input(var_1, nilai_y)` | `fmt.Scan(&var_1, &nilai_y)` | Membaca beberapa input sekaligus                       |

> ⚡ **Tips**: Gunakan `fmt.Scan` jika masih pemula, karena lebih sederhana dibanding `fmt.Scanf`.

---

#### 📤 Output

Output adalah instruksi untuk **menampilkan data ke layar**.  
Fungsinya agar pengguna bisa melihat hasil dari program.

Notasi umum output vs Go:

| Instruksi Dasar                              | Bahasa Go                                                | Tampilan                 |
| -------------------------------------------- | -------------------------------------------------------- | ------------------------ |
| `output("Praktikum",2024)`                   | `fmt.Print("Praktikum",2024)`                            | `Praktikum2024`          |
|                                              | `fmt.Println("Praktikum",2024)`                          | `Praktikum 2024`         |
|                                              | `fmt.Printf("Praktikum %v",2024)`                        | `Praktikum 2024`         |
| `print("Praktikum")`<br>`print("Algoritma")` | `fmt.Println("Praktikum")`<br>`fmt.Println("Algoritma")` | Praktikum <br> Algoritma |
|                                              | `fmt.Print("Praktikum")`<br>`fmt.Print("Algoritma")`     | `PraktikumAlgoritma`     |

**Keterangan**:

- `"Praktikum"` dan `"Algoritma"` → data teks (string)
- `2024` → bilangan bulat (integer)
- `Println` → menambahkan spasi antar data + pindah ke baris baru setelah mencetak
- `Printf` → mencetak dengan format tertentu

---

### 💻 Contoh Program (hello2.go)

```go
package main
import "fmt"

func main() {
    var mk string = "Algoritma dan Pemrograman"
    var kode, sks int

    fmt.Print("Tuliskan kode MK dan SKS: ")
    fmt.Scan(&kode, &sks)

    fmt.Println("Kredit MK", kode, "-", mk, "1 adalah", sks, "SKS")
}
```

### 2.2 Tipe Data & Variabel

#### 📌 Apa itu Variabel?

- **Variabel** adalah tempat menyimpan data sementara dalam program.
- Variabel memiliki **nama** dan **tipe data**.
- Gunanya supaya program bisa mengolah data dengan lebih mudah.

📖 **Analogi**: variabel itu seperti **kotak penyimpanan**. Kotak punya label (nama variabel) dan hanya bisa diisi sesuai jenisnya (tipe data).

---

#### 📦 Tipe Data Dasar dalam Go

| Tipe Data             | Contoh         | Deskripsi                   |
| --------------------- | -------------- | --------------------------- |
| `int`                 | `10, -5, 2024` | Bilangan bulat              |
| `float32` / `float64` | `3.14, -0.5`   | Bilangan pecahan/desimal    |
| `string`              | `"Hello"`      | Teks atau kumpulan karakter |
| `bool`                | `true, false`  | Nilai logika (benar/salah)  |

---

#### ✍️ Cara Mendeklarasikan Variabel

1. **Dengan tipe data eksplisit**

```go
var nama string = "Gibran"
var umur int = 20

```

### 2.3 🔖 Konstanta Simbolik

Konstanta adalah **nilai tetap** yang tidak bisa diubah selama program berjalan.  
Konstanta biasanya diberi **nama khusus** agar lebih mudah dipahami, misalnya `PI`.

#### ✍️ Contoh dalam Go

```go
package main
import "fmt"

const PI = 3.14159265358979323846
const MARKER = "AKHIR"

func main() {
    fmt.Println("Nilai PI:", PI)
    fmt.Println("Teks Penanda:", MARKER)
}

```

---

### 2.4 🔡 Tipe Data Character

#### 📌 Penjelasan

- Di Go, **character** sebenarnya berupa angka **integer** yang mewakili simbol tertentu sesuai tabel **ASCII/UTF-8** atau **UTF-16**.
- Ada dua tipe utama:
  - `byte` → alias untuk `uint8` (ASCII/UTF-8)
  - `rune` → alias untuk `int32` (UTF-16)

---

#### ✍️ Contoh Character di Go

```go
package main
import "fmt"

func main() {
    var c1 byte = 'A'   // kode ASCII 65
    var c2 rune = 'a'   // kode ASCII 97
    var c3 rune = '@'   // kode ASCII 64

    fmt.Printf("Karakter: %c, Kode ASCII: %d\n", c1, c1)
    fmt.Printf("Karakter: %c, Kode ASCII: %d\n", c2, c2)
    fmt.Printf("Karakter: %c, Kode ASCII: %d\n", c3, c3)
}

```

## 2.5 Contoh Soal Modul 2

Berikut adalah beberapa contoh soal terkait penggunaan tipe data integer, character dan operasinya.

---

### 1️⃣ Buatlah program yang digunakan untuk menghitung hasil penjumlahan 5 bilangan bulat.

**Masukan** terdiri dari lima bilangan bulat `a`, `b`, `c`, `d`, dan `e`.  
**Keluaran** berupa bilangan hasil penjumlahan lima bilangan bulat `a`, `b`, `c`, `d`, dan `e`.

---

#### 📌 Contoh Masukan dan Keluaran

| No  | Masukan        | Keluaran |
| --- | -------------- | -------- |
| 1   | 3 2 7 10 2     | 24       |
| 2   | 11 22 33 44 55 | 165      |

---

#### 💡 Jawaban:

```go
// filename: penjumlahan.go
package main

import "fmt"

func main() {
    var a, b, c, d, e int
    var hasil int

    fmt.Scanln(&a, &b, &c, &d, &e)
    hasil = a + b + c + d + e

    fmt.Println("Hasil penjumlahan", a, b, c, d, e, "adalah", hasil)
}

```

### 2️⃣ Sebuah program digunakan untuk menghitung persamaan:

\[
f(x) = \frac{2}{x+5} + 5
\]

**Masukan** terdiri dari sebuah bilangan bulat.  
**Keluaran** berupa bilangan yang menyatakan nilai dari \( f(x) \).

---

#### 📌 Contoh Masukan dan Keluaran

| No  | Masukan | Keluaran             |
| --- | ------- | -------------------- |
| 1   | 5       | 5.2                  |
| 2   | -23     | 4.888888888888888889 |

---

#### 💡 Jawaban:

```go
package main

import "fmt"

func main() {
    var x, fx float64
    fmt.Scan(&x)
    fx = 2/(x+5) + 5
    fmt.Println(fx)
}
```

### 3️⃣ Program ASCII

Tipe karakter sebenarnya hanya apa yang tampak dalam tampilan. Di dalamnya tersimpan dalam bentuk biner 8 bit (**byte**) atau 32 bit (**rune**).

**Tugas:**  
Buat program ASCII yang akan:

1. Membaca **5 buah data integer** dan mencetaknya dalam format karakter.
2. Membaca **3 buah data karakter** lalu mencetak **3 buah karakter setelahnya** (berdasarkan tabel ASCII).

---

#### 📌 Spesifikasi

- **Masukan** terdiri dari dua baris:
  - Baris pertama: 5 buah data integer (nilai 32 s.d. 127).
  - Baris kedua: 3 buah data karakter **berdampingan tanpa spasi**.
- **Keluaran** terdiri dari dua baris:
  - Baris pertama: 5 representasi karakter dari data integer.
  - Baris kedua: 3 buah karakter hasil pergeseran +1 ASCII dari input karakter.

---

#### 📊 Contoh Masukan dan Keluaran

| No  | Masukan           | Keluaran |
| --- | ----------------- | -------- |
| 1   | 66 97 103 117 115 | Bagus    |
|     | SNO               | TOP      |

---

#### 💡 Catatan

- Gunakan `fmt.Scanf("%c", &var)` untuk pembacaan satu karakter.
- Gunakan `fmt.Printf("%c", var)` untuk menuliskan karakter.

---

#### ✅ Jawaban

```go
// filename : ascii.go
package main

import "fmt"

func main() {
    var c1, c2, c3, c4, c5 byte
    var b1, b2, b3 byte

    // Input 5 integer → langsung dibaca sebagai byte
    fmt.Scan(&c1, &c2, &c3, &c4, &c5)

    // Input 3 karakter tanpa spasi
    fmt.Scanf("%c", &b1)
    fmt.Scanf("%c", &b2)
    fmt.Scanf("%c", &b3)

    // Output 5 karakter hasil konversi ASCII
    fmt.Printf("%c%c%c%c%c\n", c1, c2, c3, c4, c5)

    // Output 3 karakter setelahnya
    fmt.Printf("%c%c%c\n", b1+1, b2+1, b3+1)
}
```
