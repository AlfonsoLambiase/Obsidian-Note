Gli eventi **`on`** in JavaScript sono una serie di eventi che possono essere associati a vari tipi di interazioni dell'utente su un elemento del DOM (Document Object Model). Questi eventi sono definiti come proprietà di un elemento, e vengono spesso chiamati **event handler**. Ogni tipo di evento ha una proprietà `on` specifica (ad esempio `onclick`, `onmouseover`, `onkeydown`, ecc.).

### Sintassi degli eventi `on`

La sintassi di un evento `on` in JavaScript è generalmente questa:

`<element onevent="espressione">`

Dove `element` è l'elemento del DOM su cui stai ascoltando l'evento, e `event` è il tipo di evento che si vuole gestire.

**Esempio:**

`<button onclick="alert('Hai cliccato il bottone!')">Clicca qui</button>`

In questo esempio, quando l'utente clicca sul bottone, viene eseguito un alert con il messaggio "Hai cliccato il bottone!".

### Tipi di eventi con la sintassi `on`

Ecco una lista dei principali eventi che puoi gestire con la sintassi `on`:

1. **Eventi del mouse:**
    
    - `onclick`: attivato quando l'utente clicca su un elemento.
    - `ondblclick`: attivato quando l'utente fa doppio clic su un elemento.
    - `onmousedown`: attivato quando si preme un tasto del mouse sopra un elemento.
    - `onmouseup`: attivato quando si rilascia un tasto del mouse sopra un elemento.
    - `onmouseover`: attivato quando il mouse passa sopra un elemento.
    - `onmouseout`: attivato quando il mouse esce da un elemento.
    - `onmousemove`: attivato quando il mouse si sposta sopra un elemento.
    
    