### Post Sıralama
Bu çalışmamızda **Async-Awaıt** yapısı kullanarak post sıralama işlemi gerçekleştireceğiz. Postları Fake REST API sunan JSONPlaceholder sitesinden alıcağız. Siteye [Buradan](https://jsonplaceholder.typicode.com/) erişebilirsinz. 

```JavaScript
async function getUsers() {
    try {
        const users = await (await fetch("https://jsonplaceholder.typicode.com/users")).json();
        console.log(users);
    }
    catch (error) {
        console.log(error);
    }
};

getUsers();
```
