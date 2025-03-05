Una callback in JavaScript è semplicemente una funzione che "passi" a un'altra funzione per farla eseguire in seguito.

Immagina che tu faccia una richiesta, e mentre aspetti che arrivi la risposta, decidi di fare altro. Quando arriva la risposta, "chiami" un'altra funzione per gestirla.

Il **callback** è utile quando hai operazioni che richiedono tempo (come richieste di rete) e non vuoi bloccare il resto del programma mentre aspetti che finiscano.

ES.

```jsx
function faiQualcosa(callback) {
console.log("Faccio qualcosa...");
callback();  // Esegui il callback dopo
}
```

```jsx
function termina() {
console.log("Ho finito!");
}
```

```jsx
faiQualcosa(termina);
```

### Cosa succede:

1. **`faiQualcosa`** stampa "Faccio qualcosa..."
2. Poi esegue la funzione **`termina`** che stampa "Ho finito!".

Risultato:

```

Faccio qualcosa...
Ho finito!

```

La funzione **`termina`** è il callback che viene eseguito **dopo** la funzione principale (`faiQualcosa`).