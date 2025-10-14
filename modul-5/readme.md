# 🧩 Modul 5 & 6 — Perulangan (For-Loop)

## 🎯 Tujuan Pembelajaran

Setelah mengikuti praktikum ini, mahasiswa diharapkan mampu:

1. Memahami konsep dasar **perulangan (loop)** dalam pemrograman.
2. Menerapkan **struktur kontrol for-loop** untuk menyelesaikan berbagai permasalahan.
3. Menulis program menggunakan bahasa Go dengan kontrol perulangan yang efisien dan benar.

---

## 📘 5.1 Paradigma Perulangan

Perulangan merupakan salah satu struktur kontrol yang memungkinkan suatu instruksi dilakukan **berulang kali** dalam waktu atau jumlah tertentu.  
Tanpa instruksi perulangan, maka suatu instruksi akan ditulis berulang sebanyak jumlah yang diinginkan.

Sebagai contoh: menuliskan teks `"CAK1BAB3 Algoritma Pemrograman 1"` sebanyak 1000 kali.

### 🔹 Tanpa Perulangan

```go
fmt.Println("CAK1BAB3 Algoritma Pemrograman 1")
fmt.Println("CAK1BAB3 Algoritma Pemrograman 1")
fmt.Println("CAK1BAB3 Algoritma Pemrograman 1")
// ...
// dan seterusnya hingga 1000 baris
```

### 🔹 Dengan Perulangan

```go
for i := 1; i <= 1000; i++ {
    fmt.Println("CAK1BAB3 Algoritma Pemrograman 1")
}
```

Terlihat bahwa dengan for-loop, kode jauh lebih ringkas dan mudah dibaca.

⚠️ Penting: Pastikan setiap perulangan memiliki kondisi berhenti, agar program tidak berjalan tanpa henti (infinite loop).

## 📘 5.2 Karakteristik For-Loop

Perulangan dengan for-loop digunakan untuk mengeksekusi instruksi sebanyak n kali (berdasarkan iterasi).

| **Pseudocode**                                      | **Bahasa Go**                                          |
| --------------------------------------------------- | ------------------------------------------------------ |
| `for i ← 1 to n do`<br>  `// instruksi`<br>`endfor` | `for i := 1; i <= n; i++ {`<br>  `// instruksi`<br>`}` |

### 🔹 Komponen For-Loop

**Inisialisasi** — penetapan variabel iterasi, misal i := 1.

**Kondisi** — menentukan kapan loop berhenti, misal i <= n.

**Update** — perubahan nilai variabel iterasi, misal i++.

Gunakan tanda titik koma ; untuk memisahkan inisialisasi, kondisi, dan update.
Gunakan indentasi (tab atau 4 spasi) agar bagian kode mudah dibaca.

## 📘 5.3 Implementasi For-Loop

Contoh program menampilkan teks "CAK1BAB3 Algoritma Pemrograman 1" sebanyak 1000 kali:

```go
// filename: Alpo1.go
package main

import "fmt"

func main() {
var iterasi, n int
n = 1000

    for iterasi = 1; iterasi <= n; iterasi++ {
        fmt.Println(iterasi, "CAK1BAB3 Algoritma Pemrograman 1")
    }

}
```

### 5.4 Contoh Soal dan Pembahasan

#### 🧩 Soal 1

Buatlah program untuk menampilkan bilangan dari a sampai dengan b.

**Masukan:** dua bilangan bulat a dan b dengan a ≤ b.

**Keluaran:** baris bilangan dari a sampai b.

| No  | Masukan | Keluaran                         |
| --- | ------- | -------------------------------- |
| 1   | `2 5`   | `2 3 4 5`                        |
| 2   | `6 6`   | `6`                              |
| 3   | `-5 7`  | `-5 -4 -3 -2 -1 0 1 2 3 4 5 6 7` |

#### 💡 Jawaban

```go
package main
import "fmt"

func main() {
    var a, b int
    fmt.Scan(&a, &b)

    for j := a; j <= b; j++ {
        fmt.Print(j, " ")
    }
}
```

#### 📟 Contoh Eksekusi

```plaintext
Input:
2 5
Output:
2 3 4 5

```

#### 🧩 Soal 2

Buatlah program untuk menghitung luas beberapa segitiga berdasarkan input sisi alas dan tinggi.

**Masukan:**

Baris pertama berisi bilangan bulat n (jumlah segitiga)

n baris berikutnya berisi dua bilangan: alas dan tinggi

**Keluaran:**

n baris yang masing-masing berisi nilai luas segitiga

| No  | Masukan                                               | Keluaran                               |
| --- | ----------------------------------------------------- | -------------------------------------- |
| 1   | 5 <br> 11 2 <br> 32 14 <br> 6 2 <br> 15 15 <br> 20 35 | 11 <br> 224 <br> 6 <br> 112.5 <br> 350 |
| 2   | 3 <br> 12 32 <br> 231 234 <br> 43 34                  | 192 <br> 27027 <br> 731                |

#### 💡 Jawaban

```go
package main
import "fmt"

func main() {
    var n, alas, tinggi int
    var luas float64

    fmt.Scan(&n)
    for j := 1; j <= n; j++ {
        fmt.Scan(&alas, &tinggi)
        luas = 0.5 * float64(alas*tinggi)
        fmt.Println(luas)
    }
}

```

#### 📟 Contoh Eksekusi

```plaintext
Input:
3
12 32
231 234
43 34

Output:
192
27027
731


```

#### 🧩 Soal 3

Buatlah program untuk menghitung **hasil perkalian dua bilangan tanpa menggunakan operator \***.

**Masukan:** dua bilangan bulat positif
**Keluaran:** hasil perkalian dari dua bilangan tersebut

| No  | Masukan | Keluaran |
| --- | ------- | -------- |
| 1   | `2 100` | `200`    |
| 2   | `7 6`   | `42`     |

#### 💡 Jawaban

```go
package main
import "fmt"

func main() {
    var v1, v2, hasil int
    fmt.Scan(&v1, &v2)

    hasil = 0
    for j := 1; j <= v2; j++ {
        hasil += v1
    }

    fmt.Println(hasil)
}
```

#### 📟 Contoh Eksekusi

```plaintext
Input:
7 6
Output:
42

```

### 🧠 Ringkasan Materi

1. For-loop merupakan bentuk perulangan berbasis iterasi yang terdiri dari inisialisasi, kondisi, dan update.
2. Struktur dasarnya di Go adalah:

```go
for inisialisasi; kondisi; update {
    // instruksi
}
```

3. Pastikan kondisi berhenti (termination) terpenuhi agar tidak terjadi infinite loop.
4. For-loop dapat digunakan untuk berbagai operasi berulang seperti mencetak nilai, menghitung hasil aritmatika, dan pengolahan data berulang.
