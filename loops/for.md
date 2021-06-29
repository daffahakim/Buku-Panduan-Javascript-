# For Loop

Bentuk perulangan yang paling mudah adalah for. ini memiliki sintaks seperti pernyataan if namun memiliki lebih banyak opsi:

```javascript
for (condition; end condition; change) {
    // do it, do it now
}
```

dibawah ini merupakan contoh cara menjalankan kode yang sama selama 10 kali dengan perulangan `for`:

```javascript
for (var i = 0; i < 10; i = i + 1) {
  // do this code ten-times
}
```

> **_Catatan_**: `i = i + 1` dapat ditulis `i++`.

{% latihan %}
menggunakan perulangan `for`, buatlah variabel  `message` yang sama dengan rangkaian bilangan bulat (0, 1, 2, ...) dari 0 sampai 99.

{% awalan %}
var message = "";

{% solusi %}
var message = "";

for(var i = 0; i < 100; i++){
message = message + i;
}
{% pembuktian %}
var message2 = ""

for(var i = 0; i < 100; i++){
message2 = message2 + i;
}
assert(message === message2);
{% akhir latihan %}
