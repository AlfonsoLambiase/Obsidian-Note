I **metodi degli array** sono **funzioni** che puoi usare per fare delle operazioni sugli **array**. Gli array sono come delle **liste** e i metodi ti aiutano a **manipolarle**.

Ecco i metodi più facili e utili degli array!

### 1. **`push()`** — Aggiungere un elemento alla fine dell'array

Questo metodo aggiunge un nuovo elemento alla fine dell'array.

```jsx
javascript
Copia
let numeri = [1, 2, 3];
numeri.push(4);  // Aggiunge "4" alla fine
console.log(numeri);  // Risultato: [1, 2, 3, 4]

```

### 2. **`pop()`** — Rimuovere l'ultimo elemento dell'array

Questo metodo rimuove l'ultimo elemento dall'array.

```jsx

let numeri = [1, 2, 3];
numeri.pop();  // Rimuove "3"
console.log(numeri);  // Risultato: [1, 2]

```

### 3. **`shift()`** — Rimuovere il primo elemento dell'array

Questo metodo rimuove il primo elemento dall'array.

```jsx

let numeri = [1, 2, 3];
numeri.shift();  // Rimuove "1"
console.log(numeri);  // Risultato: [2, 3]

```

### 4. **`unshift()`** — Aggiungere un elemento all'inizio dell'array

Questo metodo aggiunge un nuovo elemento all'inizio dell'array.

```jsx
let numeri = [2, 3];
numeri.unshift(1);  // Aggiunge "1" all'inizio
console.log(numeri);  // Risultato: [1, 2, 3]

```

### 5. **`forEach()`** — Fare qualcosa con ogni elemento dell'array

Il metodo `forEach()` in JavaScript è un metodo molto utile che ti consente di **iterare** su ogni elemento di un array . È una forma più concisa di scrivere un ciclo `for` e permette di eseguire una funzione su ciascun elemento dell'array.

```jsx
array.forEach(function(elemento, indice, array) {
    // codice da eseguire per ogni elemento
});

```

- **`elemento`**: è l'elemento corrente dell'array che viene passato alla funzione.
- **`indice`** (opzionale): è l'indice dell'elemento corrente nell'array (puoi ignorarlo se non ti serve).
- **`array`** (opzionale): è l'array su cui è stato chiamato `forEach` (puoi ignorarlo se non ti serve).

### 6. **`slice()`**

Restituisce una **copia parziale** di un array, senza modificarlo. Puoi specificare l'indice di inizio e di fine.

```jsx

let arr = [1, 2, 3, 4, 5];
let sottoArray = arr.slice(1, 4);  // Prende gli elementi da indice 1 a 3
console.log(sottoArray);  // [2, 3, 4]

```

### 7. **`splice()`**

Rimuove o sostituisce gli elementi in un array e può anche aggiungerne di nuovi. Modifica l'array originale.

```jsx

let arr = [1, 2, 3, 4, 5];
arr.splice(2, 2, 'a', 'b');  // Rimuove 2 elementi a partire dall'indice 2 e aggiunge 'a' e 'b'
console.log(arr);  // [1, 2, 'a', 'b', 5]

```

### 8. **`map()`**

Crea un nuovo array con i risultati della funzione applicata a ogni elemento dell'array.

```jsx

let arr = [1, 2, 3];
let raddoppiati = arr.map(num => num * 2);
console.log(raddoppiati);  // [2, 4, 6]

```

### 9. **`filter()`**

Restituisce un nuovo array con gli elementi che passano un test (cioè che soddisfano una condizione).

```jsx

let arr = [1, 2, 3, 4, 5];
let pari = arr.filter(num => num % 2 === 0);
console.log(pari);  // [2, 4]

```

### 10. **`find()`**

Restituisce il **primo elemento** che soddisfa la condizione specificata.

```jsx
javascript
Copia
let arr = [1, 2, 3, 4];
let trovato = arr.find(num => num > 2);
console.log(trovato);  // 3

```

### 11. **`findIndex()`**

Restituisce l'indice del **primo elemento** che soddisfa una condizione.

```jsx

let arr = [10, 20, 30];
let indice = arr.findIndex(num => num > 15);
console.log(indice);  // 1

```

### 12. **`join()`**

Restituisce una stringa composta da tutti gli elementi dell'array, uniti da un separatore specificato.

```jsx

let arr = [1, 2, 3];
let joined = arr.join('-');
console.log(joined);  // "1-2-3"

```

### 13. **reduce()**

Riduce un array a un singolo valore applicando una funzione su ciascun elemento.

```jsx
javascript
Copia
let arr = [1, 2, 3];
let sum = arr.reduce((acc, curr) => acc + curr, 0);  // sum diventa 6

```

### 14. **reverse()**

Invertisce l'ordine degli elementi dell'array.

```jsx
javascript
Copia
let arr = [1, 2, 3];
arr.reverse();  // arr diventa [3, 2, 1]

```

### 15. **some()**

Verifica se almeno un elemento dell'array soddisfa una condizione.

```jsx
javascript
Copia
let arr = [1, 2, 3];
let hasEven = arr.some(x => x % 2 === 0);  // hasEven diventa true

```

### 16. **includes()**

Verifica se un elemento è presente nell'array, restituendo `true` o `false`.

```jsx
javascript
Copia
let arr = [1, 2, 3];
let hasTwo = arr.includes(2);  // hasTwo diventa true

```

### 17. **sort()**

Ordina gli elementi di un array in ordine crescente (di default) o in ordine personalizzato.

```jsx
javascript
Copia
let arr = [3, 1, 4, 2];
arr.sort();  // arr diventa [1, 2, 3, 4]

```

### Sintesi:

- **`push()`** – Aggiunge uno o più elementi alla fine di un array.
- **`pop()`** – Rimuove e restituisce l'ultimo elemento di un array.
- **`shift()`** – Rimuove e restituisce il primo elemento di un array.
- **`unshift()`** – Aggiunge uno o più elementi all'inizio di un array.
- **`concat()`** – Unisce due o più array in uno nuovo.
- **`slice()`** – Restituisce una copia parziale di un array (senza modificarlo).
- **`splice()`** – Rimuove, sostituisce o aggiunge elementi a un array (modifica l'array originale).
- **`forEach()`** – Esegue una funzione su ogni elemento dell'array.
- **`map()`** – Restituisce un nuovo array con i risultati di una funzione applicata a ogni elemento.
- **`filter()`** – Restituisce un array con gli elementi che soddisfano una condizione.
- **`reduce()`** – Riduce l'array a un singolo valore, applicando una funzione su ogni elemento.
- **`reduceRight()`** – Come `reduce()`, ma lavora da destra a sinistra.
- **`some()`** – Verifica se almeno un elemento soddisfa una condizione.
- **`every()`** – Verifica se tutti gli elementi soddisfano una condizione.
- **`find()`** – Restituisce il primo elemento che soddisfa una condizione.
- **`findIndex()`** – Restituisce l'indice del primo elemento che soddisfa una condizione.
- **`includes()`** – Verifica se un elemento esiste nell'array.
- **`sort()`** – Ordina gli elementi di un array.
- **`reverse()`** – Inverte l'ordine degli elementi di un array.
- **`join()`** – Unisce gli elementi dell'array in una stringa.