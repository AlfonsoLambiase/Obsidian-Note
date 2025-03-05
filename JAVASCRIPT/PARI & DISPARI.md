In JavaScript, l'operatore modulo è rappresentato dal simbolo %. Questo operatore restituisce il resto della divisione tra due numeri.

Per identificare se un numero è pari o dispari in JavaScript, puoi usare l'operatore modulo (%). Se il resto della divisione di un numero per 2 è 0, il numero è pari, altrimenti è dispari.

#### Esempio di codice:

`function checkPariDispari(numero) { if (numero % 2 === 0) { console.log(numero + " è pari"); } else { console.log(numero + " è dispari"); } } checkPariDispari(4); // Stampa: 4 è pari checkPariDispari(7); // Stampa: 7 è dispari`

#### Come funziona:

- numero % 2 === 0: Se il resto della divisione di numero per 2 è 0, allora il numero è pari.
- numero % 2 != 0 ,il numero è dispari.