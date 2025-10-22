# 🧩 Summary Materi

## 🧠 MODUL 2 — Input/Output, Variabel, dan Tipe Data

### 1. Input dan Output (I/O)

Dalam bahasa Go, input dan output dilakukan dengan package fmt.

```go
package main

import "fmt"

func main() {
    var nama string
    var umur int

    fmt.Print("Masukkan nama Anda: ")
    fmt.Scanln(&nama)

    fmt.Print("Masukkan umur Anda: ")
    fmt.Scanln(&umur)

    fmt.Println("Halo,", nama)
    fmt.Println("Umur Anda:", umur)
}
```

**🧾 Penjelasan:**

fmt.Print() → mencetak tanpa newline

fmt.Println() → mencetak dengan newline

fmt.Scanln(&variabel) → menerima input dari user

### 2. Variabel dan Data

Variabel digunakan untuk menyimpan nilai.

```go
var nama string = "Gibran"
var umur int = 20
tinggi := 175.5 // shorthand declaration
```

| Tipe Data | Deskripsi        | Contoh          |
| --------- | ---------------- | --------------- |
| `int`     | Bilangan bulat   | `10`, `-5`      |
| `float64` | Bilangan desimal | `3.14`          |
| `string`  | Teks             | `"Go Language"` |
| `bool`    | Nilai logika     | `true`, `false` |

### 3. Konstanta Simbolik

Nilai tetap yang tidak bisa diubah selama program berjalan.

```go
package main

import "fmt"

const PI = 3.14159
const APLIKASI = "GoLang App"

func main() {
    fmt.Println("Nilai PI:", PI)
    fmt.Println("Nama Aplikasi:", APLIKASI)
}
```

### 4. Tipe Data Character (Rune)

Dalam Go, karakter direpresentasikan dengan tipe rune (alias int32).

```go
package main

import "fmt"

func main() {
    var huruf rune = 'A'
    fmt.Printf("Karakter: %c\n", huruf)
    fmt.Printf("Kode ASCII: %d\n", huruf)
}
```

## ⚙️ MODUL 3 — Operasi dan Casting Tipe Data

### 1. Integer Division dan Modulo

Operasi pembagian dan sisa bagi dilakukan dengan operator / dan %.

```go
package main

import "fmt"

func main() {
    var a, b int = 10, 3

    fmt.Println("Hasil bagi:", a/b)
    fmt.Println("Sisa bagi:", a%b)
}
```

📘 Catatan: Dalam Go, pembagian antar int menghasilkan integer, bukan float.

### 2. Casting (Konversi Tipe Data)

Gunakan TipeData(nilai) untuk mengubah tipe data.

```go
package main

import "fmt"

func main() {
    var a int = 10
    var b float64 = 3.5

    hasil := float64(a) / b
    fmt.Println("Hasil:", hasil)
}
```

### 3. Konversi Integer → String (Itoa)

Gunakan strconv.Itoa(angka) untuk mengubah integer menjadi string.

```go
package main

import (
    "fmt"
    "strconv"
)

func main() {
    var umur int = 20
    umurStr := strconv.Itoa(umur) // int → string
    fmt.Println("Tipe data umurStr:", umurStr)
    fmt.Println("Gabungan string:", "Umur saya " + umurStr)
}
```

### 4. Konversi String → Integer (Atoi)

Gunakan strconv.Atoi(str) untuk mengubah string menjadi integer.
Fungsi ini mengembalikan dua nilai: hasil konversi dan error.

```go
package main

import (
    "fmt"
    "strconv"
)

func main() {
    var input string
    fmt.Print("Masukkan angka: ")
    fmt.Scanln(&input)

    angka, err := strconv.Atoi(input) // string → int
    if err != nil {
        fmt.Println("Input bukan angka!")
        return
    }

    fmt.Println("Angka setelah dikonversi:", angka)
    fmt.Println("Hasil kuadrat:", angka*angka)
}
```

## 🔁 MODUL 5 & 6 — FOR-LOOP

### 1. Paradigma Perulangan

Perulangan digunakan untuk mengeksekusi kode berulang kali.

Format dasar:

```go
for i := 0; i < 5; i++ {
    fmt.Println("Iterasi ke-", i)
}
```

### 2. Jenis For-Loop dalam Go

| Bentuk                               | Contoh                      | Deskripsi                           |
| ------------------------------------ | --------------------------- | ----------------------------------- |
| **Klasik (dengan 3 komponen)**       | `for i := 0; i < 5; i++ {}` | Perulangan dengan kondisi diketahui |
| **While-style loop**                 | `for i < 10 {}`             | Tanpa inisialisasi dan increment    |
| **Infinite loop**                    | `for {}`                    | Loop tanpa batas (gunakan `break`)  |
| **Range loop (iterasi array/slice)** | `for i, v := range arr {}`  | Digunakan untuk koleksi data        |

### 3. Implementasi Perulangan dalam Go

**Contoh 1 — Menampilkan deret angka**

```go
for i := 1; i <= 5; i++ {
fmt.Println(i)
}
```

**Contoh 2 — Menjumlahkan angka 1–n**

```go
var n, total int
fmt.Print("Masukkan n: ")
fmt.Scanln(&n)

for i := 1; i <= n; i++ {
    total += i
}
fmt.Println("Total:", total)
```

**Contoh 3 — Pola bintang**

```go
for i := 1; i <= 5; i++ {
    for j := 1; j <= i; j++ {
        fmt.Print("*")
    }
    fmt.Println()
}
```
