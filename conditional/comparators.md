Operator Perbandingan
Ada delapan operator logika di JavaScript, yaitu:
```
Equal value, ==
Equal value and type, ===
Not equal, !=
Not equal value and type, !==
Greater than, >
Less than, <
Greater than or equal, >=
Less than or equal, <=
Equal value, ==
var1 == var2
```

// apakah var1 bernilai sama dengan var2?

Operator equal value melakukan pengecekan apakah operand pertama, sebelah kiri, bernilai sama dengan operand kedua, sebelah kanan. Jika bernilai sama maka operasi akan mengembalikan true. Jika bernilai tidak sama maka operasi akan mengembalikan false.
<img src="https://miro.medium.com/max/700/1*V2uha0VelPfDnKCEWP0zKw.png"/>

Perhatikan contoh diatas. Untuk perbandingan string, string tersebut harus persis sama termasuk penulisan kapital atau tidak. Untuk perbandingan number, Anda dapat membandingkan dua buah angka walaupun dengan representasi base berbeda. Seperti pada contoh diatas saya membandingkan base 10 dengan base 16 (hexa) dan base 8 (octal) dan hasilnya tetap true.

Equal value and type, ===
```
var1 === var 2
```

// apakah var1 memliki tipe yang sama dan bernilai sama dengan var2

**Operator ==** akan mengembalikan true sementara operator === akan mengembalikan false.
Dapat terlihat bahwa hasil dari kedua operator tersebut berbeda. Operator ==, atau biasa disebut loose equality operator, hanya melakukan pengecekan pada nilai dari kedua operand. Apabila kedua operand memiliki tipe yang berbeda maka JavaScript akan mencoba untuk mengkonversi kedua operand tersebut ke tipe data yang sama.

**Sementara operator ===** , atau biasa disebut strict equality operator, melakukan dua pengecekan, yaitu pertama melakukan pengecekan terhadap tipe data kedua operand. Jika sama maka pengecekan dilanjutkan ke pengecekan nilai. Jika tipe kedua operand berbeda maka JavaScript akan langsung mengembalikan false.

Pada contoh diatas baris keempat, sebelum dilakukan pengecekan nilai dilakukan pengecekan tipe data terlebih dahulu. Kita ketahui bahwa operand pertama memiliki tipe data number sementara operand kedua memiliki tipe data string. Kedua operand tidak memiliki tipe data yang sama maka JavaScript langsung mengembalikan false.

**Penggunaan == dan ===**

Pada contoh pertama diatas terlihat ada segitiga warna kuning pada sisi nomor baris. Hal ini merupakan peringatan untuk tidak menggunakan operator ‘equal value, ==’ jika ingin membandingkan nilai boolean, undefined, atau null. Jika ingin melakukan pengecekan terhadap nilai boolean, undefined, atau null gunakan operator ‘equal value and type, ===’. Walaupun operator === juga diperuntukkan melakukan perbandingan tipe data lainnya.

Mengapa disarankan menggunakan operator strict equality? Agar hasil dari evaluasi kondisi tersebut bisa diyakinkan bahwa yang dibandingkan merupakan tipe data yang sama.

Memangnya kenapa kalau tidak sama? Pada JavaScript ketika kita melakukan perbandingan terhadap suatu nilai, nilai tersebut akan dikonversi oleh JavaScript menjadi nilai yang ‘sesuai’ untuk membandingkan kedua operand tersebut. Konversi ini pada JavaScript disebut automatic type conversion. Perhatikan contoh berikut.


Lihat perbedaan hasil evaluasi operasi diatas. Dengan loose equality operator null jika dibandingkan dengan undefined akan bernilai true. Sementara jika menggunakan strict equality operator akan menghasilkan false. Tentunya perbedaan hasil ini akan berdampak pada kode yang Anda jalankan nantinya dan berpotensi menimbulkan bug.

Saya menyarankan Anda untuk selalu menggunakan strict equality operator, ===, untuk melakukan perbandingan equality dan hindari penggunaan loose equality operator. Jika memang diperlukan untuk melakukan perbandingan nilai dari dua tipe data berbeda lakukan konversi/casting terlebih dahulu pada salah satu operand.

**Not equal value, !=**

```

var1 != var2
// apakah var1 bernilai tidak sama dengan var2
```


Seperti operator != merupakan kebalikan dari operator ==. Jika Operator == mengembalikan true jika var1 dan var2 bernilai sama, operator != akan mengembalikan true jika var1 bernilai berbeda dari var2.


**Menggunakan operator !=**

Untuk NaN saya tidak sarankan menggunakan operator == atau != untuk melakukan pengecekan terhadap NaN itu sendiri. Gunakan isNaN().

**Not equal value and type, !==**


```
var1 !== var
// apakah var1 memiliki tipe yang sama dan memiliki bernilai tidak sama dengan var2?
```


Layaknya strict equality operator, operator !==, strict inequality operator, terlebih dahulu melakukan pengecekan terhadap tipe data dari kedua operand. Perbedaan nya hanyalah operator !== melakukan kebalikannya. Pertama adaah pengecekan tipe data. Jika kedua operand memiliki tipe data yang berbeda maka operator !== akan langsung mengembalikan true. Sementara jika kedua operand memiliki tipe data yang sama baru lah dilakukan pengecekan terhadap nilai kedua operand tersebut. Jika bernilai sama maka operator !== mengembalikan false. Jika bernilai berbeda maka operator !== mengembalikan true.


Gunakan selalu strict inequality operator untuk melakukan pengecekan tipe data dan nilai
Greater than, >
var1 > var2
// apakah var1 bernilai lebih besar dari var2?

Operator > melakukan perbandingan nilai apakah operand pertama bernilai lebih besar dari operand kedua.


Operator > juga dapat digunakan untuk membandingkan string. String akan diubah nilainya menjadi bilangan decimal representasi char tersebut terlebih dahulu secara otomatis oleh JavaScript melalui sifat automatic type conversion. Kemudian nilai decimal representasi char dari kedua operand tersebut baru dibandingkan. Anda dapat melihat nilai tersebut pada table ASCII pada tautan berikut http://www.asciitable.com/. Perhatikan contoh berikut.



```

ASCII Table
Less than, <
var1 < var2
// apakah var1 bernilai lebih kecil dari var2?
```


Operator < melakukan perbandingan apakah operand pertama lebih kecil nilainya daripada operand kedua. Sifat dari operator < persis sama dengan operator > hanya perbedaan pengecekan saja.


Anda bisa merujuk ASCII table pada tautan yang telah saya berikan untuk Anda bandingkan sendiri sesuai contoh diatas.

Greater or equal than, >=

```

var1 >= var2
// apakah var2 bernilai lebih besar atau sama dengan var2?
```


Operator >= hampir sama dengan operator > hanya saja operasi perbandingan dengan operator >= akan tetap mengembalikan true jika kedua operand bernilai sama. Juga bernilai true jika operand pertama bernilai lebih besar dari operand kedua.


Operasi perbandingan string juga bisa dilakukan dengan operator >=.


Less or equal than, <=


```
var1 <= var2

// apakah var1 bernilai lebih kecil atau sama dengan var2
```


Seperti operator >=, operator <= juga melakukan pengecekan nilai operand pertama dengan operand kedua. Operasi bernilai true jika operand pertama bernilai lebih kecil dari atau sama dengan operand kedua.


Perbandingan string juga dapat dilakukan oleh operator <=.



Membandingkan Object
Membandingkan object tidak semudah membandingkan tipe data primitif. Variabel yang mengandung object hanya menyimpan alamat memory, bukan nilai dari object itu sendiri sehingga jika Anda mengekspektasikan membandingkan kedua object dengan properties dan nilai yang sama menghasilkan true Anda perlu ingat lagi konsep tersebut. Perhatikan contoh dibawah ini.


Perlu diingat konsep Object-oriented bahwa object hanya simpan reference nya saja di variabel, bukan disimpan nilainya.
Bisa kita lihat obj1 dan obj2 memiliki properties dan nilai properties yang persis sama. Namun membandingkan kedua object tersebut akan menghasilkan false karena kedua object tersebut berbeda walaupun isinya sama. Anda bisa analogikan hal tersebut seperti jika Anda mempunyai kloning diri Anda sendiri yang sama persis. Anda dan kloning Anda tidak ada berbeda secara perilaku dan fisik tapi Anda tetap individu yang berbeda dengan kloning Anda. Aktivitas Anda tidak terikat dengan kloning Anda begitu juga sebaliknya.

Pada baris 15 saya melakukan assignment obj3 = obj1. Hal ini berarti bahwa copy alamat object pada obj1 ke obj3. Sehingga sekarang obj1 dan obj3 menunjuk pada alamat memori yang sama, alamat object yang sama. Oleh karena itu ketika dilakukan operasi perbandingan maka akan menghasilkan true. Hal ini bisa dianalogikan seperti Anda sekeluarga yang tinggal di rumah yang sama. Anda dan anggota keluarga lainnya akan merujuk ke alamat dan rumah yang sama jika ditanya dimana rumah Anda. Jika terjadi sesuatu pada rumah Anda, misalkan rumah Anda sedang di renovasi, anggota keluarga lain juga akan mengatakan rumah sedang direnovasi karena rumah mereka merujuk ke rumah yang sama dengan rumah Anda.

Analogi ini hanyalah analogi sederhana untuk mempermudah pemahaman Anda. Anda perlu berhati-hati dalam menentukan apakah Anda membandingkan object atau membandingkan properties dari object. Anda akan sangat jarang menemukan kasus Anda harus membandingkan dua buah object. Biasanya properties dari object yang dibandingkan untuk menentukan suatu pilihan.


**UPDATE**

Derajat Operator
Melanjutkan dari story sebelumnya pada operator matematika, derajat operator juga berlaku untuk


* Postfix Increment, x++
* Postfix Decrement, x —
* Prefix Increment, ++x
* Prefix Decrement, — x
* Perkalian, *
* Pembagian, /
* Modulus, %
* Penjumlahan, +
* Pengurangan, -
* Less than, <
* Less than or equal, <=
* Greater than, >
* Greater than or equal, >=
* Equality, ==
* Inequality, !=
* Strict equality, ===
* Strict inequality, !==

* n, <
* Less than or equal, <=
* Greater than, >
* Greater than or equal, >=
* Equality, ==
* Inequality, !=
* Strict equality, ===
* Strict inequality, !==
