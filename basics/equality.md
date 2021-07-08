#Persamaan

Bahasa pemorgraman perlu menentukan kesetaraan satu variabel dengan variabel lain. Ini dilakukan dengan menggunakan operator persamaan.

Operator persamaan paling dasar adalah operator `==`. Operator ini melakukan segalanya untuk menentukan apakah dua variabel sama, bahkan jika mereka tidak bertipe sama.

Misalnya, kita asumsikan:

```javascript
var foo = 42;
var bar = 42;
var baz = "42";
var qux = "life";
```

`foo == bar` akan dievaluasi menjadi `true` dan `baz == qux` akan dievaluasi menjadi `false`, seperti yang diharapkan. Namun, `foo == baz` akan _juga_ dievaluasi menjadi `true` meskipun `foo` dan `baz` berbeda tipe. Di balik layar, operator kesetaraan `==` mencoba memaksa operandnya ke tipe yang sama sebelum menentukan kesetaraannya. Ini berbeda dengan operator persamaan `===`.

Operator persamaan `===` menentukan bahwa dua variabel adalah sama jika mereka bertipe sama _dan_ memiliki nilai yang sama. Dengan asumsi yang sama seperti sebelumnya, ini berarti `foo === bar` masih akan dievaluasi ke `true`, tetapi `foo === baz` sekarang akan dievaluasi ke `false`. `baz === qux` masih akan dievaluasi menjadi `false`.
