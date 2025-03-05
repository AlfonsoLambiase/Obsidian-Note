La **CSS Grid** è un sistema di layout che permette di organizzare gli elementi di una pagina in una griglia bidimensionale, cioè su righe e colonne, in modo molto più flessibile rispetto a `flexbox`.

### Fondamenta di Grid:

In pratica, **CSS Grid** ti permette di suddividere uno spazio in righe e colonne e di posizionare gli elementi in quella griglia. È come un foglio di carta con linee orizzontali (righe) e verticali (colonne) dove puoi mettere i tuoi elementi.

### Ecco un esempio base di come funziona:

1. **Creare** un contenitore grid bisogna dichiarare che un contenitore sarà una griglia con la proprietà `display: grid`.
2. **Definire** le righe e le colonne specificando la larghezza e l'altezza delle stesse.
3. **Posizionare** un elemento in una posizione specifica della griglia, puoi usare le proprietà `grid-column` e `grid-row` per definirlo.

### Riassunto delle proprietà principali di Grid:

1. **`display: grid;`**: Abilita il layout a griglia.
2. **`grid-template-columns`** e **`grid-template-rows`**: Definiscono il numero e le dimensioni delle righe e colonne.
3. **`gap`**: Imposta lo spazio tra gli elementi della griglia.
4. **`grid-column` e `grid-row`**: Permettono di specificare la posizione e l'estensione degli elementi all'interno della griglia.