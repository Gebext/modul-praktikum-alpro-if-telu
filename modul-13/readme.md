# Modul 13 — Repeat-Until

## 13.1 Paradigma Repeat-Until

Repeat-Until adalah bentuk perulangan yang termasuk dalam kategori loop berbasis kondisi, mirip dengan while-loop.
Namun berbeda dengan while-loop yang mengecek kondisi di awal, repeat-until justru mengecek kondisi di akhir.

▶ **Repeat-Until selalu menjalankan aksi minimal satu kali**, karena kondisi diperiksa setelah blok perulangan dijalankan.

Struktur ini umum ditemukan pada banyak pseudocode, meskipun beberapa bahasa pemrograman (termasuk Go) tidak memiliki keyword repeat atau until. Namun konsepnya tetap bisa diimplementasikan menggunakan for atau while.

## 13.2 Karakteristik Repeat-Until

Repeat-until memiliki dua komponen:

### 1. Aksi (body / statements)

Perintah-perintah yang akan selalu dieksekusi minimal satu kali.

### 2. Kondisi berhenti

Berbeda dengan while-loop yang berjalan selama kondisi true,
repeat-until berhenti saat **kondisi bernilai true**.

Dengan kata lain:

- Repeat-until terus berjalan selama kondisi bernilai false

- Repeat-until berhenti ketika kondisi bernilai true

## 13.3 Perbandingan dengan While-Loop

| Struktur         | Waktu pemeriksaan kondisi | Berhenti ketika | Karakter                               |
| ---------------- | ------------------------- | --------------- | -------------------------------------- |
| **While-loop**   | di awal                   | kondisi = false | aksi bisa tidak dijalankan sama sekali |
| **Repeat-until** | di akhir                  | kondisi = true  | aksi dijalankan minimal satu kali      |

## 13.4 Notasi Repeat-Until

Pseudocode

```text
repeat
    // aksi
until <kondisi bernilai true>

```

Interpretasi:
→ Ulangi aksi sampai kondisi terpenuhi (true).

## 13.5 Implementasi Repeat-Until di Bahasa Go

Karena Go tidak memiliki perintah repeat-until, kita dapat mensimulasikannya menggunakan:

**a) while-loop (for + kondisi)**

Dengan cara mengeksekusi aksi sekali di awal, lalu looping dengan syarat kebalikan dari kondisi.

**b) infinite loop + break**

Ini lebih mirip dengan repeat-until asli:

```go
for {
    // aksi
    if kondisi {
        break
    }
}
```

Konsep ini paling mendekati repeat-until karena kondisi dicek di akhir.

## 13.6 Contoh Implementasi Repeat-Until

**
Masalah:**
Minta pengguna memasukkan angka.
Ulangi sampai pengguna memasukkan angka negatif.

**Pseudocode**

```text
repeat
    input x
    print x
until x < 0

```

**Versi Go (simulasi repeat-until)
**

```go
package main
import "fmt"

func main() {
    var x int

    for {
        fmt.Scan(&x)
        fmt.Println("Anda memasukkan:", x)

        // kondisi berhenti: jika x < 0
        if x < 0 {
            break
        }
    }

    fmt.Println("Program selesai")
}
```

## 13.7 Contoh Lain: Validasi Input

**Masalah:**
Minta pengguna memasukkan password.
Ulangi sampai password benar.

**Pseudocode**

```text
repeat
    input pass
until pass = "kopi123"

```

**Versi Go
**

```go
package main
import "fmt"

func main() {
    var x int

    for {
        fmt.Scan(&x)
        fmt.Println("Anda memasukkan:", x)

        // kondisi berhenti: jika x < 0
        if x < 0 {
            break
        }
    }

    fmt.Println("Program selesai")
}
```

## 13.7 Contoh Lain: Validasi Input

**Masalah:**
Minta pengguna memasukkan password.
Ulangi sampai password benar.

**Pseudocode**

```text
repeat
    input pass
until pass = "kopi123"

```

**Versi Go**

```go
package main
import "fmt"

func main() {
    var pass string

    for {
        fmt.Print("Masukkan password: ")
        fmt.Scan(&pass)

        if pass == "kopi123" {
            break
        }
        fmt.Println("Salah! Coba lagi.")
    }

    fmt.Println("Login berhasil!")
}
```

## 13.8 Kelebihan dan Kekurangan Repeat-Until

**Kelebihan**

- Aksi selalu dijalankan minimal satu kali.

- Lebih mudah digunakan untuk validasi input.

- Cocok ketika harus menjalankan aksi dahulu sebelum mengecek kondisi.

**Kekurangan**

- Tidak semua bahasa memiliki struktur aslinya.

- Kadang sulit diubah ke bentuk while-loop jika logikanya kompleks.

- Jika kondisi akhir tidak direncanakan dengan baik → infinite loop.

## 13.9 Kesimpulan

- Repeat-Until adalah perulangan dengan pengecekan kondisi di akhir.

- Aksi dijalankan minimal satu kali sebelum kondisi diperiksa.

- Loop berhenti jika kondisi bernilai true.

- Di Go, repeat-until dapat disimulasikan menggunakan for { ... if kondisi { break } }.

- Sangat cocok digunakan untuk validasi atau proses yang harus dieksekusi setidaknya sekali.
