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
