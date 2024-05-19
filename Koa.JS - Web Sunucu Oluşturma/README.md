### Koa.js ile web sunucumuzu yazalım.
* Koa paketini indirelim.
* Index, hakkimda ve iletisim sayfaları oluşturalım.
* Sayfalara içerik olarak xxx sayfasına hoşgeldiniz şeklinde h1 başlıkları yazdıralım.
* Port numarası olarak 3000'i kullanalım.


```Terminal
npm init
npm i koa
npm i koa-router
```

```JavaScript
const Koa = require('koa');
const Router = require('koa-router');
const app = new Koa();
const router = new Router();

app.use(router.routes());

router.get('/index', ctx => {
    ctx.body = '<h1>Index sayfasina hos geldiniz</h1>'
})

router.get('/hakkimda', ctx => {
    ctx.body = '<h1>Hakkimda sayfasina hos geldiniz</h1>'
})

router.get('/iletisim', ctx => {
    ctx.body = '<h1>Iletisim sayfasina hos geldiniz</h1>'
})


const port = 3000
app.listen(port, () => {
    console.log(`Sunucu ${port} portunda baslatildi`);
});
```
