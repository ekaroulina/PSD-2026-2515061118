# Program Mencari Lagu dalam Playlist Lagu Menggunakan Binary Search
## Deskripsi
Program ini adalah implementasi algoritma **Binary Search** dalam pencarian judul lagu dari playlist berisi 11 lagu. Pengguna memasukkan judul lagu yang ingin dicari, lalu program menemukannya dengan cara membagi area pencarian menjadi dua bagian secara berulang hingga lagu ditemukan atau dipastikan tidak ada.
Program menerapkan struktur data List sebagai penyimpanan playlist yang diurutkan alfabetis menggunakan .sort() karena Binary Search hanya bekerja pada data terurut. Program juga dibuat dengan Input Validation menggunakan while True untuk memastikan pengguna selalu memasukkan input yang valid sebelum pencarian dimulai.

## Source Code
<img width="737" height="360" alt="Cuplikan layar 2026-05-11 114547" src="https://github.com/user-attachments/assets/38897f0f-01e1-45ce-9e61-4ae0d61c10ae" />
<img width="771" height="403" alt="Cuplikan layar 2026-05-11 115404" src="https://github.com/user-attachments/assets/2b4d3024-ed21-4ffb-b2bd-518bc02fb24d" />
<img width="716" height="353" alt="Cuplikan layar 2026-05-11 114704" src="https://github.com/user-attachments/assets/b78a755d-9d1e-4a12-a239-7f36368d5987" />


- Baris 1 : Mendefinisikan fungsi pencarian dengan parameter arr (playlist), n (jumlah lagu), dan target (judul yang dicari)  

- Baris 2 : Menginisialisasi pointer kiri di indeks pertama  

- Baris 3 : Menginisialisasi pointer kanan di indeks terakhir  

- Baris 4 : Menyimpan posisi hasil pencarian, default -1 berarti belum ditemukan
  
- Baris 5 : Perulangan yang berjalan selama jangkauan pencarian masih valid
  
- Baris 6 : Menghitung indeks tengah untuk menghindari overflow  

- Baris 7 : Menampilkan indeks dan judul lagu di posisi tengah  

- Baris 8 : Mengecek apakah lagu di posisi tengah cocok dengan target  

- Baris 9 : Menyimpan indeks penemuan ke variabel pos  

- Baris 10 : Menghentikan perulangan karena lagu sudah ditemukan  

- Baris 11 : Mengecek apakah judul tengah secara alfabet lebih awal dari target  

- Baris 12 : Menggeser pointer kiri, membuang separuh kiri dan melanjutkan pencarian di kanan  

- Baris 13 : Menggeser pointer kanan, membuang separuh kanan dan melanjutkan pencarian di kiri  

- Baris 14 : Mengembalikan posisi lagu, bernilai indeks jika ditemukan atau -1 jika tidak  

- Baris 15 : Mendefinisikan fungsi utama program  

- Baris 16 : Mendeklarasikan list berisi 11 judul lagu sebagai data playlist  

- Baris 17 : pMengurutkan playlist secara alfabetis, wajib dilakukan sebelum binary search  

- Baris 18 : Menyimpan jumlah total lagu ke variabel n  

- Baris 19 : Menampilkan judul program  

- Baris 20 : Menelusuri seluruh playlist beserta indeksnya  

- Baris 21 : Menampilkan indeks dan judul setiap lagu  

- Baris 22 : Perulangan validasi input yang terus berjalan sampai input valid  

- Baris 23 : Meminta input judul lagu dan membersihkan spasi di awal/akhir  

- Baris 24 : Menghentikan perulangan jika input tidak kosong  

- Baris 25 : Menampilkan pesan error jika input kosong  

- Baris 26 : Memanggil fungsi binary search dan menyimpan hasilnya  

- Baris 27 : Mengecek apakah lagu berhasil ditemukan  

- Baris 28 : Menampilkan indeks penemuan jika lagu ada  

- Baris 29 : Menampilkan pesan gagal jika lagu tidak ada  

- Baris 30 : Menjalankan main() hanya jika file dieksekusi langsung, bukan diimpor  

## Output
<img width="749" height="392" alt="Cuplikan layar 2026-05-11 114528" src="https://github.com/user-attachments/assets/fe7fbce2-f3af-4faf-b3da-8c1fcc428bf8" />

Berdasarkan output program di atas, pengguna memasukkan judul lagu yang ingin dicari yaitu "Mardua Holong". Program terlebih dahulu menampilkan seluruh isi playlist yang telah diurutkan secara alfabetis mulai dari indeks 0 hingga 10, mulai dari "Allah Peduli" sampai "When the Roll is Called Up Yonder".
Setelah input diterima, fungsi binary_search dijalankan. Pencarian dimulai dengan mengecek elemen tengah di indeks 5 yaitu "God Will Take Care of You", karena judul tersebut secara alfabet lebih awal dari "Mardua Holong" maka program membuang separuh kiri dan melanjutkan pencarian ke sisi kanan. Iterasi kedua mengecek elemen tengah baru di indeks 8 yaitu "Mardua Holong", dan judul tersebut cocok dengan target sehingga pencarian langsung berhenti. Program hanya membutuhkan 2 iterasi untuk menemukan lagu dari 11 data yang tersedia, yang membuktikan efisiensi algoritma Binary Search dibanding Sequential Search yang bisa membutuhkan hingga 9 pengecekan untuk data yang sama. Hasil akhir menampilkan bahwa lagu "Mardua Holong" berhasil ditemukan di indeks ke-8.
## Link Youtube
https://youtu.be/Mmb7XnKbzX4?si=ieQOgxv2bv8IuIyR

## Tugas Tambahan
<img width="1216" height="1280" alt="WhatsApp Image 2026-05-11 at 21 35 23" src="https://github.com/user-attachments/assets/6ad97183-7bd7-4e8f-b769-1e92c0646312" />




