# **LOCAL STORAGE**

Il **localStorage** in JavaScript è una tecnologia che permette di memorizzare dati nel browser in modo persistente, anche dopo che la pagina viene ricaricata o il browser viene chiuso. I dati salvati nel **localStorage** non scadono mai, a meno che non vengano esplicitamente rimossi.

### Come funziona?

1. **Memorizzare un dato**: Puoi usare il metodo `setItem()` per salvare un valore nel localStorage.

    `localStorage.setItem('chiave', 'valore');`
    `localStorage.setItem('nome', 'Mario');`
    
2. **Recuperare un dato**: Puoi usare `getItem()` per leggere un valore salvato precedentemente.

    `let nome = localStorage.getItem('nome');
    `console.log(nome);` 
    
3. **Rimuovere un dato**: Puoi usare `removeItem()` per eliminare una chiave dal localStorage.

    `localStorage.removeItem('nome');`
    
4. **Cancellare tutto**: Se vuoi cancellare tutti i dati nel localStorage, puoi usare `clear()`.

    `localStorage.clear();`
    

### Caratteristiche principali:

- I dati nel **localStorage** sono memorizzati come coppie **chiave-valore** (key-value).
- I dati sono **persistenti**: rimangono anche dopo che il browser è chiuso.
- Il **localStorage** è limitato alla stessa origine (dominio). Dati salvati in un sito non sono accessibili da un altro sito.

Il **localStorage** è molto utile per memorizzare preferenze o dati che devono essere accessibili anche dopo una ricarica della pagina o una chiusura del browser, ma è importante non salvare dati sensibili, perché non è crittografato.

# **SESSION STORAGE**

Il **sessionStorage** in JavaScript è simile al **localStorage**, ma ha una differenza importante: i dati memorizzati nel **sessionStorage** **scompaiono** non appena la sessione del browser termina, ovvero quando la finestra o la scheda del browser viene chiusa.
### Caratteristiche principali:

- I dati nel **sessionStorage** sono anch'essi memorizzati come coppie **chiave-valore**.
- La differenza principale rispetto al **localStorage** è che i dati nel **sessionStorage** **vengono cancellati** quando la finestra o la scheda del browser viene chiusa.
- Il **sessionStorage** è anche limitato alla stessa origine (dominio), come il **localStorage**.


### Differenze con **localStorage**:

- **localStorage** è persistente (i dati rimangono anche se il browser viene chiuso).
- **sessionStorage** dura solo per la durata della sessione (i dati vengono cancellati quando la finestra o la scheda del browser viene chiusa).
    
### Quando usare **sessionStorage**?

- Se hai bisogno di memorizzare dati temporanei durante una sessione di navigazione (ad esempio, informazioni temporanee su un processo di pagamento o un modulo che l'utente sta compilando).

