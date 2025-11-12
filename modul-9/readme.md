# 🧠 MODUL 9 — If-Then

## 9.1 Paradigma Percabangan

Sebelumnya telah dipelajari bahwa setiap baris kode program akan dieksekusi secara sekuensial, artinya dari baris pertama hingga baris terakhir akan dijalankan satu per satu.

Namun, bagaimana jika kita ingin hanya baris tertentu yang dijalankan berdasarkan syarat atau kondisi tertentu?
Misalnya: kita hanya ingin baris pertama dan terakhir saja yang dijalankan jika suatu kondisi terpenuhi.

Untuk hal ini, dalam pemrograman terdapat struktur kontrol percabangan, salah satunya yaitu if-then.

## 9.2 Karakteristik If-Then

Struktur kontrol if-then pada dasarnya terdiri dari dua bagian utama:

### 1. Kondisi (Condition)

- Merupakan syarat atau ketentuan dari percabangan.

- Harus bernilai boolean (true atau false).

- Dapat berupa variabel boolean atau ekspresi logika.

### 2. Aksi (Action)

- Sekumpulan instruksi yang dijalankan hanya jika kondisi bernilai true.

- Artinya, aksi tidak akan dijalankan secara default, melainkan harus memenuhi syarat tertentu.

## 🧩 Contoh Penulisan

🔹 Dalam Pseudocode

```plaintext
if kondisi then
    // aksi
endif

```

🔹 Dalam Bahasa Go

```go
if kondisi {
    // aksi
}

```

⚙️ Penulisan aksi biasanya diberi tab atau 4 spasi agar lebih mudah dibaca dan terlihat jelas bagian mana yang merupakan aksi.

### 9.3 Implementasi Menggunakan Go

Sebagai contoh, kita ingin membuat program yang akan menampilkan hasil pembagian **(a/b).**
Namun, hasil pembagian **hanya akan ditampilkan jika pembagi (b) tidak bernilai 0.**

```go
// filename: ifthen1.go
package main

import "fmt"

func main() {
    var a, b, hasil float64

    fmt.Scan(&a, &b)

    if b != 0 {
        hasil = a / b
        fmt.Println("Hasil pembagian adalah", hasil)
    }

    fmt.Println("Program selesai")
}
```

### 💻 Contoh Output

🔹 Input 1:

```bash
5 2

```

🔹 Output 1:

```nginx
Hasil pembagian adalah 2.5
Program selesai
```

🔹 Input 2:

```bash
5 0

```

🔹 Output 2:

```nginx
Program selesai
```

#### 🧩 Penjelasan

Baris ke-10 dan 11 (hasil = a / b dan fmt.Println(...))
hanya dieksekusi jika kondisi b != 0 bernilai true.

Saat b = 2, kondisi terpenuhi → hasil pembagian ditampilkan.

Saat b = 0, kondisi tidak terpenuhi → aksi diabaikan, program langsung selesai.

#### 💡 Kesimpulan

Struktur if-then digunakan untuk membuat keputusan logis dalam program.
Program akan mengeksekusi blok kode tertentu hanya jika kondisi terpenuhi.
Dengan demikian, programmer dapat mengontrol alur eksekusi program secara fleksibel.

### Latihan

Tulislah program Go untuk memeriksa apakah sebuah bilangan adalah bilangan positif.
Gunakan struktur if-then untuk menampilkan pesan berikut:

- Jika positif → tampilkan "Bilangan positif"

- Jika nol → tampilkan "Bilangan nol"

- Jika negatif → tampilkan "Bilangan negatif"

#### 🏁 Output yang Diharapkan

```bash
Masukkan angka: -5
Bilangan negatif

Masukkan angka: 0
Bilangan nol

Masukkan angka: 7
Bilangan positif
```
