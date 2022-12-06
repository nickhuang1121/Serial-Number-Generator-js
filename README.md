# Serial-Number-Generator-js
能夠自動產生序號的javascript，可以設定大小寫、數字、分組...等。

# Installation
<script src="serial-number-generator.js"></script>

## JavaScript
### Fast Use
```javascript
let SN = serialNumberGenerator();
```
### Detailed settings
```javascript
let SN = serialNumberGenerator(
    {
        SNLength: 20, //serial Length
        useUpperCase: true, // UpperCase
        useLowerCase: true, // LowerCas
        useNumber: true, // Number
        group: 4, // Text grouping
        quantity: "10" // How many serial numbers to generate
    }
);
```


## Sample Demo
### Html
```html
<ul id="list"></ul>
<script src="serial-number-generator.js"></script>
```

### JavaScript
```javascript
let SN = serialNumberGenerator(
    {
        SNLength: 20, //serial Length
        useUpperCase: true, // UpperCase
        useLowerCase: true, // LowerCas
        useNumber: true, // Number
        group: 4, // Text grouping
        quantity: "10" // How many serial numbers to generate
    }
);

let list = document.querySelector("#list");
let li = "";

SN.forEach(function (i) {
    li += `<li>${i}</li>`
});
list.innerHTML = li;
```

