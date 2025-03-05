Le **template strings** (o **template literals**) in JavaScript sono una funzionalità che ti permette di scrivere stringhe in modo più potente ed espressivo. Ecco una panoramica delle caratteristiche principali:

### 1. **Sintassi base con backticks**

Le **template strings** sono delimitate dai caratteri **backticks** (accent grave) ``` anziché dalle virgolette doppie `"` o singole `'`.

```jsx
javascript
Copia
let nome = "Giovanni";
let saluto = `Ciao, ${nome}!`;
console.log(saluto);  // Stampa: "Ciao, Giovanni!"

```

### 2. **Interpolazione delle variabili**

Puoi inserire variabili direttamente all'interno della stringa utilizzando un ESAPE: `${}`. Non è più necessario concatenare le stringhe con `+`.

```jsx
javascript
Copia
let nome = "Maria";
let eta = 25;
let frase = `Mi chiamo ${nome} e ho ${eta} anni.`;
console.log(frase);  // Stampa: "Mi chiamo Maria e ho 25 anni."

```

### 3. **Stringhe multilinea**

Le **template strings** supportano la scrittura di stringhe su più righe senza bisogno di utilizzare caratteri di escape come `\\n`.

```jsx
javascript
Copia
let messaggio = `Ciao,
come va?`;
console.log(messaggio);
// Stampa:
// Ciao,
// come va?

```

### 4. **Esecuzione di espressioni**

Puoi anche eseguire espressioni direttamente all'interno della stringa usando `${}`.

```jsx
javascript
Copia
let x = 5;
let y = 10;
let somma = `La somma di ${x} e ${y} è ${x + y}.`;
console.log(somma);  // Stampa: "La somma di 5 e 10 è 15."

```

### 5. **Tagging delle template strings**

Le **template strings** possono essere utilizzate con una funzione chiamata **tag**, che ti permette di personalizzare il comportamento della stringa.

Esempio di una funzione tag:

```jsx
javascript
Copia
function grassetto(strings, ...values) {
  let risultato = strings[0];
  values.forEach((valore, i) => {
    risultato += `<b>${valore}</b>` + strings[i + 1];
  });
  return risultato;
}

let nome = "Francesca";
let messaggio = grassetto`Ciao, ${nome}!`;
console.log(messaggio);  // Stampa: "Ciao, <b>Francesca</b>!"

```

### 6. **Funzioni dentro le template strings**

Puoi anche chiamare funzioni o eseguire logiche più complesse all'interno di `${}`.

```jsx
javascript
Copia
function saluta(nome) {
  return `Ciao, ${nome}!`;
}

let nome = "Anna";
let saluto = `Benvenuta, ${saluta(nome)} Come stai?`;
console.log(saluto);  // Stampa: "Benvenuta, Ciao, Anna! Come stai?"

```

### Vantaggi delle Template Strings:

- **Maggiore leggibilità**: permettono di scrivere codice più chiaro e compatto.
- **Facilità di interpolazione**: variabili e espressioni possono essere inserite direttamente nella stringa senza concatenazione.
- **Supporto per multilinea**: non è necessario preoccuparsi dei caratteri di escape per andare a capo.
- **Flessibilità**: puoi eseguire operazioni o chiamare funzioni all'interno delle stringhe.

In sintesi, le **template strings** rendono la gestione delle stringhe in JavaScript più potente e leggibile, specialmente quando si lavora con variabili e formattazione di testo.