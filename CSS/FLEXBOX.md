Flexbox è un potente modello di layout in CSS che ti permette di creare layout flessibili e dinamici con poche righe di codice. Ecco le regole principali e gli elementi coinvolti:

### **Container Flex (Flex Container)**

Per utilizzare Flexbox, devi dichiarare un contenitore come **flex**. Questo viene fatto con la proprietà `display: flex` o `display: inline-flex`.

### **Proprietà del Container Flex**

- **`flex-direction`**: Definisce la direzione principale lungo la quale gli elementi vengono disposti.
    
    - `column-reverse`: Gli elementi sono disposti verticalmente, ma in ordine inverso.
    - `row-reverse`: Gli elementi sono disposti orizzontalmente, ma in ordine inverso.
    - `column`: Gli elementi sono disposti verticalmente.
    - `row` (default): Gli elementi sono disposti orizzontalmente.
- **`flex-wrap`**: Controlla se gli elementi devono andare a capo quando non c'è abbastanza spazio.
    
    - `nowrap` (default): Gli elementi non vanno mai a capo.
    - `wrap`: Gli elementi vanno a capo quando necessario.
    - `wrap-reverse`: Gli elementi vanno a capo in ordine inverso.
- **`justify-content`**: Allinea gli elementi lungo l'asse principale (orizzontale o verticale a seconda di `flex-direction`).
    
    - `flex-start`: Allinea gli elementi all'inizio dell'asse.
    - `flex-end`: Allinea gli elementi alla fine dell'asse.
    - `center`: Centra gli elementi lungo l'asse.
    - `space-between`: Distribuisce lo spazio tra gli elementi.
    - `space-around`: Distribuisce lo spazio attorno agli elementi.
- **`align-items`**: Allinea gli elementi lungo l'asse trasversale (perpendicolare all'asse principale).
    
    `baseline`: Allinea gli elementi lungo la linea di base.
    
    `center`: Centra gli elementi lungo l'asse trasversale.
    
    `flex-end`: Allinea gli elementi alla fine dell'asse trasversale.
    
    `flex-start`: Allinea gli elementi all'inizio dell'asse trasversale.
    
    `stretch` (default): Gli elementi si espandono per occupare tutto lo spazio disponibile.
    
- **`align-content`**: Allinea le righe del contenitore (se gli elementi vanno a capo).
    
    - `space-around`: Distribuisce lo spazio attorno alle righe.
    - `center`: Centra le righe lungo l'asse trasversale.
    - `stretch` (default): Espande le righe per occupare tutto lo spazio disponibile.
    - `space-between`: Distribuisce lo spazio tra le righe.
    - `flex-end`: Allinea le righe alla fine dell'asse trasversale.
    - `flex-start`: Allinea le righe all'inizio dell'asse trasversale.

### **Proprietà degli Items Flex (Flex Items)**

Ogni elemento dentro un contenitore flex (un **flex item**) ha a disposizione alcune proprietà che permettono di definirne il comportamento.

- **`flex-grow`**: Determina la capacità di un elemento di crescere rispetto agli altri quando c'è spazio extra. Il valore predefinito è `0`, il che significa che l'elemento non crescerà mai.Un valore maggiore di `0` farà crescere l'elemento.
- **`flex-shrink`**: Determina la capacità di un elemento di ridursi quando lo spazio è insufficiente. Il valore predefinito è `1`, il che significa che l'elemento si ridurrà.
    - Se impostato a `0`, l'elemento non si ridurrà mai.
- **`flex-basis`**: Imposta la dimensione iniziale di un elemento prima che lo spazio extra venga distribuito. Può essere un valore in px, %, auto, ecc.
- **`flex`**: È una scorciatoia per combinare `flex-grow`, `flex-shrink` e `flex-basis` in una sola proprietà. Il formato è: `flex: <flex-grow> <flex-shrink> <flex-basis>`.
- **`align-self`**: Permette di allineare un singolo elemento lungo l'asse trasversale, sovrascrivendo la proprietà `align-items` del contenitore. Può assumere i valori di `align-items`, ma per un singolo elemento.
    - `auto`: Il comportamento di allineamento predefinito.
    - `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.