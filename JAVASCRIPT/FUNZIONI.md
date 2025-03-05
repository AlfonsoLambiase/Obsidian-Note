Una funzione è una porzione di codice che viene progettata per eseguire un compito specifico, normalmente ad una funzione si da un nome, e le funzioni possono (però non devono per forza) sia ricevere dei paramenti in ingresso sia restituire un valore in uscita.

**COME SI FA A DEFINIRE UNA FUNZIONE IN JAVASCRIPT?**

Innanzitutto si utilizza la parole chiave FUNCTION, questa parola chiave dice a Java script che stiamo iniziando a definire una funzione, ovvero una porzione di codice che vogliamo utilizzare e riutilizzare una o più volte per eseguire un compito specifico, dopo FUNCTION mettiamo un nome alla funzione.

es:

`function somma` ⇒ somma è il nome della funzione

al nome della funzione seguono una coppia di parentesi tonde e una coppia di parentesi graffe.

Le parentesi tonde servono ad inserire l’elenco dei parametri che ci aspettiamo che questa funzione possa ricevere, mentre la coppia di graffe va a delimitare il codice che rappresenta la funzione stessa, quindi quel codice che vogliamo rieseguire ogni volta che chiamiamo la funzione.

es:

`function somma (a, b) {`

`}`

La differenza rispetto alle variabili normali sta che nel fatto che il loro valore non viene indicato all’interno della definizione della funzioni ma è un valore che verrà indicato nel momento in cui la funzione verrà chiamata quindi (in un secondo momento) non sappiamo a priori quali saranno i valori a e b.

All’interno delle graffe possiamo fare quello che vogliamo, possiamo creare delle variabili, possiamo usare dei blocchi if oppure utilizzare dei cicli for o while, possiamo chiamare altre funzioni oppure possiamo restituire un valore.

`function somma (a+b) { function somma ( a, b) {`

`let result= a + b ⇒ return a +b }`

`return result`

`}`

**UNA VOLTA CHE ABBIAMO CREATO UNA VARIABILE COME FACCIAMO A RESTITUIRE UN RISULTATO?**

utilizzando la parola chiave RETURN la parole RETURN dice a java script che vogliamo uscire dalla funzione restituendo un risultato, il restituiamo alla funzione è il risultato dell’espressione che inseriamo subito dopo la parole chiave RETURN.

**COME FACCIAMO AD USARE QUESTA FUNZIONE ALL’INTERNO DEL NOSTRO CODICE?**

lo facciamo utilizzando il nome della funzione seguito da una coppia di parentesi tonde all’interno delle quali andiamo a mettere i valori che vogliamo dare ai parametri che questa funzione si aspetta di ricevere in questo caso A e B.

es:

`function somma (a ,b) {`

`return a + b`

`}`

`somma (2 , 3)`

In questo caso stiamo invocando la funzione che si chiama somma specificando due parametri, il parametro a prenderà prenderà il valore 2, il parametro b prenderà il valore 3, questa operazioni si chiama operazione di invocazione.

**COME FACCIAMO A CATTURARE IL VALORE CHE VIENE RESTITUITO DA UNA FUNZIONE?**

quello che possiamo fare è creare una variabile result che verrà valorizzata con il risultato dell’espressione.

`Function somma (a + b) {`

`return a + b`

`}`

`let result= somma ( 2, 3)`

`console.log (result)`

**COS’E’ CONSOLE.LOG?**

è una funzione che riceve un parametro, il parametro che riceve la funzione console.log rappresenta il messaggio che vogliamo che venga stampato all’interno della nostra console.

Una funzione può o meno ricevere dei parametri e può o meno restituire un valore.

es:

`function sayHello (nome) {`

`console.log (”hello” + nome + “!”)`

`sayHello (’Billy’)`

`}`

**COSA SUCCEDE SE PROVIAMO A CATTURARE IL VALORE RESTITUITO DA QUESTA FUNZIONE QUANDO LA FUNZIONE NON RESTITUISCE NULLA?**

cioè se provo a fare:

l`et hello= sayHello (’billy’)`

troviamo il valore `undefined,` ci uscirà solamente “`hello, billy!`”

il valore contenuto all’interno della variabile Hello sarà non definito, perché una funzione che non restituisce nulla di fatto sta restituendo un valore non definito, quindi il valore `undefind`.

**RICAPITOLANDO**

- Quando noi definiamo una funzione dobbiamo specificare il nome e l’elenco dei parametri che ovviamente non è obbligatorio e all’interno del corpo della funzione specificheremo tutte le operazioni che vogliamo fare.
- inoltre potremo specificare al suo interno anche il fatto che questa definizione debba restituire qualcosa , per esempio la somma di due valori o una stringa o qualsiasi altra cosa, questo valore lo potremo utilizzare, ad esempio, per valorizzare delle variabili o per effettuare altre operazioni.
- se una funzione non restituisce nulla non abbiamo bisogno di salvarci il risultato di queste funzioni perché la funzione non sta restituendo nulla con il suo risultato poiché il risultato non esiste.

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

- le funzioni sono importantissime, non solo in java script ma in ogni linguaggio di programmazione perché ci permettono di scrivere del codice una volta e riutilizzarlo tutte le volte che vogliamo.
- la complessità di una funzione può essere anche molto alta. All’interno di una funzione non dobbiamo necessariamente avere una riga di codice in cui facciamo solamente una cosa ma possiamo avere del codice anche meno complesso. Potremmo per esempio scrivere:

`Function somma (a, b) {`

`if ( a>5) {`

`return a*2 + b`

`}`

cioè delle condizioni che fanno biforcare il percorso della funzione e le fanno eseguire delle operazioni diverse in funzione di quelli che sono.

è possibile all’interno di una funzione sia farle prendere dei percorsi diversi sia farla uscire in qualunque momento utilizzando la parole chiave return.

- quindi una funzione può avere anche più di una parola chiave return, nel momento in cui abbiamo delle biforcazioni all’interno del nostro codice e abbiamo delle situazioni in cui vogliamo che la nostra funzione se succede una certa cosa deve restituire un certo risultato se ne succede un’altra avrà un alto risultato.
- EVITA FUNZIONI COMPLESSE
- SE HA PIU’ COSTRUTTI LA FUNZIONE SE RESTITUISCE UN NUMERO DEVE RESTITUIRE UN NUMERO, CIOE’: RESTITUIRE SEMPRE LO STESSO TIPO IN MODO TALE CHE SIA PIU’ COMPRENSIBILE.

### **Function Expressions**

JavaScript permette di assegnare comodamente le funzioni ad una variabile per utilizzarle in futuro.

`let sumFn = function (a, b) {`

`return a + b`

`}`

`let sum result = sumFn(2, 3)`

`console.log(sumResult)`

Qui è stata creata una variabile, all’interno della quale è presente una funzione.

Questo ci fa capire che in Java Script le funzioni sono a tutti gli effetti dei valori, dei valori che noi possiamo assegnare a delle variabili esattamente come se fossero dei numeri, delle stringhe o dei valori booleani.

C’è da specificare che in realtà le funzioni hanno una caratteristica diversa dai tipi primitivi, ovvero il fatto che sono delle referenze anziché dei valori veri e propri, quindi possiamo dare ad una variabile il valore che è una funzione stessa.

Quindi, quando assegniamo ad una variabile una valore e questo valore è una funzione, possiamo utilizzare questa variabile come se fosse una funzione, questo perchè di fatto quello che stiamo inserendo dentro questa variabile è un riferimento alla funzione stessa.

Possiamo anche evitare di dare un nome alla funzione ( funzione anonima) ma potrà comunque essere invocata perché il suo riferimento viene salvato all’interno di una variabile e quindi attraverso quella variabile andremo ad invocare la funzione stessa, questo tipo di approccio alle funzioni è detto FUNCTION EXPRESSION.

Questo tipo di approccio viene definito come FUNCTION EXPRESSION perchè quando noi definiamo una funzione stiamo di fatto scrivendo un’espressione, un’espressione il cui risultato è un riferimento all’espressione stessa che abbiamo definito.

IN JAVA SCRIPT TUTTO QUANTO RUOTA INTORNO AL CONCETTO DI ESPRESSIONE, cioè tutte le volte che facciamo qualcosa stiamo di fatto scrivendo un’espressione e il risultato di questa espressione può essere utilizzato all’interno di un’altra espressione.

- Le funzioni non devono necessariamente essere definite all’interno del nostro codice con un nome ma possono essere definite anche come espressioni vere e proprie.
- possiamo utilizzarle per valorizzare non soltanto delle variabili ma anche dei parametri di altre funzioni.

**ORDINE SINTASSI**

1. **Uso corretto delle parentesi**
    - Parentesi tonde `()` per le chiamate di funzione e le espressioni condizionali.
    - Parentesi graffe `{}` per i blocchi di codice.
2. **Spazi tra operatori e variabili**
    - Usa spazi per separare gli operatori dalle variabili e dai valori.
3. **Uso del punto e virgola `;`**
    - Usa il punto e virgola per terminare le dichiarazioni, evitando la dipendenza dall'inserimento automatico del punto e virgola (ASI).
4. **Indentazione**
    - Usa una corretta e coerente indentazione (generalmente 2 o 4 spazi per livello).
5. **Virgola finale nelle dichiarazioni di oggetti e array**
    - Inserisci una virgola finale nelle dichiarazioni di oggetti e array.
6. **Uso coerente delle virgolette**
    - Usa virgolette singole `'` o doppie `"` in modo coerente all'interno del codice.
7. **Uso di `const` e `let`**
    - Usa `const` per variabili immutabili e `let` per variabili che possono cambiare valore.
8. **Spazi in espressioni condizionali e cicli**
    - Aggiungi spazi prima e dopo gli operatori nelle espressioni condizionali e nei cicli.
9. **Commenti**
    - Utilizza commenti per spiegare porzioni di codice complesse o non immediatamente evidenti. Usa commenti su una riga o su più righe a seconda del contesto.
10. **Nomi chiari e descrittivi per variabili e funzioni**

- Usa nomi chiari e descrittivi, evitando abbreviazioni non comprensibili.

1. **Linee di codice brevi**

- Mantieni le linee di codice sotto i 80-100 caratteri per migliorare la leggibilità.

Adottando queste convenzioni, il codice sarà più leggibile, mantenibile e facilmente comprensibile, riducendo il rischio di errori e migliorando la collaborazione in team.