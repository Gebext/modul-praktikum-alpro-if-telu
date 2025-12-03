## Tugas Terbimbing While-Loop

### Soal 1

**Judul**: Cetak Angka Genap dari 1 sampai N
**Deskripsi**:
Buat program yang menerima input sebuah bilangan N.
Tampilkan semua angka genap dari 1 sampai N menggunakan while-loop.

**Contoh Input:**

```text
10

```

**Contoh Output:**

```text
2 4 6 8 10

```

**Catatan:**
Tidak boleh menggunakan for-loop.

### Soal 2

**Judul**: Hitung Jumlah Angka hingga Input 0
**Deskripsi**:
Buat program yang terus menerima input angka dari pengguna.
Program akan terus berjalan menggunakan while-loop sampai pengguna memasukkan angka 0.

Program harus menghitung total penjumlahan semua angka yang dimasukkan (kecuali 0), lalu menampilkannya.

**Contoh Input:**

```text
5
3
7
0
```

**Contoh Output:**

```text
Total = 15

```

**Catatan:**
Gunakan kondisi while-loop untuk menghentikan saat angka 0 muncul.

### Soal 3s

**Judul**: Validasi Password + Limit Percobaan
**Deskripsi**:
Buat program login sederhana dengan ketentuan:

- Password benar adalah: "kopi123"

- Pengguna memiliki maksimal 3 kali percobaan

- Program menggunakan while-loop

- Jika password benar → tampilkan "Login sukses!"

- sJika salah 3 kali → tampilkan "Akses ditolak!" dan berhenti

**Contoh User:**

```pgsql
Input password: abc
Salah, coba lagi (sisa 2x)
Input password: tes
Salah, coba lagi (sisa 1x)
Input password: kopi123
Login sukses!

```

**Jika Gagal:**

```text
Input password: aaa
Input password: bbb
Input password: ccc
Akses ditolak!

```

**Catatan:**
Gunakan kombinasi while-loop + conditional (if-else) dan variabel counter.
