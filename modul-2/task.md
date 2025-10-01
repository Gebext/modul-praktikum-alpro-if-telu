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

### 2️⃣ Program Biodata Mahasiswa

**Instruksi:**

- Buat program untuk membaca **nama, NIM, dan kelas** dari input pengguna.
- Tampilkan **resume singkat** mahasiswa berdasarkan input.
- Tidak ada batasan khusus untuk format resume, silakan berkreasi.

---

#### 📝 Masukan

```plaintext
Bima
1124431414
IF-48-GAB
```

#### 📝 Keluaran

```Perkenalkan saya adalah Bima, salah satu mahasiswa Prodi S1-IF dari kelas IF-48-GAB dengan NIM 1124431414.

```

#### 📝 Masukan

```plaintext
Yura
1324234545
IFX-48-12
```

#### 📝 Keluaran

```Perkenalkan saya adalah Yura, salah satu mahasiswa Prodi S1-IF dari kelas IFX-48-12 dengan NIM 1324234545.

```
