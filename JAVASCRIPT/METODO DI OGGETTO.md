Un **metodo** di un oggetto in JavaScript è una **funzione** che è **dentro** un oggetto. I metodi ti permettono di far fare delle azioni all'oggetto, come farlo **parlare**, **muoversi** o fare qualsiasi altra cosa che vuoi!

### Esempio:

Immagina un oggetto chiamato **"persona"**, e dentro c'è un metodo che fa salutare la persona.

```jsx
javascript
Copia
let persona = {
    nome: "Marco",
    saluta: function() {
        console.log("Ciao, sono " + this.nome);
    }
};

persona.saluta();  // Risultato: "Ciao, sono Marco"

```

- **`saluta`** è il **metodo**. È una funzione che dice "Ciao, sono Marco".
- **`this.nome`** è il nome della persona, che in questo caso è **Marco**.

# **METODI**

- **`Object.freeze()`**: Oggetto completamente immutabile.
- **`Object.seal()`**: Non puoi aggiungere o eliminare proprietà, ma puoi modificarle.
- **`Object.preventExtensions()`**: Non puoi aggiungere nuove proprietà, ma puoi modificare e eliminare quelle esistenti.
- **`Object.defineProperty()`**: Definisce o modifica una proprietà con regole specifiche (come se può essere modificata).
- **`Object.isFrozen()`**: Controlla se l'oggetto è congelato.
- **`Object.isSealed()`**: Controlla se l'oggetto è sigillato.
- **`Object.isExtensible()`**: Controlla se l'oggetto può essere esteso (aggiungere nuove proprietà).
- `Object.assign()` permette di copiare i valori di tutte le proprietà enumerabili da uno o più oggetti sorgente a un oggetto di destinazione. Ad esempio, può essere utilizzata per **unire oggetti** o per **copiare oggetti** , ma non fa una copia profonda delle proprietà annidate.
- `!!` viene utilizzato per **convertire un valore in un booleano**. È una tecnica compatta per forzare un valore ad essere **vero** (`true`) o **falso** (`false`).