Un **oggetto** in JavaScript è come una **scatola** che contiene **cose** dentro. Ogni cosa dentro la scatola ha un nome, e puoi aprire la scatola per guardare o usare quelle cose. Per scrivere un **oggetto** in JavaScript, devi usare le **parentesi graffe** `{ }`. Dentro queste parentesi, puoi scrivere **chiave** (o **proprietà**) e **valori** separati da due punti `:`. Ogni coppia **proprietà: valore** è separata da una virgola `,`

Immagina un oggetto che rappresenta una **macchina**:

### Esempio di oggetto "macchina":

```jsx
javascript
Copia
let macchina = {
    colore: "rosso",
    modello: "Fiat",
    velocita: 120
};

```

- La scatola si chiama `macchina`.
- Dentro la scatola, ci sono tre **cose**:
    - **colore**: "rosso"
    - **modello**: "Fiat"
    - **velocita**: 120

### Come guardare le cose dentro l'oggetto:

Per vedere il **colore** della macchina, fai così:

```jsx
javascript
Copia
console.log(macchina.colore);  // Risultato: rosso

```

# OGGETTI ANNIDATI

Gli **oggetti nested** (o oggetti annidati) sono oggetti che contengono **altri oggetti** al loro interno. Immagina che dentro una scatola ci sia un'altra scatola, e dentro quest'ultima ci sono ancora delle cose! Sono utili quando hai bisogno di organizzare dati più complessi dentro un oggetto principale.

### Esempio di oggetto nested:

```jsx
javascript
Copia
let persona = {
    nome: "Giulia",
    eta: 28,
    indirizzo: {
        via: "Via Roma 123",
        città: "Milano",
        cap: 20100
    }
};

```

### Come accedere a un oggetto nested:

Per ottenere una proprietà dentro un oggetto annidato, usi il nome dell'oggetto principale seguito dal nome della chiave (e, se necessario, il nome dell'oggetto annidato):