### Express.js ile web sunucumuzu yazalım.
* Express paketini indirelim.
* Index, hakkimda ve iletisim sayfaları oluşturalım.
* Sayfalara içerik olarak xxx sayfasına hoşgeldiniz şeklinde h1 başlıkları yazdıralım.
* Port numarası olarak 3000'i kullanalım.

```Terminal
npm init
npm i express
```

```JavaScript
const express = require('express');
const app = express();

app.get('/index', (req, res) => {
    res.send('<h1>Index sayfasina hos geldiniz.</h1>')
})

app.get('/hakkimda', (req, res) => {
    res.send('<h1>Hakkimda sayfasina hos geldiniz.</h1>')
})

app.get('/iletisim', (req, res) => {
    res.send('<h1>Iletisim sayfasina hos geldiniz.</h1>')
})

app.get('*', (req, res) => {
    res.send('404 Not Found')
})


const port = 3000;

app.listen(port, () => {
    console.log(`Sunucu ${port} portunda calisiyor.`);
});
```
