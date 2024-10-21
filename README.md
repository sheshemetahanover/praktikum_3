# **Membuat Kode Program dari flowchart pertemuan ke 5**

Tugas Pertemuan Ke 5

Nama: She she metahanover

Kelas: TI 24 A3

NIM: 312410432

## **1. bilanganterbesar.py**

Program pertama yang akan dibuat adalah Program untuk menampilkan bilangan terbesar dari 3 Bilangan yang di Inputkan

Berikut adalah flowchartnya

<img src="/.images/pertama.png" width="500" alt="Flowchart">

**Program akan meminta kita untuk memasukkan 3 angka untuk dibandingkan :**

<img src="/.images/outputprogram1.png" width="500" alt="output">

**Penjelasan Code**

**1.**

```
def mencari_bilangan_terbesar(a, b, c):
    if a > b:
        if a > c:
            return a, "A adalah terbesar"
        else:
            return c, "C adalah terbesar"
    else:
        if b > c:
            return b, "B adalah terbesar"
        else:
            return c, "C adalah terbesar"

# Input bilangan A, B, C
print("Masukkan tiga bilangan:")
a = float(input("A: "))
b = float(input("B: "))
c = float(input("C: "))

# Menentukan bilangan terbesar
largest, message = mencari_bilangan_terbesar(a, b, c)

# Menampilkan hasil
print(f"\n{message}")
print(f"Bilangan terbesar adalah: {largest}")
```

1. Kita mendefinisikan function _mencari_bilangan_terbesar_ yang mengambil tiga parameter (a,b,c).
2. function tersebut menggunakan nested if-else statement untuk membandingkan angka yang di inputkan
3. Kemudian akan menampilkan Mana bilangan terbesar
4. Lalu di Program utamanya kita masukkan angka yang harus dimasukkan oleh user
5. Lalu kita panggil kembali function _mencari_biilangan_terbesar_
6. Lalu Output bilangan terbesar dari ketiga bilangan yang di input akan muncul

## **2. bilanganN.py**

Program Kedua adalah untuk membandingkan bilangan yang di Input, input akan terus berjalan kecuali user memasukkan nilai 0

**Flowchartnya**

<img src="/.images/kedua.png" width="500" alt="Flowchart">

**Program akan meminta kita untuk memasukkan angka untuk dibandingkan, _`input akan terus diminta sebelum user memasukkan angka 0_ :**

<img src="/.images/outputprogram2.png" width="500" alt="output">

**Penjelasan Code**

```
def find_largest_number():
```

Mendefinisikan fungsi bernama _find_largest_number_ yang akan menangani logika utama program.

```
    largest = float('-inf')  # Inisialisasi dengan nilai negatif tak terhingga
```

Menginisialisasi variabel largest dengan nilai negatif tak terhingga. Ini memastikan bahwa angka pertama yang dimasukkan akan selalu lebih besar.

_\*Maksud dari -infinity(Negatif tak hingga) adalah nilai negatif berapapun._

```
    count = 0
```

Menginisialisasi variabel _count_ untuk menghitung jumlah bilangan yang dimasukkan.

```
    while True:
```

Memulai loop tak terbatas. Akan terus berjalan sampai dihentikan oleh _break_.

```
        num = float(input(f"Masukkan bilangan ke-{count + 1} (atau 0 untuk selesai): "))

```

Meminta input dari pengguna, mengkonversinya ke float, dan menyimpannya dalam variabel _num_.

```
if num == 0:
            break
```

Jika input adalah 0, keluar dari loop.

```
count += 1
```

Menambah penghitung jumlah bilangan yang dimasukkan.

```
if num > largest:
            largest = num
```

Jika bilangan yang baru dimasukkan lebih besar dari _largest_ saat ini, update _largest_.

```
return largest, count
```

Setelah loop selesai, kembalikan bilangan terbesar dan jumlah input.

```
print("Program untuk menentukan bilangan terbesar dari N bilangan")
print("Masukkan angka 0 untuk mengakhiri input\n")
```

Mencetak instruksi untuk pengguna.

```
largest, count = find_largest_number()
```

Memanggil fungsi _find_largest_number()_ dan menyimpan hasilnya.

```
if count > 0:
```

Memeriksa apakah ada bilangan yang dimasukkan.

```
print(f"\nJumlah bilangan yang dimasukkan: {count}")
    print(f"Bilangan terbesar adalah: {largest}")
```

Jika ada bilangan yang dimasukkan, cetak jumlah input dan bilangan terbesar.

```
else:
    print("\nTidak ada bilangan yang dimasukkan.")
```

Jika tidak ada bilangan yang dimasukkan (pengguna langsung memasukkan 0), program akan dijalankan dan menampilkan output perbandingan.
