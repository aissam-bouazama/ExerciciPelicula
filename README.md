
# 📄 Documentació de proves per la classe `Peli`

Aquest document conté proves per la classe `Peli` importada des de `llibreria27.js`. Les proves inclouen verificacions per diferents errors i casos especials, com errors en el format dels atributs, cadenes buides i altres possibles valors incorrectes.

## 📥 Importació

```javascript
import { Peli } from "./llibreria27.js";
```

## 🔍 Proves de l'ID
### 1. ID incorrecte (no compleix el format)
```javascript
const peli = new Peli({
  id: "y1234567y",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli);
```
### 2. ID en format numèric
```javascript
const peli1 = new Peli({
  id: 1234567,
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli1);
```
### 3. ID buit
```javascript
const peli2 = new Peli({
  id: "",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli2);
```

## 🔍 Proves del Títol
### 1. Títol numèric
```javascript
const peli3 = new Peli({
  id: "yy1234567",
  titol: 17171,
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli3);
```
### 2. Títol buit
```javascript
const peli4 = new Peli({
  id: "yy1234567",
  titol: "",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli4);
```
### 3. Títol de més de 100 caràcters
```javascript
const peli5 = new Peli({
  id: "yy1234567",
  titol: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, deleniti...",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli5);
```

## 🔍 Proves del Director
### 1. Director amb més de 50 caràcters
```javascript
const peli6 = new Peli({
  id: "yy1234567",
  titol: "thor.",
  director: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, deleniti...",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli6);
```
### 2. Director buit
```javascript
const peli7 = new Peli({
  id: "yy1234567",
  titol: "thor.",
  director: "",
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli7);
```
### 3. Director en format numèric
```javascript
const peli8 = new Peli({
  id: "yy1234567",
  titol: "thor.",
  director: 1212,
  any: 2011,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peli8);
```

## 🔍 Proves de l'Any
### 1. Any en format de cadena
```javascript
const peliany = new Peli({
  id: "yy1234567",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: "2011",
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peliany);
```
### 2. Any amb més de 4 dígits
```javascript
const peliany1 = new Peli({
  id: "yy1234567",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 20111,
  pais: ["Catalunya", "Andorra"],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(peliany1);
```

## 🔍 Proves del País
### 1. País en format de cadena
```javascript
const pelipais = new Peli({
  id: "yy1234567",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 2011,
  pais: "Catalunya",
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(pelipais);
```
### 2. País amb un número en l'array
```javascript
const pelipais1 = new Peli({
  id: "yy1234567",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra", 1],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(pelipais1);
```
### 3. País amb un element buit
```javascript
const pelipais2 = new Peli({
  id: "yy1234567",
  titol: "Thor",
  director: "Kenneth Branagh",
  any: 2011,
  pais: ["Catalunya", "Andorra", ""],
  generes: ["Adult", "Comedy"],
  qualificacions: 7.4,
});
console.log(pelipais2);
```
