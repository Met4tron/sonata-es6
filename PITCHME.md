# Palesterick

<br>
### Yuri Gomes

---

## O Que é ES6?

---

@title[Novas Funcionalidades]

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
var a = ["Hydrogen", "Helium", "Lithium", "Beryl­lium"];

var a2 = a.map(function(s) {
  return s.length;
});

var a3 = a.map(s => s.length);

// This Léxico

function Pessoa() {
  this.idade = 0;

  setInterval(() => {
    this.idade++; // propriedade |this|refere ao objeto pessoa
  }, 1000);
}

var p = new Pessoa();
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
```

---

@title[Default Arguments]

<p><span class="slide-title">Default Arguments</span></p>

```javascript
//ES5   
function multiplicar(a, b) {
  b = typeof b !== 'undefined' ?  b : 1;

  return a*b;
}
//ES6
multiplicar(5); // 5

function multiplicar(a, b = 1) {
  return a*b;
}

multiplicar(5); // 5
```

---

@title[Named Parameters]

<p><span class="slide-title">Named Parameters</span></p>

```javascript
```

---

@title[Rest]

<p><span class="slide-title">Rest</span></p>

```javascript
function multiplicar(multiplicador, ...args) {
  return args.map(x => multiplicador * x);
}

var arr = multiplicar(2, 1, 2, 3);
console.log(arr); // [2, 4, 6]
```

---

@title[Spread]

<p><span class="slide-title">Spread</span></p>

```javascript
```

---

@title[Classes]

<p><span class="slide-title">Async/Await</span></p>

```javascript
```

---

@title[Arrays]

<p><span class="slide-title">Arrays</span></p>

```javascript
for (let i of arr) {
   console.log(i); // logs "3", "5", "7"
}
```

---

@title[Loops]

<p><span class="slide-title">Loops</span></p>

```javascript
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

@title[WeakSet]

<p><span class="slide-title">WeakSet</span></p>

```javascript
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

for (var [key, value] of sayings) {
  console.log(key + " goes " + value);
}
// "cat goes meow"
// "elephant goes toot"

sayings.clear();
sayings.size; // 0
```

---

@title[WeakMap]

<p><span class="slide-title">WeakMap</span></p>

```javascript
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
