Nel **DOM** (Document Object Model), ci sono vari **metodi** che ci permettono di interagire con gli elementi HTML di una pagina web, come selezionarli, modificarli, aggiungere nuovi elementi, ecc. Ecco una panoramica dei principali metodi del DOM:

### 1. **`getElementById()`**

- **Cosa fa:** Restituisce l'elemento che ha un `id` specificato.
- **Esempio:**

    `const element = document.getElementById('miaId');`
    

### 2. **`getElementsByClassName()`**

- **Cosa fa:** Restituisce una raccolta di tutti gli elementi che hanno una classe specificata.
- **Esempio:**
   
    `const elements = document.getElementsByClassName('miaClasse');`
    

### 3. **`getElementsByTagName()`**

- **Cosa fa:** Restituisce una raccolta di tutti gli elementi con un determinato nome di tag (ad esempio, tutti i `<div>`, `<p>`, ecc.).
- **Esempio:**
   
    `const divs = document.getElementsByTagName('div');`
    

### 4. **`querySelector()`**

- **Cosa fa:** Restituisce il **primo** elemento che corrisponde al selettore CSS specificato.
- **Esempio:**

    `const element = document.querySelector('.miaClasse');`
    

### 5. **`querySelectorAll()`**

- **Cosa fa:** Restituisce tutti gli elementi che corrispondono al selettore CSS specificato (è simile a `querySelector()`, ma restituisce una NodeList di tutti gli elementi corrispondenti).
- **Esempio:**

    `const elements = document.querySelectorAll('.miaClasse');`
    

### 6. **`createElement()`**

- **Cosa fa:** Crea un nuovo elemento HTML che non è ancora inserito nel DOM.
- **Esempio:**

    `const newElement = document.createElement('div');`
    

### 7. **`appendChild()`**

- **Cosa fa:** Aggiunge un nodo come ultimo figlio di un elemento.
- **Esempio:**

    `const parent = document.getElementById('container'); parent.appendChild(newElement);`
    

### 8. **`removeChild()`**

- **Cosa fa:** Rimuove un nodo figlio da un elemento.
- **Esempio:**

    `const parent = document.getElementById('container'); const child = document.getElementById('elementoDaRimuovere'); parent.removeChild(child);`
    

### 9. **`setAttribute()`**

- **Cosa fa:** Imposta un attributo su un elemento.
- **Esempio:**

    `const element = document.getElementById('miaImmagine'); element.setAttribute('src', 'nuovaImmagine.jpg');`
    

### 10. **`getAttribute()`**

- **Cosa fa:** Restituisce il valore di un attributo di un elemento.
- **Esempio:**
 
    `const element = document.getElementById('miaImmagine'); const src = element.getAttribute('src');`
    

### 11. **`removeAttribute()`**

- **Cosa fa:** Rimuove un attributo da un elemento.
- **Esempio:**

    `const element = document.getElementById('miaImmagine'); element.removeAttribute('src');`
    

### 12. **`innerHTML`**

- **Cosa fa:** Permette di ottenere o impostare il contenuto HTML di un elemento.
- **Esempio:**

    `const element = document.getElementById('content'); element.innerHTML = '<p>Nuovo contenuto HTML</p>';`
    

### 13. **`textContent`**

- **Cosa fa:** Permette di ottenere o impostare il contenuto di testo di un elemento (senza includere HTML).
- **Esempio:**

    `const element = document.getElementById('content'); element.textContent = 'Nuovo contenuto di testo';`
    

### 14. **`addEventListener()`**

- **Cosa fa:** Aggiunge un ascoltatore di eventi a un elemento, che esegue una funzione quando si verifica un evento (come un clic, un mouseover, ecc.).
- **Esempio:**

    `const button = document.getElementById('myButton'); button.addEventListener('click', function() {   alert('Hai cliccato il bottone!'); });`
    

### 15. **`removeEventListener()`**

- **Cosa fa:** Rimuove un ascoltatore di eventi precedentemente aggiunto a un elemento.
- **Esempio:**

    `const button = document.getElementById('myButton'); button.removeEventListener('click', myFunction);`
    

### 16. **`classList.add()`**

- **Cosa fa:** Aggiunge una classe a un elemento.
- **Esempio:**
  
    `const element = document.getElementById('myElement'); element.classList.add('newClass');`
    

### 17. **`classList.remove()`**

- **Cosa fa:** Rimuove una classe da un elemento.
- **Esempio:**

    `const element = document.getElementById('myElement'); element.classList.remove('oldClass');`
    

### 18. **`classList.toggle()`**

- **Cosa fa:** Aggiunge una classe se non esiste, la rimuove se esiste già.
- **Esempio:**

    `const element = document.getElementById('myElement'); element.classList.toggle('active');`

---
# **PROPRIETA' DI NAVIGAZIONE DEL                                      DOM**

Nel contesto del **DOM**, questi metodi sono utilizzati per navigare attraverso la struttura HTML di una pagina web. Vediamo cosa fanno in modo semplice:

### 1. **parentElement**

- **Cosa fa:** Restituisce l'elemento genitore dell'elemento corrente.
- **Esempio:** Se hai un `<li>` all'interno di un `<ul>`, chiamando `parentElement` sull'`<li>`, otterrai l'elemento `<ul>`.

`<ul>   <li>Item 1</li>   <li>Item 2</li> </ul>`

Se selezioni il secondo `<li>` (Item 2) e fai `parentElement`, otterrai il `<ul>` che lo contiene.

### 2. **nextElementSibling**

- **Cosa fa:** Restituisce l'elemento subito successivo nell'ordine dei fratelli (siblings) dell'elemento corrente. Solo gli elementi "di tipo" (come `<div>`, `<p>`, ecc.) vengono considerati, non i nodi di testo o i commenti.
- **Esempio:** Se hai più `<p>` nella stessa sezione e selezioni uno di essi, `nextElementSibling` ti darà il prossimo `<p>`.

`<div>   <p>Primo paragrafo</p>   <p>Secondo paragrafo</p> </div>`

Se selezioni il primo `<p>`, con `nextElementSibling` otterrai il secondo `<p>`.

### 3. **previousElementSibling**

- **Cosa fa:** Restituisce l'elemento precedente al corrente nella sequenza di fratelli.
- **Esempio:** Simile a `nextElementSibling`, ma in direzione opposta.

`<div>   <p>Primo paragrafo</p>   <p>Secondo paragrafo</p> </div>`

Se selezioni il secondo `<p>`, chiamando `previousElementSibling`, otterrai il primo `<p>`.

### 4. **firstElementChild**

- **Cosa fa:** Restituisce il primo figlio dell'elemento corrente.
- **Esempio:** Se hai una lista di elementi, otterrai il primo elemento della lista.

`<ul>   <li>Item 1</li>   <li>Item 2</li> </ul>`

Se selezioni il `<ul>`, con `firstElementChild` otterrai il primo `<li>` (Item 1).

### 5. **lastElementChild**

- **Cosa fa:** Restituisce l'ultimo figlio dell'elemento corrente.
- **Esempio:** Come `firstElementChild`, ma con l'ultimo figlio.

`<ul>   <li>Item 1</li>   <li>Item 2</li> </ul>`

Se selezioni il `<ul>`, con `lastElementChild` otterrai l'ultimo `<li>` (Item 2).

---
# **METODI CHE INTERAGISCONO CON                            IL TESTO HTML** 

Nel DOM,  ci sono altri metodi e proprietà che puoi utilizzare per accedere e manipolare il contenuto di un elemento HTML. Ecco una panoramica delle opzioni disponibili:

### 1. **`innerText`**

- **Cosa fa:** Restituisce o imposta il contenuto di testo "visibile" (ignora i tag HTML) di un elemento. Quando imposti il valore, viene rimosso tutto il contenuto HTML ed è sostituito solo con il testo.
- **Esempio:**

    `const element = document.getElementById('myElement'); element.innerText = 'Nuovo testo!';`
    

### 2. **`textContent`**

- **Cosa fa:** Restituisce o imposta il contenuto di testo di un elemento, senza interpretare i tag HTML (come fa `innerText`). `textContent` è più veloce di `innerText`, perché non tiene conto della formattazione o della visibilità del testo.
- **Esempio:**

    `const element = document.getElementById('myElement'); element.textContent = 'Nuovo testo!';`
    

### 3. **`innerHTML`**

- **Cosa fa:** Restituisce o imposta il contenuto HTML di un elemento. A differenza di `innerText` e `textContent`, `innerHTML` consente di leggere o scrivere HTML valido, comprese le etichette HTML, all'interno di un elemento.
- **Esempio:**

    `const element = document.getElementById('myElement'); element.innerHTML = '<p>Questo è un paragrafo dentro un elemento!</p>';`
    

### 4. **`outerHTML`**

- **Cosa fa:** Restituisce o imposta l'intero markup HTML di un elemento, inclusa l'elemento stesso. È simile a `innerHTML`, ma include anche l'elemento che lo contiene.
- **Esempio:**

    `const element = document.getElementById('myElement'); const markup = element.outerHTML; // Restituisce l'HTML dell'elemento, inclusa la tag <div> o altro console.log(markup);`
    

### 5. **`value`**

- **Cosa fa:** Restituisce o imposta il valore di un campo di input, come una casella di testo, un'area di testo o una selezione di opzioni (ad esempio, in un `<select>`). Non è utilizzato per ottenere o impostare contenuti HTML o di testo, ma per valori di form.
- **Esempio:**

    `const input = document.getElementById('myInput'); const value = input.value;  // Ottieni il valore input.value = 'Nuovo valore'; // Imposta un nuovo valore`
    

### 6. **`setAttribute()` e `getAttribute()`**

- **Cosa fanno:** Questi metodi permettono di leggere o modificare gli attributi di un elemento, come `id`, `class`, `href`, ecc. Non sono direttamente legati al contenuto del testo, ma sono utili per manipolare gli attributi.
    
- **Esempio di `getAttribute()`:**

    `const element = document.getElementById('myElement'); const hrefValue = element.getAttribute('href'); // Ottieni il valore dell'attributo href`
    
- **Esempio di `setAttribute()`:**

    `const element = document.getElementById('myElement'); element.setAttribute('data-custom', '123'); // Imposta un nuovo attributo personalizzato`
    

### 7. **`textRange`**

- **Cosa fa:** Una proprietà più avanzata per la selezione di testo all'interno di un elemento. Può essere usata per selezionare e manipolare il testo visibile in modo più specifico.

### 8. **`insertAdjacentHTML()`**

- **Cosa fa:** Permette di inserire del contenuto HTML in un punto specifico rispetto a un elemento, senza modificare il suo contenuto attuale.
- **Esempio:**

    `const element = document.getElementById('myElement'); element.insertAdjacentHTML('beforeend', '<p>Un nuovo paragrafo!</p>');`
    

### 9. **`insertAdjacentText()`**

- **Cosa fa:** È simile a `insertAdjacentHTML()`, ma consente solo l'inserimento di testo (non HTML).
- **Esempio:**

    `const element = document.getElementById('myElement'); element.insertAdjacentText('beforeend', 'Testo aggiunto!');`


