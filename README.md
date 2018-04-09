##  use python 3.4.2
## script ini akan menghasilkan output menu-menu dari module-module yang ada library. Menu-menu tersebut adalah Penilaian Mahasiwa, Pembayaran Mahasiswa, dan Kalkulator. Untuk lebih jelasnya, yukk simak sedikit penjelasan berikut! Script ini menggunakan function.

## perintah untuk membuat username dan password di script yang akan kita running, dan jika dijalankan di cmd, password akan tersamarkan
```javascript
import getpass
```
## fungsi untuk menampilkan menu-menu, di sini saya beri nama parameternya yaitu 'login'
```javascript
def login():
    print("=======================================")
    print("\n\t---Pilihan Utama---")
    print("\n\t1. Penilaian Mahasiswa")
    print("\n\t2. Pembayaran Mahasiswa")
    print("\n\t3. Kalkulator")
```
## fungsi untuk memanggil menu-menu yang sebelumnya telah ditampilkan
```javascript
    pilih = input("\n\tSilahkan Pilih : ")
 ```
## jika dipilih angka 1, maka akan menampilkan sebuah output penilaian mahasiswa, dimana output itu berasal dari module yang telah dibuat pada library, yang dipackage dengan nama 'perhitungan'. Module tersebut bisa dilihat di sini [github](https://github.com/KSofi/penilaian_mahasiswa/blob/master/penilaian_mahasiswa.py)
```javascript
    if pilih == "1":
        from perhitungan.penilaian_mahasiswa import tt
```
## begitupun jika input angka 2, berarti memanggil sebuah module yang telah dibuat pada library, yang dipackage dengan nama 'perhitungan', module itu bernama 'pembayaran-mahasiswa', bisa dilihat di [github] (https://github.com/KSofi/pembayaran_mahasiswa/blob/master/pembayaran_mahasiswa.py) yaaa...
```javascript
    elif pilih == "2":
        from perhitungan.pembayaran_mahasiswa import pembayaran
```
## dan jika dipilih angka 3, maka akan muncul sebuah tampilan kalkulator. Module kalkulator sendiri bisa dilihat di [github] (https://github.com/KSofi/kalkulator/blob/master/kalkulator.py)
```javascript
elif pilih == "3":
        from perhitungan.kalkulator import kalkulator
```
## jika diinput pilihan lain, maka akan otomatis keluar
```javascript
else :
        exit
```
## di setiap akhir program yang dijalankan, akan dihadapkan dengan pertanyaan, apakah akan berlanjut menggunakan program ini atau tidak
```jabvascript
    tanya()
```
## fungsi tanya berbentuk seperti ini
```javascript
def tanya():
    tanya=input("\n\tKembali ke Pilihan Utama (y/n)? ")
    if tanya == "y":
        login()
    elif tanya == "n":
        exit
    else :
        print ("Pilihan yang Anda Masukkan Tidak Tersedia!")
```
## nah ini nih yang dimaksud username & password yang telah disinggung di atas
```javascript
user = input("\nUsername : ")
password = getpass.getpass()
print ("=========================================")

if user == "Khalis Sofi" and password == "777":
    login()

else :
    print ("Maaf Username atau Password Salah!")
```

## demikian penjelasan singkat dari saya, semoga bermanfaat. Selamat mencoba....
