# Program Phonebook Menggunakan BST
## Deskripsi Singkat
Program ini adalah implementasi struktur data **Binary Search Tree (BST)** dalam membangun sistem phonebook digital yang mampu menyimpan, mencari, memperbarui, dan menghapus kontak secara efisien. Pengguna berinteraksi melalui menu pilihan dan program akan memproses setiap operasi dengan cara menelusuri pohon secara rekursif berdasarkan urutan alfabet nama kontak.

Program menerapkan struktur data **Tree** dengan dua kelas utama yaitu kelas Node sebagai cetak biru setiap simpul yang menyimpan nama, nomor telepon, serta pointer ke anak kiri dan anak kanan, dan kelas PhonebookBST sebagai pohon utama yang mengelola seluruh operasi. Setiap kontak yang ditambahkan akan ditempatkan ke posisi yang tepat dalam pohon, nama yang lebih kecil secara alfabet masuk ke kiri dan nama yang lebih besar masuk ke kanan, sehingga pohon selalu terurut secara alfabetis tanpa perlu proses pengurutan tambahan.
Program juga menerapkan tiga metode utama BST yaitu insert untuk menambah atau memperbarui kontak, search untuk mencari kontak dengan menelusuri pohon dari akar hingga simpul yang cocok ditemukan, dan delete yang menangani tiga kasus penghapusan yaitu simpul daun tanpa anak, simpul dengan satu anak, serta simpul dengan dua anak menggunakan teknik in-order successor. Selain itu metode tampilkan_kontak menggunakan teknik In-Order Traversal yaitu menelusuri anak kiri terlebih dahulu lalu simpul saat ini kemudian anak kanan, sehingga seluruh kontak otomatis ditampilkan secara urut dari A sampai Z. Program juga dilengkapi Input Validation menggunakan blok try-except untuk memastikan pengguna selalu memasukkan input yang valid pada setiap operasi.

## Source Code
<img width="933" height="525" alt="Cuplikan layar 2026-05-25 110915" src="https://github.com/user-attachments/assets/18a235b5-8b5b-4ed5-bd3d-5e31947c055a" />
<img width="925" height="572" alt="Cuplikan layar 2026-05-25 110947" src="https://github.com/user-attachments/assets/cea52cad-5bdf-43b9-9f89-9a5c7e53b083" />
<img width="945" height="525" alt="Cuplikan layar 2026-05-25 111011" src="https://github.com/user-attachments/assets/cc75fedf-44fc-40ea-b452-c6162e2c8e81" />
<img width="786" height="436" alt="Cuplikan layar 2026-05-25 111030" src="https://github.com/user-attachments/assets/21388da6-391f-49a3-b905-d05945810aa4" />

Baris 1   : Mendefinisikan kelas Node sebagai cetak biru untuk setiap simpul dalam BST  

Baris 2   : Mendefinisikan konstruktor kelas Node dengan parameter nama dan nomor_telepon  

Baris 3   : Menginisialisasi self.nama untuk menyimpan nilai parameter nama pada objek simpul  

Baris 4   : Menginisialisasi self.nomor_telepon untuk menyimpan nilai parameter nomor_telepon pada objek simpul  

Baris 5   : Menginisialisasi self.left dengan nilai None karena simpul belum memiliki anak kiri  

Baris 6   : Menginisialisasi self.right dengan nilai None karena simpul belum memiliki anak kanan  

Baris 9   : Mendefinisikan kelas PhonebookBST sebagai struktur pohon biner pencarian utama  

Baris 10  : Mendefinisikan konstruktor kelas PhonebookBST tanpa parameter tambahan  

Baris 11  : Menginisialisasi self.root dengan nilai None sebagai tanda bahwa pohon masih kosong  

Baris 13  : Mendefinisikan metode insert_node untuk menyisipkan simpul baru secara rekursif  

Baris 14  : Mengecek apakah posisi simpul saat ini masih kosong atau belum terisi  

Baris 15  : Membuat dan mengembalikan simpul baru jika posisi saat ini masih kosong  

Baris 16  : Membandingkan nama secara huruf kecil untuk mengecek apakah nama lebih kecil dari simpul saat ini  

Baris 17  : Memanggil insert_node secara rekursif ke anak kiri dan menyimpan hasilnya ke root.left  

Baris 18  : Mengecek apakah nama lebih besar dari simpul saat ini untuk menentukan arah ke kanan  
 
Baris 19  : Memanggil insert_node secara rekursif ke anak kanan dan menyimpan hasilnya ke root.right  

Baris 20  : Masuk ke blok else apabila nama yang dimasukkan sudah ada dalam pohon  

Baris 21  : Memperbarui nomor telepon pada simpul yang sudah ada dengan nilai baru  

Baris 22  : Mencetak pesan pemberitahuan bahwa kontak sudah ada dan nomor teleponnya telah diperbarui  

Baris 23  : Mengembalikan simpul yang telah diproses agar struktur pohon tetap terhubung

Baris 25  : Mendefinisikan metode find_min_node untuk mencari simpul dengan nilai terkecil dalam subpohon  

Baris 26  : Menyimpan referensi simpul awal ke variabel current sebagai titik mulai penelusuran  

Baris 27  : Memulai perulangan while yang terus berjalan selama current dan anak kirinya tidak kosong  

Baris 28  : Memindahkan current ke anak kiri untuk terus menelusuri nilai terkecil  

Baris 29  : Mengembalikan simpul paling kiri yang merupakan nilai terkecil dalam subpohon

Baris 31  : Mendefinisikan metode delete_node untuk menghapus simpul tertentu dari pohon secara rekursif  

Baris 32  : Mengecek apakah simpul saat ini kosong yang berarti nama yang dicari tidak ditemukan  

Baris 33  : Mencetak pesan bahwa kontak yang ingin dihapus tidak ditemukan dalam pohon  

Baris 34  : Mengembalikan None karena simpul tidak ditemukan  

Baris 35  : Mengecek apakah nama lebih kecil dari simpul saat ini untuk meneruskan pencarian ke kiri  

Baris 36  : Memanggil delete_node secara rekursif ke anak kiri  

Baris 37  : Mengecek apakah nama lebih besar dari simpul saat ini untuk meneruskan pencarian ke kanan  

Baris 38  : Memanggil delete_node secara rekursif ke anak kanan  

Baris 39  : Masuk ke blok else apabila simpul yang akan dihapus telah ditemukan  

Baris 40  : Mengecek apakah simpul adalah daun yaitu tidak memiliki anak kiri maupun anak kanan  

Baris 41  : Mengembalikan None untuk menghapus simpul daun dari pohon  

Baris 42  : Mengecek apakah simpul hanya tidak memiliki anak kiri  

Baris 43  : Mengembalikan anak kanan sebagai pengganti simpul yang dihapus  

Baris 44  : Mengecek apakah simpul hanya tidak memiliki anak kanan  

Baris 45  : Mengembalikan anak kiri sebagai pengganti simpul yang dihapus  

Baris 46  : Masuk ke blok else apabila simpul memiliki dua anak sekaligus  

Baris 47  : Mencari simpul penerus yaitu nilai terkecil di subpohon kanan menggunakan find_min_node  

Baris 48  : Menyalin nama dari simpul penerus ke simpul yang akan dihapus  

Baris 49  : Menyalin nomor telepon dari simpul penerus ke simpul yang akan dihapus  

Baris 50  : Menghapus simpul penerus dari subpohon kanan secara rekursif  

Baris 51  : Mencetak pesan bahwa kontak telah berhasil dihapus dari phonebook  

Baris 52  : Mengembalikan simpul yang telah diproses agar struktur pohon tetap terhubung

Baris 54  : Mendefinisikan metode search_node untuk mencari simpul berdasarkan nama secara rekursif  

Baris 55  : Mengembalikan simpul saat ini jika kosong berarti tidak ditemukan atau jika nama cocok  

Baris 56  : Mengembalikan hasil pencarian yang bisa berupa simpul yang ditemukan atau None  

Baris 57  : Mengecek apakah nama yang dicari lebih kecil dari nama simpul saat ini  

Baris 58  : Memanggil search_node secara rekursif ke anak kiri jika nama lebih kecil  

Baris 59  : Memanggil search_node secara rekursif ke anak kanan jika nama lebih besar

Baris 61  : Mendefinisikan metode publik search sebagai pintu masuk utama untuk fitur pencarian kontak  

Baris 62  : Memanggil search_node mulai dari akar pohon dan mengembalikan hasilnya

Baris 64  : Mendefinisikan metode tampilkan_kontak untuk menampilkan semua kontak secara terurut A sampai Z  

Baris 65  : Mengecek apakah simpul saat ini tidak kosong sebelum melakukan penelusuran  

Baris 66  : Memanggil tampilkan_kontak secara rekursif ke anak kiri karena in-order traversal dimulai dari kiri  
  
Baris 67  : Mencetak nama dan nomor telepon simpul saat ini ke layar

Baris 68  : Memanggil tampilkan_kontak secara rekursif ke anak kanan sebagai langkah terakhir in-order traversal

Baris 71  : Mendefinisikan fungsi main sebagai titik masuk utama program  

Baris 72  : Membuat objek PhonebookBST baru dan menyimpannya ke variabel phonebook  

Baris 73  : Menginisialisasi variabel pilih dengan nilai 0 sebagai nilai awal pilihan menu  

Baris 74  : Memulai perulangan utama yang terus berjalan selama pilihan bukan angka 5  

Baris 75  : Mencetak pilihan menu nomor 1 yaitu Tambah atau Ubah Kontak  

Baris 76  : Mencetak pilihan menu nomor 2 yaitu Cari Kontak  

Baris 77  : Mencetak pilihan menu nomor 3 yaitu Hapus Kontak

Baris 78  : Mencetak pilihan menu nomor 4 yaitu Tampilkan Semua Kontak A sampai Z

Baris 79  : Mencetak pilihan menu nomor 5 yaitu Keluar dari program

Baris 81  : Memulai blok try untuk menangkap kemungkinan kesalahan input dari pengguna

Baris 82  : Meminta pengguna memasukkan angka pilihan menu dan mengubahnya ke tipe integer

Baris 83  : Menangkap kesalahan ValueError jika input yang dimasukkan bukan angka

Baris 84  : Mencetak pesan kesalahan bahwa input tidak valid

Baris 85  : Melanjutkan ke iterasi berikutnya dan kembali ke tampilan menu tanpa memproses pilihan

Baris 87  : Mengecek apakah pengguna memilih menu 1 yaitu Tambah atau Ubah Kontak 

Baris 88  : Memulai blok try untuk menangkap kesalahan saat pengguna memasukkan data kontak

Baris 89  : Meminta pengguna memasukkan nama kontak yang ingin disimpan

Baris 90  : Meminta pengguna memasukkan nomor telepon dan mengubahnya ke tipe integer

Baris 91  : Mengecek apakah nama dan nomor sudah terisi dan tidak kosong sebelum menyimpan

Baris 92  : Memanggil metode insert untuk menyimpan kontak baru ke dalam pohon

Baris 93  : Mencetak pesan bahwa kontak berhasil disimpan ke phonebook

Baris 94  : Menangkap kesalahan ValueError jika nomor telepon yang dimasukkan bukan angka

Baris 95  : Mencetak pesan kesalahan bahwa input data kontak tidak valid

Baris 97  : Mengecek apakah pengguna memilih menu 2 yaitu Cari Kontak

Baris 98  : Meminta pengguna memasukkan nama kontak yang ingin dicari

Baris 99  : Memanggil metode search dan menyimpan hasilnya ke variabel hasil

Baris 100 : Mengecek apakah hasil pencarian ditemukan atau tidak None

Baris 101 : Mencetak detail kontak yang ditemukan berupa nama dan nomor telepon

Baris 102 : Masuk ke blok else apabila kontak tidak ditemukan dalam pohon

Baris 103 : Mencetak pesan bahwa kontak dengan nama tersebut tidak ada dalam phonebook

Baris 105 : Mengecek apakah pengguna memilih menu 3 yaitu Hapus Kontak

Baris 106 : Meminta pengguna memasukkan nama kontak yang ingin dihapus

Baris 107 : Memanggil metode delete untuk menghapus kontak dari pohon

Baris 109 : Mengecek apakah pengguna memilih menu 4 yaitu Tampilkan Semua Kontak

Baris 110 : Mengecek apakah pohon masih kosong sebelum menampilkan kontak

Baris 111 : Mencetak pesan bahwa phonebook masih kosong jika belum ada kontak tersimpan

Baris 112 : Masuk ke blok else apabila pohon sudah berisi setidaknya satu kontak

Baris 113 : Memanggil tampilkan_kontak mulai dari akar pohon untuk menampilkan seluruh kontak

Baris 115 : Mengecek apakah pengguna memilih menu 5 yaitu Keluar 

Baris 116 : Mencetak pesan bahwa program telah selesai

Baris 117 : Masuk ke blok else apabila input angka berada di luar rentang 1 sampai 5

Baris 118 : Mencetak pesan bahwa pilihan menu yang dimasukkan tidak tersedia

Baris 121 : Mengecek apakah file ini dijalankan langsung dan bukan diimpor sebagai modul

Baris 122 : Memanggil fungsi main untuk memulai jalannya program

## Output
<img width="783" height="570" alt="Cuplikan layar 2026-05-25 111153" src="https://github.com/user-attachments/assets/b26930c4-c998-49c3-9008-a09062bf9d65" />
<img width="678" height="237" alt="Cuplikan layar 2026-05-25 111207" src="https://github.com/user-attachments/assets/4bbb872f-60ae-48fe-9620-85a3813cb2d1" />

Berdasarkan output program di atas, pengguna pertama kali memilih menu 1 yaitu Tambah atau Ubah Kontak, kemudian memasukkan nama eka dengan nomor telepon 08989765. Program memanggil metode insert yang menelusuri pohon BST dan karena pohon masih kosong, simpul baru langsung dibuat sebagai akar, lalu menampilkan pesan "Kontak 'eka' berhasil disimpan".

Selanjutnya pengguna kembali memilih menu 1 dan memasukkan nama eka lagi dengan nomor telepon baru 0987532245. Karena nama eka sudah ada dalam pohon, program tidak membuat simpul baru melainkan langsung memperbarui nomor telepon pada simpul yang sudah ada. Program menampilkan dua pesan sekaligus yaitu "Kontak dengan nama 'eka' sudah ada. Nomor telepon diperbarui" dan "Kontak 'eka' berhasil disimpan", yang membuktikan bahwa metode insert_node menangani duplikasi nama dengan cara memperbarui data bukan menambah simpul baru.

Pengguna kemudian memilih menu 2 yaitu Cari Kontak dan memasukkan nama eka. Metode search_node menelusuri pohon mulai dari akar dan langsung menemukan kontak karena eka adalah satu-satunya simpul sekaligus akar pohon. Program menampilkan Nama: eka dan No. Telp: 987532245, dengan catatan angka 0 di depan tidak muncul karena nomor telepon disimpan sebagai tipe integer bukan string.

Pengguna lalu memilih menu 3 yaitu Hapus Kontak dan memasukkan nama eka. Metode delete_node menemukan simpul eka yang merupakan simpul daun tanpa anak kiri maupun kanan, sehingga simpul langsung dihapus dengan mengembalikan nilai None dan pohon kembali kosong.

Pada percobaan terakhir pengguna memilih menu 4 yaitu Tampilkan Semua Kontak, namun karena kontak eka sudah dihapus dan pohon kembali kosong, program menampilkan pesan "Phonebook masih kosong". Pengguna kemudian memilih menu 5 dan program menampilkan "Program selesai" lalu berhenti.
## Link Youtube
