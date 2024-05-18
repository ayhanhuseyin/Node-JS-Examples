### FS File System
Bu çalışmamızda Node.js FS Modülü kullanarak 4 adet çalışma yapapacağız.

### 1. Dosya oluşturma
Employees.json dosyası oluşturalım ve içerisine {"name": "Employee 1 Name", "salary": 2000} verisini ekleyelim.

```JavaScript
const fs = require('fs');

fs.writeFile('employees.json', '{"name": "Employee 1 Name", "salary": 2000}', 'utf-8', (err) => {
    if (err) {
        console.log("JSON dosyasi olusturulamadi");
    }
    console.log("JSON dosyasi olusturuldu.");
});
```

### 2. Veri okuma

```JavaScript
const fs = require('fs');

fs.readFile('employees.json', 'utf-8', (err, data) => {
    if (err) {
        console.log("Dosya okunamadi");
    }
    console.log(data);
});
```

### 3. Veri Güncelleme

```JavaScript
const fs = require('fs');

fs.appendFile('employees.json', '\nYeni veriler', 'utf-8', (err) => {
    if (err) {
        console.log("Veri guncellenemedi");
    }
    console.log("Veriler guncellendi");
});
```

### 4. Dosya silme

```JavaScript
const fs = require('fs');

fs.unlink('employees.json', (err) => {
    if (err) {
        console.log("Dosya silinemedi");
    }
    console.log("Dosya basariyla silindi");
});
```
