Lo **scope** definisce **dove puoi usare una variabile** nel tuo programma. Quando una variabile è "dentro" una funzione, è visibile solo all'interno di quella funzione (questo è lo **scope locale**). Le variabili fuori dalla funzione sono visibili in tutto il programma (questo è lo **scope globale**).

### Esempio di **scope locale**:

```jsx
javascript
Copia
function miaFunzione() {
    let x = 10;  // x è visibile solo dentro questa funzione
    console.log(x);  // Funziona, stampa 10
}

miaFunzione();
console.log(x);  // Errore! x non è definita fuori dalla funzione

```

### Esempio di **scope globale**:

```jsx
javascript
Copia
let y = 20;  // y è una variabile globale

function miaFunzione() {
    console.log(y);  // y è visibile dentro la funzione perché è globale
}

miaFunzione();  // Funziona, stampa 20
console.log(y);  // Funziona, stampa 20

```

### In breve:

- Le variabili **globali** sono accessibili ovunque.
- Le variabili **locali** sono accessibili solo dentro la funzione dove sono state create