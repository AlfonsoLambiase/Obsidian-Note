L'**optional chaining** (`?.`) è una funzionalità di JavaScript che ti permette di accedere in modo sicuro alle proprietà di un oggetto, anche quando alcune di esse potrebbero non esistere o essere `null`/`undefined`.
### Perché serve l'optional chaining?
Immagina di avere un oggetto complesso con molte proprietà, alcune delle quali potrebbero essere `null` o `undefined`. Se cerchi di accedere a una proprietà di un oggetto che è `null` o `undefined`, JavaScript genererà un errore.

es.
```
`let persona = { nome: "Giulia" };`
`console.log(persona.indirizzo?.citta); // undefined`
```


Con `?.`, se la proprietà `indirizzo` non esiste, invece di generare un errore, il risultato sarà `undefined`, ma il programma non si ferma.
Quindi, in breve: l'optional chaining (`?.`) ti permette di accedere alle proprietà senza preoccuparti che l'oggetto sia `null` o `undefined`. Se non c'è, ti dà semplicemente `undefined`, senza errori!

[^1]: 
