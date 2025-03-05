Un **metodo costruttore** è come una **macchina** che ti aiuta a **creare oggetti** con le stesse proprietà.

Immagina che vuoi creare più **persone** con il **nome** e l'**età**. Anziché scrivere ogni volta il codice per ogni persona, usi un costruttore per **automaticamente** creare tante persone. La parola chiave **`this`** in JavaScript è un modo per fare riferimento all'**oggetto** che sta eseguendo una **funzione**. Puoi pensarlo come una sorta di "aiuto" per dire: "**questo oggetto**".

### Passaggi:

1. **Funzione costruttore**: È una **funzione** che dice come creare un oggetto (per esempio, una persona).
    
    ```jsx
    javascript
    Copia
    function Persona(nome, eta) {
        this.nome = nome;  // La persona avrà un "nome"
        this.eta = eta;    // La persona avrà un "eta"
    }
    
    ```
    
2. **Creare oggetti**: Per creare una persona, usi la parola **new**.
    
    ```jsx
    javascript
    Copia
    let persona1 = new Persona("Giulia", 25);  // Crea una persona di nome Giulia e età 25
    let persona2 = new Persona("Luca", 30);    // Crea una persona di nome Luca e età 30
    
    ```
    

Ora, **persona1** e **persona2** sono due oggetti separati con **nome** e **età** diverse, creati dalla stessa "macchina" (funzione costruttore).

### Aggiungere un metodo:

Puoi anche aggiungere **azioni** agli oggetti, come un "saluto". Ecco come:

```jsx
javascript
Copia
function Persona(nome, eta) {
    this.nome = nome;
    this.eta = eta;
    this.saluta = function() {
        console.log("Ciao, sono " + this.nome);
    };
}

let persona1 = new Persona("Giulia", 25);
persona1.saluta();  // Risultato: "Ciao, sono Giulia"

```

### Sintesi:

- **Costruttore** è una **funzione** che crea oggetti con le stesse proprietà.
- Con **new**, puoi creare tanti oggetti senza scrivere codice ripetitivo.