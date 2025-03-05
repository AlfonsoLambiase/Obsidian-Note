La funzione `nth-child` in CSS è una **pseudo-classe** che ti permette di selezionare **elementi in base alla loro posizione** all'interno di un contenitore, come una lista o un div. In pratica, puoi applicare uno stile a un elemento che si trova in una posizione specifica tra i suoi fratelli (parenti diretti).

### Sintassi di base:

```css
css
Copia
selector:nth-child(n)

```

- **`selector`** è l'elemento che vuoi selezionare (come `li`, `p`, `div`, ecc.).
- **`n`** è un valore che può essere un numero, una formula o un altro tipo di espressione per selezionare un elemento in una posizione specifica.
- `nth-child(1)` seleziona il primo elemento.
- `nth-child(2n)` seleziona tutti gli **elementi pari**.
- `nth-child(3n)` seleziona tutti gli **elementi ogni terzo**.
- `nth-child(odd)` seleziona gli **elementi dispari**.
- `nth-child(5)` seleziona il **quinto elemento**.

La funzione `nth-child` è potente e ti permette di selezionare facilmente gruppi di elementi in una struttura HTML senza dover aggiungere classi o ID.