`addEventListener` è un metodo di JavaScript che permette di "ascoltare" gli eventi su un elemento del DOM (Document Object Model). Quando un evento accade, come un clic su un bottone, il movimento del mouse o la pressione di un tasto, il metodo esegue una funzione (chiamata anche "callback") che hai definito.

### Sintassi di `addEventListener`

La sintassi di `addEventListener` è la seguente:

`element.addEventListener(event, callback, useCapture);`

- **`element`**: è l'elemento del DOM su cui stai ascoltando l'evento (ad esempio un bottone, una finestra, un documento, ecc.).
- **`event`**: è il tipo di evento che stai ascoltando, come `"click"`, `"keydown"`, `"mouseenter"`, ecc.
- **`callback`**: è la funzione che verrà eseguita quando l'evento si verifica.
- **`useCapture`**: è un parametro opzionale che indica se l'evento deve essere gestito durante la fase di cattura o di bubbling. Normalmente puoi ometterlo (è `false` di default) e lasciare che l'evento venga gestito durante il bubbling.

### Esempio di uso:

`const bottone = document.querySelector("button");  bottone.addEventListener("click", function() {   
`alert("Hai cliccato il bottone!"); });`

In questo esempio, quando clicchi sul bottone, il browser esegue la funzione di callback che mostra un alert.

### Eventi che può gestire `addEventListener`

`addEventListener` può gestire **qualsiasi tipo di evento** che il browser supporta. Ecco una lista dei tipi di eventi più comuni:

1. **Eventi del mouse**:
    
    - `"click"`: quando un utente clicca su un elemento.
    - `"dblclick"`: quando un utente fa doppio clic.
    - `"mousedown"`: quando si preme un tasto del mouse sopra un elemento.
    - `"mouseup"`: quando si rilascia un tasto del mouse sopra un elemento.
    - `"mouseover"`: quando il puntatore del mouse entra in un elemento.
    - `"mouseout"`: quando il puntatore del mouse esce da un elemento.
    - `"mousemove"`: quando il mouse si sposta sopra un elemento.
2. **Eventi della tastiera**:
    
    - `"keydown"`: quando un tasto della tastiera viene premuto.
    - `"keypress"`: quando un tasto viene premuto e mantenuto (meno usato, in disuso).
    - `"keyup"`: quando un tasto della tastiera viene rilasciato.
3. **Eventi di focus e input**:
    
    - `"focus"`: quando un elemento (come un campo di input) riceve il focus.
    - `"blur"`: quando un elemento perde il focus.
    - `"input"`: quando il valore di un elemento di input cambia.
    - `"change"`: quando l'utente cambia il valore di un campo (spesso usato su `<input>` o `<select>`).
4. **Eventi relativi al documento o finestra**:
    
    - `"load"`: quando una risorsa (come un'immagine, una pagina o un iframe) è completamente caricata.
    - `"resize"`: quando la finestra del browser viene ridimensionata.
    - `"scroll"`: quando l'utente scorre il contenuto di una pagina o di un elemento.
    - `"unload"`: quando la pagina sta per essere scaricata.
5. **Eventi di touch (per dispositivi mobili)**:
    
    - `"touchstart"`: quando l'utente inizia a toccare uno schermo.
    - `"touchend"`: quando l'utente termina il tocco su uno schermo.
    - `"touchmove"`: quando il dito si muove sopra lo schermo.
6. **Eventi di animazione e transizione**:
    
    - `"animationstart"`: quando un'animazione CSS inizia.
    - `"animationend"`: quando un'animazione CSS finisce.
    - `"transitionend"`: quando una transizione CSS finisce.