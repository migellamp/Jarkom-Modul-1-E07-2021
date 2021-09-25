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

## Soal 7 : Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
Display Filter : ```ftp-data.command contains ".zip" && ftp-data contains "Real.pdf" ``` 
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%207a.jpg) <br />
Pilih bar paling atas > klik kanan > pilih ```Follow > TCP Stream``` > Ubah menjadi bentuk RAW
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%207c.jpg) <br />
Save as > menjadi file .zip yaitu ```Real.zip``` > buka ```file Real.pdf```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%207d.jpg) <br />

## Soal 8 : Cari paket yang menunjukan pengambilan file dari FTP tersebut!

## Soal 9 : Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

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

## Soal 11 : Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80! Pada Capture Filter: src port 80

## Soal 12 : Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

## Soal 13 : Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Filter Capture : ```dst port 443```
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2013.jpg) <br />
![alt text](https://github.com/migellamp/Jarkom-Modul-1-E07-2021/blob/main/images/soal%2013b.jpg) <br />

## Soal 14 : Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id! Pada Capture Filter: dst host kemenag.go.id

## Soal 15 : Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
