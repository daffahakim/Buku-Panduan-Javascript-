# Komentar

Dalam proses pengembangan sebuah program, tentunya kita akan disibukkan dengan penulisan kode-kode yang begitu banyak dan 'tampak' rumit sehingga akan sulit untuk dipahami oleh orang lain. Untuk menangani masalah ini, sebagai programmer kita sebaiknya menambahkan komentar untuk menjelaskan algoritma dan keterangan-keterangan yang diperlukan dalam program sehingga program menjadi lebih mudah dipahami oleh yang melihatnya. Hal ini juga akan membantu dalam proses pemeliharaan (maintenance) dari program yang telah kita buat.

Selain kebutuhan diatas komentar juga banyak digunakan untuk menuliskan informasi tentang kode program, misalnya nama nama pembuat kode program, kapan kode tersebut dibuat / dimodifikasi, lisensi dari program tersebut, maupun deskripsi lain yang diperlukan.

Komentar baris tunggal dimulai dengan tanda //.

Teks apa pun yang berada di antara // dan akhir baris akan diabaikan oleh JavaScript (tidak akan dieksekusi).

Contoh ini menggunakan komentar baris tunggal yang letaknya sebelum baris kode:

```javascript
<!DOCTYPE html>
<html>
<body>

<h1 id="myH"></h1>
<p id="myP"></p>

<script>
// merubah heading:
document.getElementById("myH").innerHTML = "Komentar pada JavaScript";
// merubah paragraf:
document.getElementById("myP").innerHTML = "Paragraf Pertamaku";
</script>

</body>
</html>
```

Contoh ini menggunakan komentar baris tunggal di akhir setiap baris untuk menjelaskan kode:

```javascript
<!DOCTYPE html>
<html>
<body>

<h2>Komentar pada JavaScript</h2>

<p id="demo"></p>

<script>
var x = 5;    // Deklarasikan x, berikan nilai 5
var y = x + 2;  // Deklarasikan y, berikan nilai x + 2
// Tulis y pada demo:
document.getElementById("demo").innerHTML = y;
</script>


</body>
</html>
```
