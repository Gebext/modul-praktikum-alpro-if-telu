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

### 2️⃣ Memeriksa Tahun Kabisat

## Deskripsi Soal

Buatlah program dalam bahasa **Go** untuk memeriksa apakah sebuah tahun merupakan **tahun kabisat**.

- **Syarat tahun kabisat**:
  1. Tahun habis dibagi 400, atau
  2. Tahun habis dibagi 4 tetapi **tidak habis dibagi 100**.
- **Input**: Sebuah bilangan bulat (tahun)
- **Output**: `true` jika tahun kabisat, `false` jika bukan

### Contoh Input/Output

| No  | Input Tahun | Keluaran Kabisat |
| --- | ----------- | ---------------- |
| 1   | 2016        | true             |
| 2   | 2000        | true             |
| 3   | 2018        | false            |

---

# Modul 3.3 – Contoh Soal: Konversi Temperatur

## Deskripsi Soal

Buatlah program dalam bahasa **Go** untuk mengubah temperatur dari **Celsius** ke:

- Reamur (°R)
- Fahrenheit (°F)
- Kelvin (K)

### Rumus Konversi

- Fahrenheit:  
  \[
  F = C \times \frac{9}{5} + 32
  \]
- Reamur:  
  \[
  R = C \times \frac{4}{5}
  \]
- Kelvin:  
  \[
  K = C + 273
  \]

- **Input**: Bilangan riil (temperatur dalam Celsius)
- **Output**: Temperatur dalam Reamur, Fahrenheit, dan Kelvin

### Contoh Input/Output

```plaintext
Temperatur Celsius: <u>50</u>
Derajat Reamur: 40
Derajat Fahrenheit: 122
Derajat Kelvin: 323
```
