# MODUL 3. I/O, TIPE DATA & VARIABEL (LATIHAN 1)

Modul ini merupakan kelanjutan dari Modul 2.  
Fokus dari Modul 3 adalah pendalaman materi dari Modul 2.  
Materi di modul ini bersifat tambahan dan dibahas secara khusus, tetapi bukan menjadi materi utama.  
Soal yang diberikan tetap seputar input/output, tipe data, dan variabel.

---

## 3.1 Integer Division (Div) dan Modulo (Mod)

Pembagian pada tipe data integer (integer division atau `div`) berbeda dengan pembagian biasa:

- Hasil pembagian integer akan bertipe **integer**, sehingga bagian pecahan (desimal) diabaikan.
- Hasil pembagian integer disebut **quotient**.

**Contoh:**

- 10 ÷ 3 = 3.333...
- 10 div 3 = 3

### Contoh kode Go (Integer Division)

```go
package main
import "fmt"

func main() {
    var bil_1 int = 10
    var bil_2 int = 3
    var hasil = bil_1 / bil_2
    fmt.Println(hasil) // output: 3
}

Operator Modulo

Modulo (%) digunakan untuk mencari sisa pembagian.

Contoh:

    10 mod 3 = 1

Contoh kode Go (Modulo)

package main
import "fmt"

func main() {
    var bil_1 int = 10
    var bil_2 int = 3
    var hasil = bil_1 % bil_2
    fmt.Println(hasil) // output: 1
}

Penerapan: Mencari Digit Bilangan

    Bilangan mod 10 → menghasilkan digit terakhir.

    Bilangan div 10 → menghilangkan digit terakhir.

Contoh:

    1234 mod 10 = 4

    5677 mod 10 = 7

    1234 div 10 = 123

    5677 div 10 = 567

Contoh tabel digit bilangan (X = 2357)
i	Digit ke-i	Operasi	Keterangan
1	2	(X div 1000) mod 10	X div 1000 = 2 (tidak perlu mod)
2	3	(X div 100) mod 10	X div 100 = 23 → mod 10 = 3
3	5	(X div 10) mod 10	X div 10 = 235 → mod 10 = 5
4	7	(X div 1) mod 10	X div 1 = 2357 → mod 10 = 7
3.2 Casting (Konversi Tipe Data)

Di bahasa Go, tipe data bersifat statis, artinya tipe data variabel tidak bisa diubah saat program berjalan.
Namun, kita bisa menggunakan casting untuk konversi antar tipe data.
Contoh kode Go (Float → Int)

package main
import "fmt"

func main() {
    var pi float64 = 3.14
    var nilai int = int(pi) // hasil: 3
    fmt.Println(nilai)
}

Format Casting di Go

var nama_variabel tipe_data = tipe_data(nilai)

Casting String ↔ Integer dengan strconv
1. String → Integer

package main
import (
    "fmt"
    "strconv"
)

func main() {
    var teks string = "2024"
    tahun, err := strconv.Atoi(teks)
    if err == nil {
        fmt.Println(tahun) // output: 2024
    }
}

2. Integer → String

package main
import (
    "fmt"
    "strconv"
)

func main() {
    var bilangan int = 113071049
    var teks string = strconv.Itoa(bilangan)
    fmt.Println(teks) // output: "113071049"
}

Ringkasan

Integer Division & Modulo:
- Digunakan untuk pembagian integer dan mencari sisa pembagian.

Casting:
- Konversi antar tipe data.
- Contoh: float → int, string ↔ int (dengan strconv).
```
