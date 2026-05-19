# Program Antrean Pemesanan Tiket Bioskop dengan Queue Array
## Deskripsi Singkat
Program ini adalah implementasi **Queue Array** untuk simulasi sistem antrean pelanggan bioskop. Pengguna dapat menambah pelanggan ke antrean, memanggil pelanggan untuk dilayani, serta melihat status antrean secara real-time. Program menerapkan logika VIP pelanggan yang Kode-nya mengandung angka 2 pada dua digit terakhir langsung mendapat kursi tanpa masuk antrean. Program menggunakan struktur data List sebagai penyimpanan antrean dengan metode .append() untuk enqueue dan .pop(0) untuk dequeue (FIFO), dilengkapi validasi kapasitas maksimal 10 pelanggan serta menu interaktif berbasis while True untuk operasi antrean secara berkelanjutan.

## Source Code
<img width="1057" height="597" alt="Cuplikan layar 2026-05-19 170920" src="https://github.com/user-attachments/assets/45b389fb-9f8b-4b6a-919a-482f37ebb363" />
<img width="1049" height="604" alt="Cuplikan layar 2026-05-19 171002" src="https://github.com/user-attachments/assets/5f9c7351-acd0-4579-a666-dd1945982fe8" />

### Penjelasan 

**Baris 1** : Mendefinisikan class QueueBioskop sebagai representasi sistem antrean bioskop

**Baris 2** : Mendefinisikan method konstruktor __init__ dengan parameter kapasitas (default 10) untuk mengatur batas maksimal antrean

**Baris 3** : Menginisialisasi self.queue sebagai list kosong yang akan menyimpan data pelanggan dalam antrean

**Baris 4** : Menginisialisasi self.kapasitas untuk menyimpan nilai batas maksimal antrean dari parameter

**Baris 5** : Menginisialisasi self.total_pelanggan dengan nilai 0 sebagai penghitung total pelanggan yang ada

**Baris 7** : Mendefinisikan method enqueue dengan parameter tiket_id untuk menambahkan pelanggan ke antrean

**Baris 8** : Mengecek apakah tiket_id mengandung angka "2" sebagai penanda pelanggan VIP menggunakan kondisi if

**Baris 9** : Mencetak pesan bahwa pelanggan VIP langsung mendapat kursi tanpa perlu masuk antrean

**Baris 10** : Menambah nilai self.total_pelanggan sebesar 1 untuk pelanggan VIP yang masuk

**Baris 11** : Masuk ke blok else apabila pelanggan bukan VIP (tiket_id tidak mengandung angka "2")

**Baris 12** : Mengecek apakah panjang antrean sudah mencapai atau melebihi kapasitas maksimal menggunakan kondisi if

**Baris 13** : Mencetak pesan bahwa kapasitas bioskop penuh jika kondisi pada Baris 12 terpenuhi

**Baris 14** : Menghentikan eksekusi method dengan return agar pelanggan tidak masuk antrean saat penuh

**Baris 16** : Menambahkan tiket_id pelanggan ke bagian paling belakang list self.queue menggunakan append

**Baris 17** : Mencetak pesan konfirmasi bahwa pelanggan berhasil masuk antrean

**Baris 18** : Menambah nilai self.total_pelanggan sebesar 1 untuk pelanggan reguler yang masuk antrean

**Baris 20** : Mendefinisikan method dequeue untuk melayani dan mengeluarkan pelanggan dari antrean

**Baris 21** : Mengecek apakah antrean tidak kosong menggunakan kondisi if sebelum melakukan proses pelayanan

**Baris 22** : Mengambil dan menghapus elemen pertama dari self.queue menggunakan pop(0) sesuai prinsip FIFO, lalu menyimpannya ke variabel pelanggan

**Baris 23** : Mengurangi nilai self.total_pelanggan sebesar 1 karena pelanggan sudah dilayani

**Baris 24** : Mencetak pesan bahwa pelanggan dipanggil untuk membeli tiket

**Baris 25** : Masuk ke blok else apabila antrean dalam kondisi kosong

**Baris 26** : Mencetak pesan bahwa antrean kosong sehingga tidak ada pelanggan yang bisa dilayani

**Baris 28** : Mendefinisikan method display untuk menampilkan informasi lengkap kondisi antrean saat ini

**Baris 29** : Mencetak jumlah total pelanggan di bioskop beserta kapasitas maksimal dengan keterangan VIP tidak dihitung antrean

**Baris 30** : Mengecek apakah antrean dalam kondisi kosong menggunakan kondisi if

**Baris 31** : Mencetak pesan "Antrean kosong" jika tidak ada pelanggan di antrean

**Baris 32** : Masuk ke blok else apabila antrean memiliki pelanggan

**Baris 33** : Mencetak daftar seluruh pelanggan dalam antrean dengan format A -> B -> C menggunakan join

**Baris 35** : Mendefinisikan method is_empty untuk mengecek apakah antrean kosong

**Baris 36** : Mengembalikan nilai True jika panjang self.queue sama dengan 0, dan False jika sebaliknya menggunakan return

**Baris 39** : Membuat objek bioskop dari class QueueBioskop dengan kapasitas 10 kursi

**Baris 41** : Memulai perulangan while True yang akan terus berjalan hingga pengguna memilih untuk keluar

**Baris 42** : Mencetak teks "Menu:" sebagai judul menu pilihan

**Baris 43** : Mencetak pilihan menu 1 untuk menambah pelanggan ke antrean

**Baris 44** : Mencetak pilihan menu 2 untuk melayani pelanggan

**Baris 45** : Mencetak pilihan menu 3 untuk melihat pelanggan pertama dalam antrean

**Baris 46** : Mencetak pilihan menu 4 untuk melihat pelanggan terakhir dalam antrean

**Baris 47** : Mencetak pilihan menu 5 untuk mengecek apakah antrean kosong

**Baris 48** : Mencetak pilihan menu 6 untuk melihat jumlah pelanggan dalam antrean

**Baris 49** : Mencetak pilihan menu 7 untuk keluar dari program

**Baris 51** : Membaca input pilihan menu dari pengguna dan menyimpannya ke variabel pilihan

**Baris 53** : Mengecek dengan kondisi if apakah pengguna memilih menu "1" untuk menambah pelanggan

**Baris 54** : Membaca input nama pelanggan dari pengguna

**Baris 55** : Membaca input NPM pelanggan dari pengguna

**Baris 56** : Membuat tiket_id dari 2 huruf pertama nama (huruf kapital) digabung 2 digit terakhir NPM

**Baris 57** : Memanggil method enqueue dengan tiket_id yang sudah dibuat untuk mendaftarkan pelanggan

**Baris 58** : Mengecek dengan kondisi elif apakah pengguna memilih menu "2" untuk melayani pelanggan

**Baris 59** : Memanggil method dequeue untuk melayani pelanggan pertama dalam antrean

**Baris 60** : Mengecek dengan kondisi elif apakah pengguna memilih menu "3" untuk melihat pelanggan pertama

**Baris 61** : Mencetak tiket_id pelanggan pertama dari antrean, atau "Kosong" jika antrean kosong

**Baris 62** : Mengecek dengan kondisi elif apakah pengguna memilih menu "4" untuk melihat pelanggan terakhir

**Baris 63** : Mencetak tiket_id pelanggan terakhir dari antrean, atau "Kosong" jika antrean kosong

**Baris 64** : Mengecek dengan kondisi elif apakah pengguna memilih menu "5" untuk cek antrean kosong

**Baris 65** : Mencetak hasil pengecekan apakah antrean kosong atau tidak menggunakan method is_empty

**Baris 66** : Mengecek dengan kondisi elif apakah pengguna memilih menu "6" untuk melihat jumlah pelanggan

**Baris 67** : Memanggil method display untuk menampilkan informasi lengkap kondisi antrean

**Baris 68** : Mengecek dengan kondisi elif apakah pengguna memilih menu "7" untuk keluar dari program

**Baris 69** : Mencetak pesan perpisahan sebelum program berhenti

**Baris 70** : Menghentikan perulangan while dengan perintah break sehingga program selesai

**Baris 71** : Masuk ke blok else apabila input pengguna tidak sesuai pilihan yang tersedia (1 hingga 7)

**Baris 72** : Mencetak pesan bahwa pilihan tidak valid dan meminta pengguna mencoba kembali

**Baris 74** : Pengecekan if __name__ == "__main__" untuk memastikan kode dijalankan langsung bukan diimpor sebagai modul

**Baris 75** : Memanggil fungsi main() sebagai titik masuk program



## Output
<img width="776" height="390" alt="Cuplikan layar 2026-05-19 171757" src="https://github.com/user-attachments/assets/20f7c875-1846-4562-9914-cf472cca4ccf" />
<img width="675" height="504" alt="Cuplikan layar 2026-05-19 171818" src="https://github.com/user-attachments/assets/f8634272-ebdf-4b0e-8cc4-878c8297980c" />
<img width="689" height="528" alt="Cuplikan layar 2026-05-19 171833" src="https://github.com/user-attachments/assets/87f85e96-89ea-4eb5-9243-d4c37c5602a0" />

Berdasarkan output program di atas, pengujian dilakukan dengan beberapa skenario untuk memastikan seluruh fitur berjalan dengan benar.

Pengujian pertama dilakukan dengan memilih menu 1 untuk menambah pelanggan. Pengguna memasukkan nama "eka" dan kode pelanggan "234", sehingga program membentuk tiket_id menjadi "EK34" dengan mengambil 2 huruf pertama nama (huruf kapital) dan 2 digit terakhir kode pelanggan. Program kemudian mencetak pesan "Pelanggan EK34 masuk antrean" yang menandakan proses enqueue berhasil dijalankan.

Pengujian kedua kembali memilih menu 1 dengan nama "gita" dan kode pelanggan "902", sehingga tiket_id yang terbentuk adalah "GI02". Karena tiket_id tersebut mengandung angka "2", program mengenali pelanggan ini sebagai VIP dan langsung mencetak pesan "Pelanggan GI02 langsung mendapat kursi tanpa antre!" tanpa memasukkannya ke dalam antrean.

Pengujian ketiga memilih menu 2 untuk melayani pelanggan. Program memanggil method dequeue dan mengeluarkan pelanggan pertama dari antrean yaitu "EK34", lalu mencetak pesan "Pelanggan EK34 dipanggil untuk membeli tiket". Hal ini membuktikan bahwa antrean bekerja sesuai prinsip FIFO (First In First Out), di mana pelanggan yang masuk lebih awal dilayani lebih dahulu.

Pengujian keempat memilih menu 3 untuk melihat pelanggan pertama. Karena pelanggan EK34 sudah dilayani dan tidak ada pelanggan reguler lain dalam antrean, program mencetak "Pelanggan pertama: Kosong". Begitu pula saat menu 4 dipilih untuk melihat pelanggan terakhir, program mencetak "Pelanggan terakhir: Kosong" karena antrean memang dalam keadaan kosong.

Pengujian kelima memilih menu 5 untuk mengecek status antrean. Program memanggil method is_empty dan mengembalikan nilai True, yang ditampilkan sebagai "Antrean kosong? True", membuktikan bahwa antrean benar-benar kosong setelah pelanggan EK34 dilayani.

Pengujian keenam memilih menu 6 untuk melihat jumlah pelanggan. Program memanggil method display dan mencetak "Total pelanggan di bioskop: 1/10 (VIP tidak dihitung antrean)" diikuti "Antrean kosong." Angka 1 pada total pelanggan berasal dari pelanggan VIP GI02 yang tetap dihitung dalam self.total_pelanggan meskipun tidak masuk ke dalam antrean.

Terakhir, pengguna memilih menu 7 untuk keluar dari program, sehingga program mencetak "Keluar dari program" dan perulangan while dihentikan dengan perintah break.

## Link Youtube

