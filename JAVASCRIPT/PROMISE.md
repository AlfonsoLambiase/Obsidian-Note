In JavaScript, un **Promise** è un oggetto che rappresenta il risultato di un'operazione asincrona che potrebbe non essere ancora completata, ma lo sarà in futuro.

Immagina di chiedere a un amico di portarti una pizza. Quando gli fai la richiesta, non puoi avere la pizza subito. Il tuo amico promette che te la porterà, ma non sa esattamente quando. Quando la pizza arriva, lui ti dice "Ecco la pizza, la promessa è stata mantenuta!" oppure, se non riesce a portarla, ti dice "Mi dispiace, non posso portartela" (e in quel caso la promessa è stata "rifiutata").

### Struttura di un Promise:

Un **Promise** ha tre possibili stati:

1. **Pending (In attesa)**: La promessa non è ancora stata né risolta né rifiutata (è come se tu stai aspettando la pizza).
2. **Fulfilled (Completata)**: L'operazione è stata completata con successo (la pizza è arrivata!).
3. **Rejected (Rifiutata)**: Si è verificato un errore o un problema nell'operazione (la pizza non è arrivata).

### Sintassi base di un Promise:
```
let miaPromessa = new Promise(resolve, reject) {      
let successo = true; 
if(successo){resolve("Operazione completata con successo!")} 
else {reject("Si è verificato un errore.")}}); 

miaPromessa()
.then(result){console.log(result)})
.catch(function(error){console.log(error)});
```

### Cosa succede:

- **`resolve()`**: Se tutto va bene (ad esempio la pizza arriva), il Promise si risolve e il risultato viene passato.
- **`reject()`**: Se c'è un errore (ad esempio la pizza non arriva), il Promise viene rifiutato e l'errore viene passato.

### `.then()` e `.catch()`:

- **`.then()`**: Si usa per gestire il risultato di una promessa completata con successo.
- **`.catch()`**: Si usa per gestire eventuali errori, cioè quando la promessa è stata rifiutata.


## **CONCATENARE PROMISE**

Se desideri concatenare promesse senza usare `async` e `await`, puoi farlo esclusivamente utilizzando il metodo `.then()`. Ecco un esempio di come concatenare due promesse senza `async`/`await`, restituendo il risultato tramite `return`:

### Esempio con `.then()`:

`function firstPromise(){ 
return new Promise((resolve, reject) => { 
setTimeout(() => resolve('First Promise resolved'), 1000)})}  
function secondPromise() {   return new Promise((resolve, reject) => {     setTimeout(() => resolve('Second Promise resolved'), 1000);   }); }  firstPromise()   .then(result => {     console.log(result); // Stampa: 'First Promise resolved'     return secondPromise(); // Restituisce la seconda Promise   })   .then(result => {     console.log(result); // Stampa: 'Second Promise resolved'     return 'Final result'; // Puoi anche restituire un valore finale   })   .then(finalResult => {     console.log(finalResult); // Stampa: 'Final result'   })   .catch(error => {     console.error(error); // Gestisce eventuali errori   });`

### Spiegazione:

- **`firstPromise()`**: Restituisce una promessa che si risolve dopo un secondo.
- **`.then()`**: Usa il metodo `.then()` per concatenare l'output di una promessa con la successiva. Ogni `.then()` restituisce una nuova promessa.
- **`return secondPromise()`**: All'interno di un `.then()`, puoi restituire una nuova promessa che si concatenarà al prossimo `.then()`.
- Puoi anche restituire un valore qualsiasi (ad esempio `'Final result'`) che verrà passato al prossimo `.then()`.

In questo modo, concatenando promesse tramite `.then()`, puoi ottenere un flusso di esecuzione simile a quello delle `Promise` senza dover usare `async/await`.