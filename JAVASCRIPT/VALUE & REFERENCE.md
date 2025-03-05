### **Valore**

Quando una variabile ha un **valore**, significa che contiene i dati direttamente. Se crei una nuova variabile e le assegni lo stesso valore, è come fare una copia. Cambiare una delle due variabili non cambia l'altra.

- **Esempio (valore):**
    
    ```python
    python
    Copia
    a = 5
    b = a  # b copia il valore di a
    b = 10  # Cambiando b non cambia a
    
    print(a)  # 5
    print(b)  # 10
    
    ```
    

### **Riferimento**

Quando una variabile ha un **riferimento**, significa che contiene un "link" che punta ai dati, non i dati stessi. Se cambi i dati attraverso una variabile, anche l'altra variabile che punta allo stesso dato viene cambiata.

- **Esempio (riferimento):**
    
    ```python
    python
    Copia
    lista1 = [1, 2, 3]
    lista2 = lista1  # lista2 punta alla stessa lista di lista1
    lista2[0] = 100  # Cambiando lista2 cambia anche lista1
    
    print(lista1)  # [100, 2, 3]
    print(lista2)  # [100, 2, 3]
    
    ```
    

### In breve:

- **Valore**: copia dei dati. Cambiare una variabile non cambia l'altra.
- **Riferimento**: entrambe le variabili puntano agli stessi dati. Cambiare uno cambia anche l'altro.

# COPIA PER VALORE/RIFERIMENTO

In JavaScript, la **copia per valore** e la **copia per riferimento** sono due concetti chiave che descrivono come i dati vengono copiati o condivisi tra variabili. La differenza principale dipende dal tipo di dato che stai cercando di copiare: **tipi primitivi** (come numeri, stringhe, booleani) o **oggetti** (compresi array e funzioni). Vediamo la differenza in dettaglio:

### 1. **Copia per valore** (per tipi primitivi)

Quando copi un **tipo primitivo** (come un numero, una stringa, un booleano), la variabile di destinazione ottiene una **copia indipendente** del valore, non un riferimento al valore originale. Modificare una delle variabili **non influenzerà l'altra**.

Esempio con un **numero** (tipo primitivo):

```jsx
javascript
Copia
let a = 10;
let b = a; // copia per valore
b = 20;

console.log(a); // 10
console.log(b); // 20

```

In questo caso:

- `a` e `b` sono indipendenti.
- Modificando `b`, `a` rimane invariato perché `b` ha una copia del valore di `a`, non un riferimento.

### 2. **Copia per riferimento** (per oggetti e array)

Quando copi un **oggetto** (inclusi array, funzioni, oggetti), stai copiando un **riferimento** all'oggetto originale, non una copia del suo valore. Quindi, entrambe le variabili **punteranno allo stesso oggetto**. Modificare l'oggetto tramite una variabile influenzerà l'altro, perché entrambi i riferimenti puntano allo stesso oggetto in memoria.

Esempio con un **array** (oggetto complesso):

```jsx
javascript
Copia
let arr1 = [1, 2, 3];
let arr2 = arr1; // copia per riferimento
arr2[0] = 10;

console.log(arr1); // [10, 2, 3]
console.log(arr2); // [10, 2, 3]

```

In questo caso:

- `arr1` e `arr2` sono **riferimenti allo stesso array**.
- Modificando `arr2`, anche `arr1` viene modificato, perché entrambe le variabili puntano allo stesso oggetto in memoria.

### Copia superficiale vs. copia profonda

Quando copiamo un oggetto (o array) con il **metodo di copia per riferimento**, otteniamo una **copia superficiale**. Questo significa che se l'oggetto contiene altri oggetti o array, vengono copiati solo i riferimenti agli oggetti interni, non una copia indipendente di essi.

Esempio di **copia superficiale**:

```jsx
javascript
Copia
let originalArray = [1, [2, 3], 4];
let cloneArray = [...originalArray]; // copia superficiale

cloneArray[1][0] = 99;

console.log(originalArray); // [1, [99, 3], 4]
console.log(cloneArray);    // [1, [99, 3], 4]

```

Qui:

- L'array esterno è stato copiato, ma l'array interno (l'elemento `[2, 3]`) è ancora lo stesso oggetto per entrambe le variabili, quindi modificando `cloneArray[1]`, anche `originalArray[1]` viene modificato.

Se desideri una **copia profonda**, che copia anche gli oggetti interni in modo indipendente, devi usare un metodo diverso, come `JSON.parse(JSON.stringify(array))` oppure librerie come `lodash` per una copia profonda.

### Riassunto

- **Copia per valore**: Quando copi un **tipo primitivo**, crei una copia indipendente del valore. Modificare una variabile non influisce sull'altra.
- **Copia per riferimento**: Quando copi un **oggetto** o un **array**, crei un nuovo riferimento allo stesso oggetto in memoria. Modificare uno influirà sull'altro.