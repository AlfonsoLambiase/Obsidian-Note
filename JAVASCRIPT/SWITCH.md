
Il `switch` in JavaScript è un'istruzione che ti permette di fare delle verifiche su una variabile, confrontandola con diversi valori possibili. È come una serie di `if-else` più compatta e leggibile quando hai molte condizioni da verificare.

### Sintassi del `switch`:

```jsx

switch (variabile) {
  case valore1:
    // codice da eseguire se variabile === valore1
    break;
  case valore2:
    // codice da eseguire se variabile === valore2
    break;
  // aggiungi altri casi se necessario
  default:
    // codice da eseguire se nessun caso corrisponde
}

```

Il `switch` è utile quando hai più opzioni da verificare per una stessa variabile e rende il codice più ordinato rispetto a molteplici `if-else`. Se non c'è corrispondenza, il `default` viene eseguito.