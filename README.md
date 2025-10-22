Nama: Razy Al Farisi
Nim: 312410524

# input
![foto](https://github.com/razyyalfarisi/foto/blob/666763a800f1a19448df2d67817159d2ab591e68/Screenshot%202025-10-22%20193334.png)

Menandakan bahwa isi di dalam tag ini adalah kode JavaScript.
(Catatan: sekarang lebih umum ditulis `type="text/javascript"` atau cukup `<script>` saja).

`function test()`
Ini mendefinisikan fungsi bernama `test`, yang akan dijalankan saat tombol ditekan.

`var val1 = document.kirim.T1.value`
Mengambil nilai dari input teks bernama `T1` di form `kirim`.
Misalnya, jika kamu ketik `5`, maka `val1 = "5"`.

`if (val1 % 2 == 0)`
Mengecek apakah nilai `val1` habis dibagi 2.
Operator `%` (modulus) menghitung sisa bagi.
Jadi:

Jika `val1 % 2 == 0`, berarti bilangan genap

Jika tidak, berarti bilangan ganjil

`document.kirim.T2.value = "bilangan genap"`
Jika genap, maka kotak input `T2` akan berisi teks "bilangan genap"

`else document.kirim.T2.value = "bilangan ganjil"`
Jika tidak genap (berarti ganjil), maka isi teksnya menjadi "bilangan ganjil"

`<form name="kirim">`
Form diberi nama kirim supaya bisa diakses lewat JavaScript dengan document.kirim.

`<input type="text" name="T1">`
Kotak tempat kamu memasukkan angka.

`<input type="text" name="T2">`
Kotak yang akan menampilkan hasilnya (bilangan genap/ganjil).

`<input type="button" value="TEBAK" onclick="test()">`
Tombol untuk menjalankan fungsi test() saat diklik.

# button

![foto](https://github.com/razyyalfarisi/foto/blob/b2c52f4e7035c5abc6dd1af804909407822a94bb/Screenshot%202025-10-22%20190252.png)

![foto](https://github.com/razyyalfarisi/foto/blob/b2c52f4e7035c5abc6dd1af804909407822a94bb/Screenshot%202025-10-22%20194245.png)

![foto](https://github.com/razyyalfarisi/foto/blob/b2c52f4e7035c5abc6dd1af804909407822a94bb/Screenshot%202025-10-22%20194237.png)

![foto](https://github.com/razyyalfarisi/foto/blob/b2c52f4e7035c5abc6dd1af804909407822a94bb/Screenshot%202025-10-22%20194252.png)


`function ubahWarnaLB(warna)`
Fungsi ini digunakan untuk mengubah warna latar belakang (background) halaman.

`document.bgColor = warna;` artinya ubah warna background dokumen menjadi warna yang diberikan.

`function ubahWarnaLD(warna)`
Fungsi ini digunakan untuk mengubah warna teks (font).

`document.fgColor = warna;` artinya ubah warna teks menjadi warna yang diberikan.

`<input type="button"` ...>
Membuat tombol.

`onClick="ubahWarnaLB('RED')"`
Artinya: ketika tombol diklik, panggil fungsi `ubahWarnaLB()` dan kirimkan parameter `'RED'`.
Maka latar belakang jadi merah.

Ada beberapa tombol lain untuk mengganti warna:

Latar belakang: Merah, Putih

Warna teks: Biru, Hijau

# dom

![foto](https://github.com/razyyalfarisi/foto/blob/c6de833ba101e879d32b441849c19b9a61d482d6/Screenshot%202025-10-22%20194646.png)

`function hitung(ele)`
Fungsi ini dipanggil setiap kali pengguna mengklik (mencentang atau menghapus centang) pada checkbox.
Parameter `ele` merepresentasikan elemen checkbox yang sedang diklik.

`var total = document.getElementById('total').value;`
Mengambil nilai total harga saat ini dari kotak input dengan id `"total"`.

`total = (total ? parseInt(total) : 0);`
Kalau input `total` belum ada isinya nilai awalnya diatur jadi `0`.
Kalau sudah ada angka diubah dari teks menjadi angka (integer).

```js
harga = ele.value;
total += parseInt(harga);
```
Artinya harga menu tersebut ditambahkan ke total.

```js
harga = ele.value;
total -= parseInt(harga);
```
Artinya harga menu tersebut dikurangkan dari total (selama total > 0).

`document.getElementById('total').value = total;`
Menampilkan hasil total akhir ke dalam kotak input di bawah daftar menu.

```html
<input type="checkbox" value="13000" onclick="hitung(this);">
```
`value` = harga menu

`onclick="hitung(this)"` = ketika diklik, panggil fungsi `hitung()` dan kirim checkbox-nya (`this`).

Elemen `<input id="total" type="text">`
Tempat menampilkan hasil total harga.

