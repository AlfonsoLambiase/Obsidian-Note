In JavaScript, **`async`** e **`await`** sono delle parole chiave che rendono più semplice lavorare con le operazioni asincrone, come quelle che utilizzano le **Promises**.

### `async`:

Quando metti la parola chiave **`async`** davanti a una funzione, quella funzione diventa una funzione asincrona. Una funzione asincrona restituirà automaticamente una **Promise**, anche se non la scrivi esplicitamente. Questo ti permette di usare **`await`** all'interno di quella funzione.

### `await`:

La parola chiave **`await`** ti permette di "aspettare" che una **Promise** venga risolta prima di andare avanti con il codice. Si può usare solo dentro una funzione **`async`**.

### Esempio semplice:

```
`// Funzione che simula una promessa asincrona`
`function ordinaPizza() {`
  `return new Promise(resolve => {`
    `setTimeout(() => resolve("Pizza pronta!"), 2000); // Simula il tempo per preparare la pizza (2 secondi)`
  `});`
`}`

`// Funzione asincrona che usa await`
`async function mangiaPizza() {`
  `console.log("Sto aspettando la pizza...");`
  
  `// Usa await per aspettare che la promessa venga completata`
  `let risultato = await ordinaPizza();`
  
  `console.log(risultato); // Verrà stampato dopo 2 secondi`
`}`

`mangiaPizza();  // Inizia l'operazione di ordinare e mangiare la pizza`
```


### Cosa succede in questo esempio:

- Quando esegui il codice, vedrai prima "Sto aspettando la pizza...", poi dopo 2 secondi vedrai "Pizza pronta!".
- Il codice usa **`await`** per attendere che la promessa (simulata dalla funzione `ordinaPizza`) venga completata prima di continuare l'esecuzione.

### Perché usare `async` e `await`?

- **Leggibilità:** Il codice diventa più chiaro e simile a un flusso lineare, invece di avere tanti **.then()** annidati.
- **Gestione delle operazioni asincrone più semplice:** Non c'è bisogno di gestire manualmente i callback o le promesse una dopo l'altra.

### Riepilogo:

- **`async`** rende una funzione asincrona (ritorna una Promise).
- **`await`** "attende" la Promise dentro una funzione asincrona, sospendendo il codice finché non è pronta.

In sostanza, **`async`** e **`await`** ti permettono di scrivere codice asincrono che sembra più semplice e facile da seguire.