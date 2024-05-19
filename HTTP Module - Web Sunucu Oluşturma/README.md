### HTTP Module kullanarak Kendi Web Sunucumuzu yazalım.
* CreateServer metodunu kullanacağız.
* Index, hakkimda ve iletisim sayfaları oluşturalım.
* Sayfalara içerik olarak xxx sayfasına hoşgeldiniz şeklinde h1 başlıkları yazdıralım.
* Port numarası olarak 5000'i kullanalım.


```JavaScript
const http = require('http');

const server = http.createServer((req, res) => {

    const url = req.url;

    if (url === '/') {
        res.write('<h1>Ana Sayfa</h1>')
    }
    else if (url === '/index') {
        res.write('<h1>Index sayfasina hos geldiniz.</h1>')
    }
    else if (url === '/hakkimda') {
        res.write('<h1>Hakkimda sayfasina hos geldiniz.</h1>')
    }
    else if (url === '/iletisim') {
        res.write('<h1>Iletisim sayfasina hos geldiniz.</h1>')
    }
    else {
        res.write('<h1>404 Not Found</h1>')
    }

    res.end();

});


const port = 5000;

server.listen(port, () => {
    console.log(`Sunucu port ${port} baslatildi`);
});
```

