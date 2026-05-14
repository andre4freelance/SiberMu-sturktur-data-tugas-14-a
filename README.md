# Tugas Praktek 14 - Konversi Bilangan menggunakan Stack

Tugas ini merupakan implementasi struktur data **Stack (Tumpukan)** menggunakan bahasa C untuk mengonversi bilangan dari basis Desimal (Basis 10) ke basis bilangan lainnya, yaitu:
1. **Biner** (Basis 2)
2. **Oktal** (Basis 8)
3. **Heksadesimal** (Basis 16)

## Struktur Program

Program ini mengimplementasikan stack menggunakan tipe data `struct` berisi array (statis) dengan batas maksimal elemen sebanyak `300`. Fungsi dasar stack yang dibuat pada kode ini meliputi:
- `initializestack()`: Menginisialisasi stack.
- `push()`: Menambahkan elemen ke posisi paling atas pada tumpukan.
- `pop()`: Mengambil dan menghapus elemen teratas dari tumpukan.
- `empty()`: Memeriksa apakah tumpukan dalam keadaan kosong.
- `full()`: Memeriksa apakah tumpukan dalam keadaan penuh.

## Cara Kerja

Program akan meminta pengguna untuk menginputkan sebuah bilangan bulat (desimal). Selanjutnya, pengguna dapat memilih menu konversi. 
Proses konversi dilakukan dengan cara membagi bilangan desimal dengan basis tujuan (2 untuk biner, 8 untuk oktal, 16 untuk heksadesimal) secara berulang hingga bilangannya menjadi 0. Sisa bagi (*modulus*) dari setiap pembagian tersebut kemudian dimasukkan (`push`) ke dalam stack. 

Terakhir, isi stack dikeluarkan (`pop`) satu persatu untuk menampilkan hasil konversi. Karena prinsip stack adalah LIFO (*Last In First Out*), angka sisa bagi yang terakhir dimasukkan akan menjadi angka pertama yang dicetak, yang mana sesuai dengan aturan matematika konversi bilangan. Khusus untuk bilangan Heksadesimal, angka 10 hingga 15 akan diganti dengan karakter huruf A hingga F.

## Cara Menjalankan Program (Kompilasi)

Untuk menjalankan program ini di lingkungan Linux, macOS, atau WSL, ikuti langkah berikut di terminal/CLI:

1. Pastikan Anda sudah menginstal *compiler* C (seperti `gcc`).
2. Buka terminal di dalam folder proyek ini.
3. Lakukan kompilasi file kode sumber `main.c`:
   ```bash
   gcc main.c -o main
   ```
4. Jalankan program hasil kompilasi:
   ```bash
   ./main
   ```

## Contoh Menu Program

Ketika dijalankan, program akan menampilkan menu antarmuka seperti berikut:
```text
-------konversi desimal ke biner oktal dan heksadesimal------

masukkan bilangan desimal = 255

---MENU---
1 untuk konversi ke biner
2 untuk konversi ke oktal
3 untuk konversi ke heksa
4 untuk keluar

pilih : 
```
