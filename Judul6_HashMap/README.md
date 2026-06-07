# Program Kamus Bahasa Batak ke Bahasa Indonesia Menggunakan Hash Map
## Deskripsi Singkat
Program ini adalah implementasi HashMap Separate Chaining untuk simulasi kamus sederhana bahasa daerah. Pengguna dapat menambahkan pasangan kata dan arti, mencari arti suatu kata, menghapus kata dari kamus, serta menampilkan seluruh isi kamus berdasarkan indeks hash. Program menggunakan struktur data Linked List untuk menangani collision pada setiap bucket hash, di mana setiap node menyimpan key, value, dan pointer next. Fungsi hash dibuat dengan menjumlahkan nilai ASCII tiap karakter pada key menggunakan ord() lalu dimodulo dengan ukuran tabel. Program dilengkapi operasi utama seperti insert() untuk menambah data, search() untuk mencari kata, remove_key() untuk menghapus kata, serta display() untuk menampilkan isi tabel hash secara keseluruhan dengan bentuk rantai node (linked list).

## Source Code
<img width="488" height="534" alt="Cuplikan layar 2026-06-05 142530" src="https://github.com/user-attachments/assets/daae5422-1483-4bcf-bf7b-78ae25417375" />
<img width="455" height="563" alt="Cuplikan layar 2026-06-05 143500" src="https://github.com/user-attachments/assets/21d1ab29-f4c2-4891-bc4e-97f4e3795e07" />
<img width="504" height="333" alt="Cuplikan layar 2026-06-05 142557" src="https://github.com/user-attachments/assets/f6601570-6185-418c-bfeb-2a2b87765d98" />

* **Baris 1**

```python
class Node:
```

Membuat class `Node` yang digunakan sebagai elemen pada linked list di setiap bucket hash table.

* **Baris 2**

```python
def __init__(self, key, value):
```

Constructor class `Node` yang dijalankan saat objek node dibuat.

* **Baris 3**

```python
self.key = key
```

Menyimpan key/kata ke dalam atribut `key`.

* **Baris 4**

```python
self.value = value
```

Menyimpan value/arti kata ke dalam atribut `value`.

* **Baris 5**

```python
self.next = None
```

Pointer ke node berikutnya dalam linked list. Awalnya bernilai `None`.

* **Baris 8**

```python
class HashMapSeparateChaining:
```

Membuat class `HashMapSeparateChaining` sebagai struktur data hash map menggunakan metode separate chaining.

* **Baris 9**

```python
def __init__(self, size=10):
```

Constructor class hash map dengan ukuran default tabel sebesar 10.

* **Baris 10**

```python
self.SIZE = size
```

Menyimpan ukuran hash table ke atribut `SIZE`.

* **Baris 11**

```python
self.table = [None] * self.SIZE
```

Membuat array/list hash table berisi `None` sebanyak ukuran tabel.

* **Baris 13**

```python
def hash_function(self, key):
```

Method untuk menentukan index penyimpanan berdasarkan key.

* **Baris 14**

```python
return sum(ord(c) for c in key) % self.SIZE
```

Mengubah setiap karakter menjadi kode ASCII menggunakan `ord()`, menjumlahkannya, lalu mengambil sisa bagi dengan ukuran tabel agar mendapatkan index.

* **Baris 16**

```python
def insert(self, key, value):
```

Method untuk menambahkan data baru ke hash map.

* **Baris 17**

```python
index = self.hash_function(key)
```

Menentukan index penyimpanan menggunakan hash function.

* **Baris 18**

```python
current = self.table[index]
```

Mengambil node pertama pada bucket/index tersebut.

* **Baris 20**

```python
while current is not None:
```

Melakukan traversal linked list selama node masih ada.

* **Baris 21**

```python
if current.key == key:
```

Memeriksa apakah key sudah ada di dalam hash map.

* **Baris 22**

```python
current.value = value
```

Jika key ditemukan, maka value diperbarui.

* **Baris 23**

```python
return
```

Menghentikan proses insert karena data sudah diperbarui.

* **Baris 24**

```python
current = current.next
```

Berpindah ke node berikutnya.

* **Baris 26**

```python
new_node = Node(key, value)
```

Membuat node baru berisi key dan value.

* **Baris 27**

```python
new_node.next = self.table[index]
```

Node baru diarahkan ke node lama pada bucket tersebut.

* **Baris 28**

```python
self.table[index] = new_node
```

Menjadikan node baru sebagai kepala linked list pada bucket.

* **Baris 30**

```python
def search(self, key):
```

Method untuk mencari data berdasarkan key.

* **Baris 31**

```python
index = self.hash_function(key)
```

Menentukan index menggunakan hash function.

* **Baris 32**

```python
current = self.table[index]
```

Mengambil node pertama pada bucket tersebut.

* **Baris 34**

```python
while current is not None:
```

Melakukan traversal linked list.

* **Baris 35**

```python
if current.key == key:
```

Memeriksa apakah key sesuai dengan yang dicari.

* **Baris 36**

```python
return current
```

Mengembalikan node jika key ditemukan.

* **Baris 37**

```python
current = current.next
```

Berpindah ke node berikutnya.

* **Baris 39**

```python
return None
```

Mengembalikan `None` jika key tidak ditemukan.

* **Baris 41**

```python
def remove_key(self, key):
```

Method untuk menghapus data berdasarkan key.

* **Baris 42**

```python
index = self.hash_function(key)
```

Menentukan index bucket dari key.

* **Baris 43**

```python
current = self.table[index]
```

Mengambil node pertama pada bucket.

* **Baris 44**

```python
prev = None
```

Variabel untuk menyimpan node sebelumnya.

* **Baris 46**

```python
while current is not None:
```

Traversal linked list selama node masih ada.

* **Baris 47**

```python
if current.key == key:
```

Memeriksa apakah key ditemukan.

* **Baris 48**

```python
if prev is None:
```

Memeriksa apakah node yang dihapus adalah node pertama.

* **Baris 49**

```python
self.table[index] = current.next
```

Jika node pertama, head bucket dipindahkan ke node berikutnya.

* **Baris 50**

```python
else:
```

Jika node bukan node pertama.

* **Baris 51**

```python
prev.next = current.next
```

Node sebelumnya diarahkan ke node setelah node yang dihapus.

* **Baris 52**

```python
return True
```

Mengembalikan `True` karena penghapusan berhasil.

* **Baris 54**

```python
prev = current
```

Menyimpan node saat ini sebagai node sebelumnya.

* **Baris 55**

```python
current = current.next
```

Berpindah ke node berikutnya.

* **Baris 57**

```python
return False
```

Mengembalikan `False` jika key tidak ditemukan.

* **Baris 59**

```python
def display(self):
```

Method untuk menampilkan isi hash map.

* **Baris 60**

```python
print("\nIsi Kamus:")
```

Menampilkan judul output.

* **Baris 61**

```python
for i in range(self.SIZE):
```

Melakukan perulangan untuk setiap bucket dalam hash table.

* **Baris 62**

```python
print(f"{i}: ", end="")
```

Menampilkan nomor index bucket.

* **Baris 63**

```python
current = self.table[i]
```

Mengambil node pertama pada bucket.

* **Baris 65**

```python
while current is not None:
```

Traversal linked list pada bucket.

* **Baris 66**

```python
print(f"({current.key} : {current.value}) -> ", end="")
```

Menampilkan key dan value dari node.

* **Baris 67**

```python
current = current.next
```

Berpindah ke node berikutnya.

* **Baris 69**

```python
print("NULL")
```

Menandakan akhir linked list pada bucket.

* **Baris 72**

```python
def main():
```

Function utama program.

* **Baris 73**

```python
kamus = HashMapSeparateChaining()
```

Membuat objek hash map bernama `kamus`.

* **Baris 75 - 81**

```python
kamus.insert("mangan", "makan")
kamus.insert("madabu", "jatuh")
kamus.insert("bisuk", "bijak")
kamus.insert("aek", "air")
kamus.insert("jagal", "daging")
kamus.insert("au", "aku")
kamus.insert("muruk", "marah")
```

Menambahkan beberapa data kata dan arti ke dalam hash map.

* **Baris 83**

```python
kamus.display()
```

Menampilkan seluruh isi kamus.

* **Baris 85**

```python
hasil = kamus.search("mangan")
```

Mencari key `"mangan"` pada hash map.

* **Baris 86**

```python
if hasil is not None:
```

Memeriksa apakah data ditemukan.

* **Baris 87**

```python
print(f"\nArti dari '{hasil.key}' adalah '{hasil.value}'")
```

Menampilkan arti kata jika ditemukan.

* **Baris 88 - 89**

```python
else:
    print("\nKata tidak ditemukan")
```

Menampilkan pesan jika kata tidak ditemukan.

* **Baris 91**

```python
kamus.remove_key("bisuk")
```

Menghapus key `"bisuk"` dari hash map.

* **Baris 92**

```python
print("\nSetelah menghapus kata 'bisuk':")
```

Menampilkan pesan setelah penghapusan data.

* **Baris 93**

```python
kamus.display()
```

Menampilkan isi hash map setelah data dihapus.

* **Baris 95**

```python
hasil = kamus.search("langga")
```

Mencari key `"langga"`.

* **Baris 96 - 99**

```python
if hasil is not None:
    print(f"\nArti dari '{hasil.key}' adalah '{hasil.value}'")
else:
    print("\nKata tidak ditemukan")
```

Menampilkan hasil pencarian kata.

* **Baris 102**

```python
if __name__ == "__main__":
```

Memastikan program dijalankan langsung, bukan di-import sebagai module.

* **Baris 103**

```python
main()
```

Memanggil function `main()` untuk menjalankan program.


## Output
<img width="613" height="393" alt="Cuplikan layar 2026-06-05 142615" src="https://github.com/user-attachments/assets/ecc88a63-f3e0-46c2-a0bf-99490f3e3988" />

Berdasarkan output program di atas, program terlebih dahulu menampilkan seluruh isi kamus yang disimpan menggunakan struktur data HashMap dengan metode Separate Chaining. Data ditampilkan berdasarkan indeks hash dari 0 sampai 9. Setiap indeks dapat berisi lebih dari satu data karena adanya collision, yaitu kondisi ketika beberapa key memiliki nilai hash yang sama dan disimpan dalam bentuk linked list. Hal ini terlihat pada indeks 2 yang menyimpan data `(bisuk : bijak)` dan pada indeks 4 yang menyimpan `(muruk : marah)` serta `(au : aku)` dalam satu bucket yang sama. Selain itu terdapat juga data lain seperti `(jagal : daging)` pada indeks 1, `(aek : air)` pada indeks 5, `(mangan : makan)` pada indeks 6, dan `(madabu : jatuh)` pada indeks 8.

Setelah seluruh isi kamus ditampilkan, program menjalankan fungsi `search("mangan")` untuk mencari arti kata `"mangan"`. Program terlebih dahulu menghitung nilai hash dari kata tersebut untuk menentukan indeks penyimpanannya, kemudian melakukan traversal pada linked list di bucket terkait hingga menemukan key yang sesuai. Karena data ditemukan pada indeks 6, program menampilkan output `Arti dari 'mangan' adalah 'makan'`.

Selanjutnya program menjalankan fungsi `remove_key("bisuk")` untuk menghapus data dengan key `"bisuk"`. Program kembali menghitung hash key untuk menentukan bucket yang sesuai, kemudian melakukan traversal linked list hingga menemukan node dengan key tersebut. Setelah data ditemukan, node dihapus dari linked list sehingga bucket indeks 2 menjadi kosong dan hanya menampilkan `NULL`.

Program kemudian kembali menampilkan isi kamus setelah proses penghapusan. Output menunjukkan bahwa data `(bisuk : bijak)` sudah tidak ada lagi, sedangkan data lainnya tetap tersimpan dengan benar pada bucket masing-masing.

Terakhir, program menjalankan fungsi `search("langga")` untuk mencari kata `"langga"`. Setelah proses pencarian dilakukan pada bucket yang sesuai, program tidak menemukan key tersebut di dalam hash map sehingga menghasilkan output `Kata tidak ditemukan`. Hal ini menunjukkan bahwa fungsi pencarian dapat membedakan data yang tersedia dan data yang tidak ada di dalam struktur HashMap.

## Link Yt
