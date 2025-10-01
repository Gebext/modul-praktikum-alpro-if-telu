## Soal Latihan Modul 2

### 1️⃣ Telusuri Program

**Instruksi:**

- Kompilasi dan eksekusi program berikut.
- Masukkan data sesuai instruksi sebanyak yang diminta.
- Perhatikan keluaran yang diperoleh.
- Jelaskan apa yang sebenarnya dilakukan oleh program ini.

---

#### 📄 Program:

```go
package main

import "fmt"

func main() {
    var (
        satu, dua, tiga string
        temp string
    )

    fmt.Print("Masukan input string: ")
    fmt.Scanln(&satu)

    fmt.Print("Masukan input string: ")
    fmt.Scanln(&dua)

    fmt.Print("Masukan input string: ")
    fmt.Scanln(&tiga)

    fmt.Println("Output awal = " + satu + " " + dua + " " + tiga)

    temp = satu
    satu = dua
    dua = tiga
    tiga = temp

    fmt.Println("Output akhir = " + satu + " " + dua + " " + tiga)
}
```
