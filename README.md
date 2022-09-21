# Jarkom-Modul-1-A04-2022

**Jarkom A04**<br>
**Anggota Kelompok**

| Nama                   | NRP        |
| ---------------------- | ---------- |
| Samuel                 | 5025201187 |
| Mohamad Kholid Bughowi | 5025201253 |
| Gloria Dyah Pramesti   | 5025201033 |

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
**Soal 5.** Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!<br>
**Penjelasan:** Menggunakan `tcp.srcport == 443`, didapat hasil sebagai berikut<br>
![no 5](https://user-images.githubusercontent.com/89601859/191540649-52591bbd-72c7-4f27-8a8e-9367ff4c4ea2.jpg)<br><br>
**Soal 6.** Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !<br>
**Penjelasan:** Pertama cari IP dari lipi.go.id dengan menggunakan `http.host == “lipi.go.id”`. Lalu didapat hasil sebagai berikut<br>
![no 6-1](https://user-images.githubusercontent.com/89601859/191540998-5e912808-deed-4fe8-a82b-233500cd31d4.jpg)<br>
Didapat port nya adalah **_192.168.0.27_**<br>
Lalu gunakan `ip.dst == 192.168.0.27`, jadi didapat hasil sebagai berikut<br>
![no 6-2](https://user-images.githubusercontent.com/89601859/191541916-fd273cec-0d88-4227-9617-4eb829e74488.jpg)<br><br>
**Soal 7.** Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!<br>
**Penjelasan:** Pertama kita perlu mengetahui berapa ip addres kita, untuk mengetahuinya bisa dengan mengetikkan command berikut di terminal (linux) `hostname -I`. Didapatkan ip address `10.8.28.210`
Kemudian dilakukan display filter dengan command berikut : ip.src == 10.8.28.210
Maka dihasilkan hasil filter seperti berikut :
![no 7-1](https://user-images.githubusercontent.com/49820990/191553649-63e448dc-6da1-43b5-8ce7-975d38ec26b5.png)

**Soal 8.** Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.<br>
**Penjelasan:** Berikut beberapa percakapan yang berhasil kami capture
![8 1](https://user-images.githubusercontent.com/49820990/191553918-fabd4933-1aeb-43ae-ae8c-f56e6c7dd9c6.png)
![8 2](https://user-images.githubusercontent.com/49820990/191553943-4c86b330-4895-46bc-a10c-023daddfa2ea.png)
![8 3](https://user-images.githubusercontent.com/49820990/191554066-5c67863c-cfa5-4d33-85fe-1b64f899d4c2.png)

**Soal 9.** Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format `[nama_kelompok].des3` dan simpan output file dengan nama `“flag.txt”`.<br>
**Penjelasan:** Berdasarkan percakapan yang dilakukan di tcp.stream == 12. Seseorang mengirimkan paket berupa file terenkripsi melalui port tcp 9002. Oleh karena itu, kita lakukan display filter dengan command berikut : tcp.port == 9002. Untuk mendapatkan semua informasi paket yang dikirim dan diterima pada port tersebut. Berikut hasil filter nya
![9 1](https://user-images.githubusercontent.com/49820990/191554367-328f598b-dbee-4757-8f7c-a299bbd4ce58.png)

Kita coba cek satu per satu dan berhasil menemukan stream paket tcp seperti berikut:
![9 2](https://user-images.githubusercontent.com/49820990/191554489-0459aede-1c6c-4dfd-91a8-86d0092d555a.png)

String tersebut kita simpan dalam bentuk raw
![9 3](https://user-images.githubusercontent.com/49820990/191554603-54765957-2687-4468-8e29-bad1356c7f3f.png)

Kemudian di rename menjadi `A04.des3`. Selanjutnya, file ini akan di decrypt dengan `openssl des3`, dengan command berikut :

```shell
openssl des3 -d -in A04.des3 -out flag.txt
```

Kemudian masukkan password sesuai dengan clue yang diberikan di percakapan, passwordnya adalah _nakano_.
Setelah berhasil ter-decrypt, isinya adalah `JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}`

**Soal 10.** Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!<br>
**Penjelasan:** Passwordnya _nakano_
