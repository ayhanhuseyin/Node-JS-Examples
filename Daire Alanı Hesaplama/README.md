### Node.JS Daire Alanı Hesaplama
Merhabalar, bu çalışmamızda daire alanı hesaplama ile ilgili bir örnek yapacağız. Hepimizin Matematik derslerinden bildiği üzere Dairenin Alanı = π x r2 şeklinde hesaplanır. Node.JS Javascript çalışma ortamında yarıçap değerini konsoldan parametre olarak girerek alanı bulmaya çalışacağız. Konsol çıktısı: Yarıçapı (Yarıçap) olan dairenin alanı: (Alan) şeklinde olmalıdır.

```JavaScript
const args = process.argv.slice(2);

if (args.length === 0) {
    console.log('Lütfen bir yarıçap değeri girin.');
    process.exit(1);
}

const radius = parseFloat(args[0]);


if (isNaN(radius) || radius <= 0) {
    console.log('Lütfen geçerli bir yarıçap değeri girin.');
    process.exit(1);
}

const pi = Math.PI;
const area = pi * 2 * radius;

console.log(`Yarıçapı (${radius}) olan dairenin alanı: ${area})`);

```
