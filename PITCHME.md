# Palesterick

<br>
![firstGif](https://media.giphy.com/media/WiM5K1e9MtEic/giphy.gif)
<br>
#### Yuri Gomes

---

## O Que é ES6?

<br>
![](https://media.giphy.com/media/l1J9DGe9KBzJOq5Nu/giphy.gif)

---

## Novas Funcionalidades

---

@title[Let]

<p><span class="slide-title">Let</span></p>
<br>
Declara uma variável local de escopo do bloco, opcionalmente inicializando-a com um valor.

```javascript
//ES5
if (true) {
  var x = 5;
}

console.log(x); //5

//ES6
if (true) {
  let y = 5;
}
console.log(y); // ReferenceError: y não está definido
```

---

@title[Const]

<p><span class="slide-title">Const</span></p>
<br>
Declara uma constante apenas de leitura.

```javascript
// Isto irá causar um  erro
function f() {}
const f = 5;

// Isto também irá causar um erro.
function f() {
  const g = 5;
  var g;

  //declarações
}
```

---

@title[Arrow Functions]

<p><span class="slide-title">Arrow Functions</span></p>

```javascript
var arr = [1, 2, 3];
var squares = arr.map(function (x) { return x * x });
```
---

<p><span class="slide-title">Arrow Functions</span></p>

```javascript
const arr = [1, 2, 3];
const squares = arr.map(x => x * x);

```
---

<p><span class="slide-title">Arrow Functions</span></p>

```javascript
function UiComponent() {
    var _this = this; // (A)
    var button = document.getElementById('myButton');
    button.addEventListener('click', function () {
        console.log('CLICK');
        _this.handleClick(); // (B)
    });
}
UiComponent.prototype.handleClick = function () {
    ···
};

```
---

<p><span class="slide-title">Arrow Functions</span></p>

```javascript

function UiComponent() {
    var button = document.getElementById('myButton');
    button.addEventListener('click', () => {
        console.log('CLICK');
        this.handleClick(); // (A)
    });
}

```
---

@title[Template String]

<p><span class="slide-title">Template String</span></p>

```javascript
//ES5
var a = 5;
var b = 10;
console.log("Quinze é " + (a + b) + " e\nnão " + (2 * a + b) + ".");
// "Quinze é 15 e
// não 20."
```
---

<p><span class="slide-title">Template String</span></p>

```javascript
//ES6
var a = 5;
var b = 10;
console.log(`Quinze é ${a + b} e\nnão ${2 * a + b}.`);
// "Quinze é 15 e
// não 20."
```

---

@title[Destructuring Assignment]

<p><span class="slide-title">Destructuring Assignment</span></p>

```javascript
const atributosPersonagem = {
  forca: 20,
  mentalidade: 40,
  resistencia: 10
};

let { forca, mentalidade } = atributosPersonagem;
console.log(forca);//20
console.log(mentalidade);//40
```

---

@title[Default Arguments]

<p><span class="slide-title">Default Parameters</span></p>

```javascript
//ES5
function multiplicar(a, b) {
  b = typeof b !== "undefined" ? b : 1;

  return a * b;
}

multiplicar(5); // 5
```

---

<p><span class="slide-title">Default Parameters </span></p>

```javascript
// ES6
function multiplicar(a = 10, b = 1) {
  return a * b;
}
multiplicar()//10
multiplicar(5); // 5
```

---

@title[Named Parameters]

<p><span class="slide-title">Named Parameters</span></p>

```javascript
//ES5

function selectEntries(options) {
  options = options || {};
  var start = options.start || 0;
  var end = options.end || -1;
  var step = options.step || 1;
}
```

---

<p><span class="slide-title">Named Parameters</span></p>

```javascript
function selectEntries({ start = 0, end = -1, step = 1 } = {}) {}
```

---

<p><span class="slide-title">Named Parameters</span></p>

```javascript
```

---

@title[Rest]

<p><span class="slide-title">Rest</span></p>

```javascript
var arr1 = ["a", "b"];
var arr2 = ["c"];
var arr3 = ["d", "e"];

console.log(arr1.concat(arr2, arr3)); // [ 'a', 'b', 'c', 'd', 'e' ]
```

---

<p><span class="slide-title">Rest</span></p>

```javascript
const arr1 = ["a", "b"];
const arr2 = ["c"];
const arr3 = ["d", "e"];

console.log([...arr1, ...arr2, ...arr3]);
// [ 'a', 'b', 'c', 'd', 'e' ]
```

@title[Object Literals]

<p><span class="slide-title">Object Literals</span></p>

```javascript
var obj = {
    foo: function () {
        ···
    },
    bar: function () {
        this.foo();
    }, // trailing comma is legal in ES5
}
```
---

```javascript
const obj = {
    foo() {
        ···
    },
    bar() {
        this.foo();
    },
}
```
---

@title[Classes]

<p><span class="slide-title">Async/Await</span></p>

```javascript
class Carro {
  constructor() {
    this.cor = "Vermelho";
    this.marca = "Volkswagen";
    this.ano = "2018";
  }

  marca() {
    return console.log(`A marca do carro é ${this.marca}`);
  }
}
```

---

@title[Arrays]

<p><span class="slide-title">Arrays</span></p>

```javascript
//for..of
const arr = ['a', 'b', 'c'];
for (const elem of arr) {
    console.log(elem);// a , b , c
}
```
---

<p><span class="slide-title">Arrays</span></p>

```javascript
//Array.fill()
let arr = [1, 2, 3, 4, 5];
arr.fill(2); // [2, 2, 2, 2, 2]
```

---

@title[Symbols]

<p><span class="slide-title">Symbols</span></p>

```javascript
```

---

@title[Set]

<p><span class="slide-title">Set</span></p>

```javascript
var mySet = new Set();
mySet.add(1);
mySet.add("some text");
mySet.add("foo");

mySet.has(1); // true
mySet.delete("foo");
mySet.size; // 2

for (let item of mySet) console.log(item);
// 1
// "some text
```

---

@title[Map]

<p><span class="slide-title">Map</span></p>

```javascript
var sayings = new Map();
sayings.set("dog", "woof");
sayings.set("cat", "meow");
sayings.set("elephant", "toot");
sayings.size; // 3
sayings.get("fox"); // undefined
sayings.has("bird"); // false
sayings.delete("dog");
sayings.has("dog"); // false
sayings.get("cat"); // meow
sayings.get("elephant"); //toot

for (var [key, value] of sayings) {
  console.log(key + " goes " + value);
};
// "cat goes meow"
// "elephant goes toot"

sayings.clear();
sayings.size; // 0
```

---

@title[Generators]

<p><span class="slide-title">Generators</span></p>

```javascript
```

---

@title[Typescript]

<p><span class="slide-title">Typescript</span></p>

```javascript
```

---

@title[Transpiladores]

<p><span class="slide-title">Transpiladores</span></p>

```javascript
```

---

@title[Obrigado]

## Obrigado

![](https://media.giphy.com/media/mQG644PY8O7rG/giphy.gif)
