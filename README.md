# Laporan Resmi Jaringan Komputer Modul 1 - E07

Anggota Kelompok:

M Fikri Sunandar 05111940000135

Migel Aulia Mandiri Putra 05111940000194

Rizaldi Nur Rahman N 05111940000201

## Soal 1 : Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
Display Filter : ```http.host contains "ichimarumaru.tech"``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%201a.jpg) <br />
Pilih bar paling atas > klik kanan > pilih ```Follow > TCP Stream```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%201b.jpg) <br />
Dapat dilihat pada bagian server, yaitu ```Server: nginx/1.18.0 (Ubuntu)```

## Soal 2 : Temukan paket dari web-web yang menggunakan basic authentication method!
Display filter: ```http.authbasic"``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%202.png) <br />
Terlihat ada 3 paket yang menggunakan basic authentication.

## Soal 3 : Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
Display filter: ```http contains “.png”```
Kemudian pilih bar satu-satunya yang muncul, lalu lihat isi packet tersebut, tepatnya pada field “Authentication” > Credentials > klik kanan > Copy > Value
USER : ```kuncimenujulautan```
PASS : ```tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%203a.png)

Masukkan user dan pass ke **basic.ichimarumaru.tech**, lalu ikuti instruksi di dalamnya
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%203b.png)

## Soal 4 : Temukan paket mysql yang mengandung perintah query select!
Display Filter : ```mysql.query contains "SELECT" or mysql contains "select"``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%204a.jpg) <br />
Pilih bar paling atas > klik kanan > pilih ```Follow > TCP Stream```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%204b.jpg) <br />

## Soal 5 : Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
Display Filter : ```mysql.query contains "INSERT"``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%205a.png) <br />
Klik kanan pada paket yang ada -> klik "Follow" -> klik "TCP Stream"
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%205b.png) <br />
Terlihat username: ```akakanomi``` dan password: ```pemisah4lautan```

Login ke ```portal.ichimarumaru.tech``` dengan username dan password tadi. Dan ikuti instruksi yang ada.
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%205c.png) <br />
Instruksi: Masukan konfigurasi pengkabelan T568B

Urutan ke 1 : Putih Orange RD+ (data terima+)

Urutan ke 2 : Orange RD- (data terima-)

Urutan ke 3 : Putih Hijau TD+ (data kirim +)

Urutan ke 4 : Biru NC (tidak dipakai)

Urutan ke 5 : Putih Biru NC (tidak dipakai)

Urutan ke 6 : Hijau TD- (data kirim -)

Urutan ke 7 : Putih Coklat NC (tidak dipakai)

Urutan ke 8 : Coklat NC (tidak dipakai)

## Soal 6 : Cari username dan password ketika melakukan login ke FTP Server!
Display filter : ```ftp.request.command == USER```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%206a.png) <br />

Klik kanan pada bar paling atas > ```Follow > TCP Stream```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%206b.png) <br />
Terlihat ada ```USER : secretuser``` dan ```PASS : aku.pengen.pw.aja ```

## Soal 7 : Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
Display Filter : ```ftp-data.command contains ".zip" && ftp-data contains "Real.pdf" ``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%207a.jpg) <br />
Pilih bar paling atas > klik kanan > pilih ```Follow > TCP Stream``` > Ubah menjadi bentuk RAW
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%207c.jpg) <br />
Save as > menjadi file .zip yaitu ```Real.zip``` > buka ```file Real.pdf```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%207d.jpg) <br />

## Soal 8 : Cari paket yang menunjukan pengambilan file dari FTP tersebut!
Display Filter : ```ftp.request.command == RETR``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%208.png) <br />

## Soal 9 : Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
Display Filter : ```ftp-data.command ~ "secret.zip"```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%209a.png) <br />

Pilih bar paling atas > ```Follow TCP Stream``` > ubah menjadi RAW dan Save AS menjadi ```secret.zip```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%209b.png) <br />

Buka secret.zip, terdapat file ```Wanted.pdf``` sebagai berikut
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%209c.png) <br />

## Soal 10 : Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
Setelah mendapatkan file ```secret.zip``` pada soal 9, terdapat file yang terkunci yaitu bernama ```Wanted.pdf```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2010a.jpg) <br />
Selanjutnya untuk mencari password, pada soal letak password terletak pada file “history.txt” <br />
Display Filter : ```ftp-data contains "secret.zip"```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2010b.jpg) <br />
Pilih bar paling atas > klik kanan > pilih ```Follow > TCP Stream```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2010c.jpg) <br />
Saat dibuka terdapat clue yaitu ```key= bukanapaapa.txt```, oleh karena itu mencari lagi menggunakan <br />
Display filter : ```ftp-data contains "bukanapaapa"```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2010d.jpg) <br />
Pilih bar paling atas > klik kanan > pilih ```Follow > TCP Stream``` > muncul sebuah password yang dapat digunakan untuk membuka secret.zip yaitu ```d1b1langbukanapaapajugagapercaya```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2010e.jpg) <br />
Setelah mendapat password, tinggal dibuka file secret.zip > wanted.pdf dengan password diatas.
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2010f.jpg) <br />

## Soal 11 : Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
Capture filter : ```src port 80```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2011a.png) <br />
Klik enter -> maka akan muncul paket-paket yang berasal dari port 80
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2011b.png) <br />


## Soal 12 : Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Capture filter : ```port 21```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2012a.png) <br />

Hasil
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2012b.png) <br />

## Soal 13 : Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Filter Capture : ```dst port 443```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2013.jpg) <br />
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2013b.jpg) <br />

## Soal 14 : Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id! 
Capture Filter: ```dst host kemenag.go.id```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2014a.png) <br />
Klik enter -> maka akan muncul paket-paket yang tujuannya ke ```kemenag.go.id```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2014b.png) <br />

## Soal 15 : Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Capture filter : src ```<ip anda>```. Menggunakan ip saya : ```src 192.168.0.177```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2015a.png) <br />

haisl :
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2015b.png) <br />