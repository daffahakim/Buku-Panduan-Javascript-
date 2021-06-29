# Perulangan Do...While 

do...while perulangan yang menjalankan pernyataan tertentu hingga kondisi pengujian bernilai salah (false). kondisi dievaluasi setelah menjalankan pernyataan

Sintaks untuk do... while adalah:

```javascript
do {
  // Pernyataan
} while (kondisi);
```

sebagai contoh, dibawah ini cara mencetak angka sampai kurang dari 10 dengan perulangan `do...while`:

```javascript
var i = 0;
do {
  document.write(i + " ");
  i++; // incrementing i by 1
} while (i < 10);
```

> **_Catatan_**: `i = i + 1` dapat ditulis `i++`.

{% Latihan %}
Menggunakan perulangan `do...while`, cetaklah angka sampai kurang dari 5.
{% Mulai %}
var i = 0;
{% Solusi %}
var i = 0;
do {
i++; // menambah i dengan 1
} while (i < 5);
{% AkhirLatihan %}
