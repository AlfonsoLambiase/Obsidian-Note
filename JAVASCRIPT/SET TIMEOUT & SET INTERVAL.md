# SET TIMEOUT

`setTimeout` in JavaScript è una funzione che permette di eseguire un'azione dopo un certo periodo di tempo. È come dire: "Aspetta un po', poi fai questa cosa".

### Sintassi:

```jsx
javascript
Copia
setTimeout(funzione, tempo);

```

- **`funzione`** è la funzione che vuoi eseguire dopo un certo tempo.
- **`tempo`** è il numero di millisecondi che JavaScript deve aspettare prima di eseguire la funzione (1000 millisecondi = 1 secondo).

### Esempio semplice:

```jsx
javascript
Copia
setTimeout(function() {
    console.log("Ciao dopo 2 secondi!");
}, 2000);  // 2000 millisecondi = 2 secondi

```

### Cosa succede:

1. **`setTimeout`** aspetta 2 secondi (2000 millisecondi).
2. Dopo 2 secondi, esegue la funzione che stampa "Ciao dopo 2 secondi!"

# SET INTERVAL

**`setInterval`** in JavaScript è una funzione che esegue una determinata azione ripetutamente, a intervalli regolari di tempo. È come dire: "Fai questa cosa ogni X millisecondi".

### Sintassi:

```jsx

setInterval(funzione, intervallo);

```

- **`funzione`** è la funzione che vuoi eseguire.
- **`intervallo`** è il tempo (in millisecondi) che deve passare tra ogni esecuzione della funzione.

### Esempio semplice:

```jsx

setInterval(() => {
    console.log("Ogni secondo!");
}, 1000);  // 1000 millisecondi = 1 secondo

```

### Cosa succede:

1. La funzione passata a **`setInterval`** stampa "Ogni secondo!".
2. Poi la funzione verrà eseguita ogni **1 secondo** (1000 millisecondi)

### Fermare un intervallo:

Per fermare un intervallo, puoi usare **`clearInterval()`**, passando l'ID che `setInterval` restituisce.

Esempio:

```jsx
javascript
Copia
let intervalID = setInterval(() => {
    console.log("Ogni secondo!");
}, 1000);

// Dopo 5 secondi, fermiamo l'intervallo
setTimeout(() => {
    clearInterval(intervalID);
    console.log("Intervallo fermato!");
}, 5000);

```

### Cosa succede:

1. Il messaggio "Ogni secondo!" verrà stampato ogni secondo.
2. Dopo 5 secondi, **`clearInterval`** ferma l'intervallo e stampa "Intervallo fermato!"