# Modul 12 - While-Loop

## 12.1 Paradigma Perulangan

**Perulangan (loop)** adalah struktur kontrol yang memungkinkan suatu instruksi dijalankan **secara berulang-ulang**. Tanpa perulangan, sebuah instruksi harus ditulis berkali-kali sehingga kode menjadi panjang dan tidak efisien.

Pada modul sebelumnya (for-loop), kita mempelajari perulangan yang jumlah iterasinya sudah diketahui. Namun pada banyak kasus nyata, kita tidak mengetahui jumlah pengulangan sejak awal. Inilah yang disebut **perulangan berbasis kondisi**.

**Contoh perulangan berbasis kondisi dalam kehidupan sehari-hari
**

- “Menulis selama tinta pena masih ada.”
  Kondisi perulangan: tinta masih ada

- “Saya makan selama saya masih lapar.”
  Kondisi perulangan: masih terasa lapar

**Penting: Pastikan kondisi perulangan suatu saat dapat bernilai false.
Jika tidak, program akan mengalami infinite loop dan tidak pernah berhenti.**

**Jenis perulangan berbasis kondisi**

1. while-loop
2. repeat-until (dibahas pada modul berikutnya)

## 12.2 Karakteristik While-Loop

While-loop menggunakan dua komponen utama:

**s1. Kondisi (condition)**

Kondisi harus menghasilkan nilai boolean: true atau false.
Selama kondisi bernilai true, perulangan akan terus berjalan.

**2. Aksi (body / statements)**

Aksi adalah instruksi-instruksi yang dieksekusi berulang.
Di dalam aksi harus ada perubahan yang dapat membuat kondisi menjadi false, agar loop berhenti.

Jika kondisi tidak pernah berubah menjadi false → **infinite loop.**

## 12.3 Notasi While-Loop

### Pseudocode

```text
while <kondisi> do
    // aksi
endwhile

```

### Notasi di Bahasa Go

Walaupun Go tidak memiliki keyword while, ia menggunakan for dengan cara yang sama seperti while-loop:

```go
for kondisi {
    // aksi
}
```

## 12.4 Contoh Implementasi While-Loop di Go

Program:
Menerima dua bilangan dari pengguna, lalu menampilkan hasil penjumlahannya **selama hasil penjumlahannya genap.**

Jika hasil penjumlahan ganjil → perulangan berhenti.

**Kode Go**

```go
// filename: whileloop1.go
package main
import "fmt"

func main() {
    var a int
    var b int

    fmt.Scan(&a, &b)

    // while (a + b) % 2 == 0
    for (a + b) % 2 == 0 {
        fmt.Println("Hasil penjumlahan", a+b)
        fmt.Scan(&a, &b)
    }

    fmt.Println("Program selesai")
}
```

Penjelasan

- Kondisi while-loop adalah (a + b) % 2 == 0
  → berarti perulangan berlangsung selama hasilnya genap

- Jika hasilnya ganjil, kondisi menjadi false dan loop berhenti.

- Program menampilkan pesan Program selesai setelah loop berhenti.

### 12.5 Kesimpulan

- While-loop digunakan ketika jumlah iterasi tidak diketahui sejak awal.

- Loop berjalan selama kondisi bernilai true.

- Pastikan terdapat instruksi yang dapat mengubah kondisi agar loop tidak berjalan selamanya.

- Di bahasa Go, while-loop ditulis menggunakan keyword for dengan hanya kondisi (tanpa inisialisasi dan increment).
