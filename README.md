# Jarkom-Modul-1-A04-2022
**Jarkom A04**<br>
**Anggota Kelompok**

|Nama                   |     NRP|
|-----------------------|----------------------|
|Samuel                 |    5025201187|
|Mohamad Kholid Bughowi |    5025201253|
|Gloria Dyah Pramesti   |    5025201033|

**Soal 1.** Sebutkan web server yang digunakan pada "monta.if.its.ac.id"!<br>
**Penjelasan:** Menuliskan `http` dan didapatkan hasil seperti berikut<br>
![no 1](https://user-images.githubusercontent.com/91613088/191537275-92937bc1-07c5-4a9e-8160-cd8632036017.png)<br><br>
**Soal 2.** Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq?<br>
**Penjelasan:** Menuliskan `http.host`<br>
![no 2](https://user-images.githubusercontent.com/91613088/191537289-e546a649-3636-477f-894e-e6dad9a5cb68.png)<br>
Detail topik HTML dijalankan di Visual Studio Code dan mendapatkan hasil seperti ini<br>
![no 2-1](https://user-images.githubusercontent.com/91613088/191537297-8d6dcae9-b7ac-4b9f-88fd-f91236836cc6.jpg)<br>
Maka judul TA yang sedang dibuka oleh Ishaq adalah Perancangan Sistem Pengendali Panas Otomatis pada Mesin Sangrai Kopi dengan Logika Fuzzy<br><br>
**Soal 3.** Filter sehingga wireshark hanya menampilkan paket yang menuju port 80! 
**Penjelasan:** Menuliskan `tcp.dstport == 80` dan akan menampilkan paket yang menuju port 80<br>
![no 3](https://user-images.githubusercontent.com/91613088/191537306-4c9f75d5-50ff-41a1-98a3-972738086a44.png)<br>
![no 3-1](https://user-images.githubusercontent.com/91613088/191537263-8869dcdc-be2c-4f60-a753-ad9796b812eb.png)<br><br>
**Soal 4.** Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!<br>
**Penjelasan:** Menggunakan `tcp.srcport == 21`, didapat hasil sebagai berikut<br>
![no 4](https://user-images.githubusercontent.com/89601859/191540380-1d435877-3fda-49df-aa35-03cc9102dc32.jpg)<br><br>
**Soal 5.** Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!
**Penjelasan:** Menggunakan `tcp.srcport == 443`, didapat hasil sebagai berikut<br>
![no 5](https://user-images.githubusercontent.com/89601859/191540649-52591bbd-72c7-4f27-8a8e-9367ff4c4ea2.jpg)<br><br>
**Soal 6.** Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !<br>
**Penjelasan:** Pertama cari IP dari lipi.go.id dengan menggunakan `http.host == “lipi.go.id”`. Lalu didapat hasil sebagai berikut<br>
![no 6-1](https://user-images.githubusercontent.com/89601859/191540998-5e912808-deed-4fe8-a82b-233500cd31d4.jpg)<br>
Didapat port nya adalah ***192.168.0.27***<br>
Lalu gunakan `ip.dst == 192.168.0.27`, jadi didapat hasil sebagai berikut<br>
![no 6-2](https://user-images.githubusercontent.com/89601859/191541916-fd273cec-0d88-4227-9617-4eb829e74488.jpg)<br><br>
