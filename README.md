# START KIT SASS

## 📂 Cấu trúc thư mục
```
start-kit-sass
├── .vscode
│   └── settings.json
├── assets
│   ├── css/
│   ├── font/
│   ├── icon/
│   ├── img/
│   └── js/
├── scss
│   ├── base/
│   ├── layout/
│   ├── pages/
│   └── style.scss
├── vendor
│   ├── bootstrap-4.5.3/
│   ├── bootstrap-table/
│   ├── _jquery.min.js
│   ├── moment.min.js
│   └── popper.min.js
├── index.html
├── .gitignore
└── README.md
```
## Setup

Nếu dùng **Visual Studio Code** hãy cài các extensions này.
- **watch sass:** để compile file scss/sass thành css (dưới đây là config setting cho watch sass).
```
"liveSassCompile.settings.formats": [

    {
        "format": "expanded",
        "extensionName": ".css",
        "savePath": "/assets/css"
    }
],
"liveSassCompile.settings.generateMap": true,
```
- **prettier formater:** Để format code html, config 150 tức là độ dài 1 dòng nếu hơn sẽ xuống dòng.
```
"prettier.printWidth": 150,
```
- **Beautify css/sass/scss/less:** format file scss/sass, Nên format đê cho dễ nhìn.

Các config này nằm trong folder 
```
├── .vscode
│   └── settings.json
``` 
ở gốc thư mục. Nếu chưa có thì hãy tạo nó.
## Folder assets
- **css/:** file css khi được compile từ file scss.
- **font/:** chứa font của dự án.
- **icon/:** Chứa icon của dự án.
- **img/:** Chứa các hình ảnh.
- **js/:** Chứa các file javascript, Mỗi trang sẽ import một file javascript riêng của trang đó.
## Folder scss
### base:
- **element:/** Nơi để các style chung global, như style của button chính, input custom, radio custom...
- **lib/:** File để custom các style của các thư viện.
- **mixins/:** File bao gồm các mixins để kế thừa. Những style hay được dùng đi dùng lại thì sẽ viết thành mixins để dùng lại cho nhanh và tiện.
- **reset/:** File reset các style mặc định của các trình duyệt nếu cần.
- **variables/:** Biến global được dùng trong dự án.nm
### layout:
- **layout.scss:** file chưa layout như style của container, container-fluid...
- Chứa các layout chung của nhiều trang như ```header```  

Tạo một trang mới trong ```pages/``` sau đó import trong file ```style.scss```. **Lưu ý:** Tên file có dấu ```_``` để không compile file đó, chỉ cần compile file ```style.scss```.
## Folder vendor: 
Chứa các thư viện hoặc plugin bên ngoài như boostrap, jquery...