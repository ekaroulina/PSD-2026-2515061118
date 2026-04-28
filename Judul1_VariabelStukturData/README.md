# Program Nilai Ujian Mahasiswa
# Penjelasan Singkat
Program ini adalah implementasi list 1D dalam manajemen nilai ujian siswa yang memungkinkan pengguna menyimpan dan mengelola nilai ujian untuk 5 mata pelajaran yaitu Matematika, Bahasa Indonesia, IPA, IPS, dan Bahasa Inggris. Pengguna dapat memasukkan nilai (0–100) untuk setiap mata pelajaran dan program otomatis menghitung rata-ratanya, serta dilengkapi fitur untuk melihat alamat memori (address) dari array nilai baik secara keseluruhan maupun per index yang berguna untuk memahami cara Python menyimpan data di memori komputer. Dalam implementasinya, program menerapkan struktur data List sebagai inti penyimpanan, dengan algoritma Sequential Traversal menggunakan `for i in range(5)` untuk menelusuri tiap elemen, serta Input Validation Algorithm melalui kombinasi `try/except` dan `while True` yang memastikan setiap data yang dimasukkan selalu valid sebelum disimpan ke dalam array.
# Source Code
<img width="702" height="612" alt="Cuplikan layar 2026-04-28 183620" src="https://github.com/user-attachments/assets/77f31ba5-ed0b-43c6-b4fa-1c16a8766892" />
<img width="734" height="306" alt="Cuplikan layar 2026-04-28 183642" src="https://github.com/user-attachments/assets/8bc3c614-1fbb-4c49-90ef-3984c8a5435b" />
Baris 1 : Membuat fungsi menu()
Baris 2 : Menampilkan judul program "=== PROGRAM NILAI UJIAN SISWA ==="
Baris 3 : Menampilkan opsi 1 (tampilkan address array nilai)
Baris 4 : Menampilkan opsi 2 (tampilkan address semua index array)
Baris 5 : Menampilkan opsi 3 (masukkan nilai ujian ke semua mata pelajaran)
Baris 6 : Menampilkan opsi 4 (keluar program)
Baris 7 : Membuat fungsi main() yang merupakan fungsi utama jalannya program
Baris 8 : Membuat list nilai berisi 5 elemen bernilai 0 sebagai tempat menyimpan nilai ujian
Baris 9 : Membuat list mata_pelajaran berisi nama 5 mata pelajaran
Baris 10 : Membuat variabel running bernilai True sebagai penanda program aktif
Baris 11 : Membuat perulangan while yang terus berjalan selama running bernilai True
Baris 12 : Memanggil fungsi menu() untuk menampilkan pilihan setiap putaran
Baris 13 : Memulai blok try untuk menangkap kemungkinan error input
Baris 14 : Meminta user mengetik pilihan dan menyimpannya sebagai angka bulat di variabel choice
Baris 15 : Menangkap error ValueError jika user mengetik bukan angka
Baris 16 : Menampilkan pesan error "Masukkan angka yang valid!"
Baris 17 : Kembali ke awal perulangan while menggunakan continue
Baris 18 : Mengecek apakah user memilih opsi 1
Baris 19 : Menampilkan alamat memori dari keseluruhan list nilai menggunakan id()
Baris 20 : Mengecek apakah user memilih opsi 2
Baris 21 : Memulai perulangan for sebanyak 5 kali (i = 0 sampai 4)
Baris 22 : Menampilkan index, nama mata pelajaran, dan alamat memori tiap elemen nilai
Baris 23 : Mengecek apakah user memilih opsi 3
Baris 24 : Menampilkan instruksi "Masukkan nilai ujian (0-100)"
Baris 25 : Memulai perulangan for luar untuk 5 mata pelajaran
Baris 26 : Memulai perulangan while dalam yang terus berjalan sampai input valid
Baris 27 : Memulai blok try untuk menangkap error input nilai
Baris 28 : Meminta user mengetik nilai mata pelajaran ke-i dan menyimpannya ke nilai[i]
Baris 29 : Mengecek apakah nilai yang dimasukkan berada di rentang 0 sampai 100
Baris 30 : Keluar dari perulangan while jika nilai valid menggunakan break
Baris 31 : Kondisi else jika nilai di luar rentang 0-100
Baris 32 : Menampilkan pesan "Nilai harus antara 0 dan 100!"
Baris 33 : Menangkap error ValueError jika input bukan angka
Baris 34 : Menampilkan pesan "Input tidak valid, silakan masukkan angka!"
Baris 35 : Menampilkan semua isi list nilai setelah seluruh nilai diisi
Baris 36 : Menghitung dan menampilkan rata-rata nilai dengan 1 angka desimal
Baris 37 : Mengecek apakah user memilih opsi 4
Baris 38 : Mengubah running menjadi False untuk menghentikan perulangan while
Baris 39 : Menampilkan pesan "Program selesai."
Baris 40 : Kondisi else jika user mengetik angka selain 1, 2, 3, atau 4
Baris 41 : Menampilkan pesan "Pilihan tidak valid!"
Baris 42 : Mengecek apakah file dijalankan langsung bukan sebagai modul import
Baris 43 : Memanggil fungsi main() untuk menjalankan program
# Output
<img width="470" height="347" alt="Cuplikan layar 2026-04-28 195408" src="https://github.com/user-attachments/assets/7698be99-e683-4640-a17f-96f647009a67" />
<img width="477" height="414" alt="Cuplikan layar 2026-04-28 195419" src="https://github.com/user-attachments/assets/b1caa331-f2c1-4608-ae60-1cc5d28d202c" />


