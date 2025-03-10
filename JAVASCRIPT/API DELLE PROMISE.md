Ci sono metodi utilizzati per lavorare con **Promise** in JavaScript, e ti permettono di gestire operazioni asincrone in modo più efficiente. Vediamo di spiegare ognuno di questi:

### 1. `Promise.all()`

`Promise.all()` è un metodo che gestisce ed esegue tutte le promise contemporaneamente restitutendo un **array di promesse** che si risolve quando **tutte le promesse** nell'array sono risolte (o una di esse è rifiutata). Se una sola fallisce, finiscono tutte nel `.catch`

#### Come funziona:

- **Se tutte le promesse si risolvono con successo**, la promessa restituita da `Promise.all()` si risolve con un array di tutti i risultati.
- **Se una delle promesse viene rifiutata**, la promessa restituita da `Promise.all()` viene rifiutata immediatamente e il risultato sarà l'errore della prima promessa rifiutata.

#### Esempio:

`const promise1 = Promise.resolve(3);`
`const promise2 = Promise.resolve(42);`
`const promise3 = new Promise((resolve, reject) => setTimeout(resolve, 100, 'foo'));  
`Promise.all([promise1, promise2, promise3])`  
`.then(values => {     console.log(values)})` 
`.catch(error => {     console.error(error)});`

In questo caso, `Promise.all()` risolve tutte le promesse e restituisce i risultati in un array.

### 2. `Promise.race()`

`Promise.race()` è un altro metodo che prende un array di promesse, ma invece di aspettare che tutte si risolvano, si risolve **non appena la prima promessa** nell'array (la piu' veloce) si risolve o si rifiuta, le altre non verranno lette.

#### Come funziona:

- La promessa restituita da `Promise.race()` si risolve o si rifiuta con il valore o errore della **prima promessa** che si risolve o viene rifiutata.
- Le altre promesse nell'array vengono ignorate una volta che la prima si è risolta o rifiutata.

#### Esempio:

`const promise1 = new Promise((resolve, reject) => setTimeout(resolve, 500, 'first'));
`const promise2 = new Promise((resolve, reject) => setTimeout(resolve, 100, 'second'));` 
`Promise.race([promise1, promise2])` 
`.then(value => { console.log(value)})` 
`.catch(error => {  console.error(error)})

In questo caso, `Promise.race()` si risolve con `"second"` perché `promise2` è la prima a risolversi.

### In sintesi:

- **`Promise.all()`** è utile quando vuoi che tutte le promesse siano completate prima di proseguire, e gestisce tutti i risultati insieme.
- **`Promise.race()`** è utile quando vuoi ottenere il risultato della prima promessa che si completa (sia che si risolva o venga rifiutata).