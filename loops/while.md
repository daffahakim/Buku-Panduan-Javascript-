# While Loop

perulangan `while`, perulangan ini akan terus berulang selama kondisi yang ditentukan benar.

```javascript
while (kondisi) {
  //kode akan terus dilakukan selama kondisinya benar
}
```

sebagai contoh, kode dibawah ini akan terus berulang selama "i" masih kurang dari 5:

```javascript
var i = 0,
  x = "";
while (i < 5) {
  x = x + "Nomornya adalah " + i;
  i++;
}
```

**Catatan**: Berhati hatilah, untuk menghindari pengulangan yang tak terbatas jika kondisi selalu benar!

{% Latihan %}
dengan menggunakan perulangan `while`, buatlah variabel bernama `message` yang sama dengan gabungan bilangan bulat (0, 1, 2, ...) asalkan panjangnya (`message.length`) kurang dari 100.
{% mulai %}
var message = "";
{% solusi %}
var message = "";
var i = 0;

while (message.length < 100) {
message = message + i;
i = i + 1;
}
{% pembuktian %}
var message2 = "";
var i2 = 0;

while (message2.length < 100) {
message2 = message2 + i2;
i2 = i2 + 1;
}
assert(message === message2);
{% endexercise %}
