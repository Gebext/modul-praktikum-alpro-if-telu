## Soal Latihan Modul 2

### 1️⃣ Menghitung Nilai x dari Persamaan f(x)

## Deskripsi Soal

Buatlah program dalam bahasa **Go** untuk menghitung nilai \(x\) dari persamaan:

\[
f(x) = \frac{2}{x + 5} + 5
\]

- **Input**: Sebuah bilangan riil yang menyatakan \(f(x)\).
- **Output**: Sebuah bilangan riil yang menyatakan nilai \(x\).

Rumus kebalikan untuk mencari \(x\) dari \(f(x)\):

\[
x = \frac{2}{f(x) - 5} - 5
\]

### Contoh Masukan dan Keluaran

| No  | Masukan (f(x)) | Keluaran (x) |
| --- | -------------- | ------------ |
| 1   | 5.2            | 5            |
| 2   | 4.125          | 11           |

---

## Jawaban (Kode Go)

```go
package main

import "fmt"

func main() {
    var fx, x float64
    fmt.Print("Masukkan nilai f(x): ")
    fmt.Scan(&fx)

    x = 2/(fx - 5) - 5
    fmt.Println("Nilai x:", x)
}
```

### 2️⃣ Menghitung Volume dan Luas Permukaan Bola

## Deskripsi Soal

Buatlah program dalam bahasa **Go** untuk menghitung **volume** dan **luas permukaan (kulit)** bola berdasarkan jari-jari.

Rumus:

- **Volume bola**:  
  \[
  V = \frac{4}{3} \pi r^3
  \]
- **Luas permukaan bola**:  
  \[
  A = 4 \pi r^2
  \]

Gunakan \(\pi \approx 3.1415926535\).

- **Input**: Bilangan bulat (jari-jari bola)
- **Output**: Volume dan luas permukaan bola (bilangan desimal)

### Contoh Input/Output

```plaintext
Jejari = 5
Bola dengan jejari 5 memiliki volume 523.5988 dan luas kulit 314.1593
```
