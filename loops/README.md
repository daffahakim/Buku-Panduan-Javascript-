# Perulangan

Loops (perulangan) adalah kondisi dimana satu variabel dalam suatu perulangan berubah dan akan terus berulang sampai kondisi yang diinginkan tercapai, loop digunakan jika kamu ingin menggunakan kode yang sama secara berulang ulang, setiap kali dengan nilai yang berbeda

contoh menuliskan kode yang sama tanpa menggunakan perulangan :

```javascript
doThing(cars[0]);
doThing(cars[1]);
doThing(cars[2]);
doThing(cars[3]);
doThing(cars[4]);
```

dengan perulangan kamu dapat menulisnya lebih sinkgat, contoh :

```javascript
for (var i = 0; i < cars.length; i++) {
  doThing(cars[i]);
}
```
