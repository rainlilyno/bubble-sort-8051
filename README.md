# bubble-sort-8051
Analisis Performa Bubble Sort pada Mikrokontroler 8051



# Deskripsi Proyek
Proyek ini merupakan tugas mata kuliah Organisasi dan Arsitektur Komputer yang bertujuan untuk menganalisis performa algoritma Bubble Sort pada mikrokontroler 8051 menggunakan simulator MCU 8051 IDE.
Dua implementasi dibandingkan dalam proyek ini:
*V1 : Bubble Sort standar.
*V2 : Bubble Sort dengan optimasi Early Exit menggunakan register R3 sebagai flag.

Pengujian dilakukan pada tiga skenario data:
1. Best Case
2. Average Case
3. Worst Case
Parameter yang diamati meliputi waktu eksekusi, penggunaan register, dan hasil pengurutan data.



# Platform
* Mikrokontroler : AT89S52 (Arsitektur 8051)
* Simulator : MCU 8051 IDE v1.4.9
* Bahasa Pemrograman : Assembly 8051
* Clock : 12 MHz



# Cara Menjalankan Program
1. Buka MCU 8051 IDE.
2. Pilih File → Open.
3. Buka file `.asm` yang ingin diuji.
4. Klik Assemble.
5. Jalankan simulasi menggunakan tombol Run.
6. Amati perubahan memori, register, dan waktu eksekusi.


Skenario Pengujian
Program diuji menggunakan tiga skenario data yang berbeda. Perubahan hanya dilakukan pada bagian inisialisasi array di alamat memori 20H--24H.

Best Case
Data telah terurut sejak awal.
MOV 20H,#01H
MOV 21H,#03H
MOV 22H,#05H
MOV 23H,#07H
MOV 24H,#08H
Array:
{01, 03, 05, 07, 08}

Average Case
Data berada dalam kondisi acak.
MOV 20H,#05H
MOV 21H,#03H
MOV 22H,#08H
MOV 23H,#01H
MOV 24H,#07H
Array:
{05, 03, 08, 01, 07}

Worst Case
Data berada dalam urutan terbalik.
MOV 20H,#08H
MOV 21H,#07H
MOV 22H,#05H
MOV 23H,#03H
MOV 24H,#01H
Array:
{08, 07, 05, 03, 01}

Ketiga skenario tersebut digunakan pada implementasi V1 (Bubble Sort Standar) maupun V2 (Bubble Sort dengan Early Exit).



# Hasil Utama
* Kedua implementasi berhasil mengurutkan data dengan benar.
* V2 mampu melakukan early exit ketika array sudah terurut.
* Pada beberapa kondisi, overhead instruksi tambahan menyebabkan V2 tidak selalu lebih cepat dibandingkan V1.
* Performa terbaik V2 diperoleh pada skenario tertentu yang memungkinkan pengurangan jumlah iterasi.



# Anggota Kelompok
1. Laila Maulidia Aghnia Putri
2. Marsela Nur Choirunnisa
3. Wahyu Yuliarto 


