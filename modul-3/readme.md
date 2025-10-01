# MODUL 3. I/O, TIPE DATA & VARIABEL (LATIHAN 1)

Modul ini merupakan kelanjutan dari modul sebelumnya. Fokus dari Modul 3 adalah pendalaman materi dari Modul 2.  
Materi di modul ini bersifat tambahan dan dibahas secara khusus, tetapi bukan menjadi materi utama untuk soal-soal di modul ini.  
Soal yang diberikan tetap serupa dengan modul sebelumnya, yaitu seputar input/output, tipe data, dan variabel.

---

## 3.1 Integer Division (Div) dan Modulo (Mod)

Pembagian pada tipe data integer (integer division atau div) sedikit berbeda dengan pembagian biasa.

- Hasil pembagian integer akan bertipe integer, sehingga bagian pecahan (floating point) diabaikan.
- Hasil pembagian integer disebut **quotient**.

Contoh:

- 10 ÷ 3 = 3.333...
- Hasil integer division = 3

### Contoh kode Go:

```go
package main
import "fmt"

func main() {
    var bil_1 int = 10
    var bil_2 int = 3
    var hasil = bil_1 / bil_2
    fmt.Println(hasil) // output: 3
}
```

Operator Modulo

Modulo (atau mod) adalah operasi untuk mencari sisa pembagian pada integer division.

Contoh:

10 mod 3 = 1

Contoh kode Go:

```go
package main
import "fmt"

func main() {
var bil_1 int = 10
var bil_2 int = 3
var hasil = bil_1 % bil_2
fmt.Println(hasil) // output: 1
}
```

Contoh penerapan: mencari digit bilangan

Setiap bilangan jika di-modulus dengan 10 → menghasilkan digit terakhir.

1234 mod 10 = 4

5677 mod 10 = 7

Jika dibagi 10 (div), digit terakhir akan hilang:

1234 div 10 = 123

5677 div 10 = 567

Contoh: X = 2357

---

| i   | Digit ke-i | Operasi             | Keterangan                       |
| --- | ---------- | ------------------- | -------------------------------- |
| 1   | 2          | (X div 1000) mod 10 | X div 1000 = 2 (tidak perlu mod) |
| 2   | 3          | (X div 100) mod 10  | X div 100 = 23 → mod 10 = 3      |
| 3   | 5          | (X div 10) mod 10   | X div 10 = 235 → mod 10 = 5      |
| 4   | 7          | (X div 1) mod 10    | X div 1 = 2357 → mod 10 = 7      |

---

## 3.2 Casting atau Konversi Tipe Data

Di bahasa Go, tipe data bersifat statis → tipe data variabel tidak bisa diubah saat program berjalan.
Namun, kita bisa menggunakan casting untuk mengubah tipe data.

```go
package main
import "fmt"

func main() {
    var pi float64 = 3.14
    var nilai int = int(pi) // hasil: 3
    fmt.Println(nilai)
}
```

Format casting di Go:

```java
var var_name data_type = data_type(value)
```
