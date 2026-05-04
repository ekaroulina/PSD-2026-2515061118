# Program Mengurutkan NPM
Program ini merupakan implementasi algoritma **Insertion Sort**. Program memungkinkan pengguna memasukkan sejumlah NPM, kemudian setiap NPM akan divalidasi agar hanya menerima input berupa angka dan harus terdiri dari tepat **10 digit**. Setelah seluruh data berhasil disimpan ke dalam list, program akan melakukan proses pengurutan NPM berdasarkan **3 digit terakhir** dari setiap NPM, bukan berdasarkan keseluruhan angka, sehingga urutan yang dihasilkan sesuai dengan kebutuhan identifikasi nomor urut mahasiswa dari kode belakang NPM. Dalam implementasinya, program menerapkan struktur data **List** sebagai media penyimpanan utama, menggunakan algoritma **Insertion Sort** sebagai metode pengurutan dengan teknik penyisipan elemen pada posisi yang sesuai, serta memanfaatkan operasi **modulus (%1000)** untuk mengambil tiga angka terakhir sebagai acuan pembanding. Selain itu, program juga dilengkapi dengan **Input Validation Algorithm** melalui kombinasi `try/except`, `while True`, dan pengecekan rentang nilai 10 digit agar data yang masuk dipastikan valid sebelum diproses ke tahap sorting.



# Source Code
<img width="787" height="509" alt="Cuplikan layar 2026-05-04 174400" src="https://github.com/user-attachments/assets/c9c11325-8fa5-4689-a5b6-ec10bb53c2d3" />
<img width="749" height="268" alt="Cuplikan layar 2026-05-04 175140" src="https://github.com/user-attachments/assets/7f82c34a-43d3-4a8f-8f7d-aae82aa87658" />
Baris 1 : Membuat fungsi insertion_sort(arr, n) yang digunakan untuk mengurutkan data NPM di dalam list.
Baris 2 : Membuat perulangan for dari index 1 sampai index terakhir array sebagai proses utama algoritma Insertion Sort.
Baris 3 : Menyimpan elemen array yang sedang diproses ke variabel temp sebagai data sementara yang akan disisipkan.
Baris 4 : Membuat variabel j = i - 1 untuk menunjuk elemen sebelum temp yang akan dibandingkan.
Baris 5 : Membuat perulangan while yang berjalan selama j >= 0 dan 3 digit terakhir arr[j] lebih besar dari 3 digit terakhir temp.
Baris 6 : Menggeser elemen arr[j] satu posisi ke kanan karena nilainya lebih besar.
Baris 7 : Mengurangi nilai j satu langkah ke kiri untuk membandingkan dengan elemen sebelumnya.
Baris 8 : Menyisipkan nilai temp ke posisi yang benar setelah proses pergeseran selesai.
Baris 9 : Membuat fungsi main sebagai fungsi utama jalannya program.
Baris 10 : Memulai blok try untuk menangkap kemungkinan error saat input jumlah NPM.
Baris 11 : Meminta user memasukkan jumlah NPM lalu mengubahnya menjadi bilangan bulat dan menyimpannya ke variabel n.
Baris 12 : Menangkap error ValueError jika user memasukkan selain angka.
Baris 13 : Menampilkan pesan "Input tidak valid!".
Baris 14 : Menghentikan program menggunakan return jika input jumlah NPM salah.
Baris 15 : Membuat list kosong arr = [] sebagai tempat menyimpan seluruh data NPM mahasiswa.
Baris 16 : Menampilkan pesan bahwa user harus memasukkan NPM 10 digit.
Baris 17 : Membuat perulangan for sebanyak jumlah NPM yang dimasukkan user.
Baris 18 : Membuat perulangan while True agar input akan terus diminta sampai benar.
Baris 19 : Memulai blok try untuk menangkap kemungkinan error saat input NPM.
Baris 20 : Meminta user memasukkan satu NPM lalu mengubahnya menjadi integer dan menyimpannya pada variabel nilai.
Baris 21 : Mengecek apakah NPM kurang dari 10 digit atau lebih dari 10 digit.
Baris 22 : Menampilkan pesan "NPM harus terdiri dari 10 digit, silakan input lagi!" jika NPM tidak valid.
Baris 23 : Jika NPM valid maka program masuk ke blok else.
Baris 24 : Menambahkan NPM yang valid ke dalam list arr menggunakan append().
Baris 25 : Menghentikan perulangan while True agar lanjut ke input NPM berikutnya.
Baris 26 : Menangkap error ValueError jika user memasukkan huruf atau simbol saat input NPM.
Baris 27 : Menampilkan pesan "Input tidak valid, silakan masukkan angka!".
Baris 28 : Menampilkan seluruh isi list NPM sebelum dilakukan pengurutan.
Baris 29 : Memanggil fungsi insertion_sort(arr, n) untuk memulai proses sorting data.
Baris 30 : Menampilkan teks "NPM setelah diurutkan (Insertion Sort):" sebagai output hasil.
Baris 31 : Membuat perulangan for untuk menampilkan NPM yang sudah terurut satu per satu.
Baris 32 : Mencetak isi array hasil sorting dalam satu baris.
Baris 33 : Memberikan baris kosong setelah output selesai ditampilkan.
Baris 34 : Mengecek apakah file Python dijalankan langsung.
Baris 35 : Memanggil fungsi main agar seluruh program dieksekusi.

#Output
<img width="861" height="213" alt="Cuplikan layar 2026-05-04 174330" src="https://github.com/user-attachments/assets/f6ede017-5aec-4c26-b43b-7e546aa8fda6" />
