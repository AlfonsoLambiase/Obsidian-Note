_JSX_ è un'estensione di sintassi per JavaScript che consente di scrivere markup di tipo HTML all'interno di un file JavaScript.

# **JSX: inserimento del markup in JavaScript**

Il Web è stato costruito su HTML, CSS e JavaScript. Per molti anni, gli sviluppatori web hanno mantenuto il contenuto in HTML, il design in CSS e la logica in JavaScript, spesso in file separati.

Ma man mano che il Web diventava più interattivo, la logica determinava sempre di più i contenuti. JavaScript era responsabile dell'HTML, ecco perché **in React, la logica di rendering e il markup convivono nello stesso posto: i componenti.**

Ogni componente React è una funzione JavaScript che può contenere del markup che React renderizza nel browser.

JSX assomiglia molto a HTML, ma è un po' più rigido e può visualizzare informazioni dinamiche.

**NOTA!**

_JSX e React sono due cose separate. Spesso vengono usate insieme, ma puoi usarle [indipendentemente](https://reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html#whats-a-jsx-transform) l'una dall'altra. JSX è un'estensione di sintassi, mentre React è una libreria JavaScript._

**Le regole di JSX**

1. Restituisce un singolo elemento radice Per restituire più elementi da un componente, racchiuderli in un singolo tag padre.

Ad esempio, puoi usare <div>:

`<div> <h1>Hedy Lamarr's Todos</h1> <img src="[https://i.imgur.com/yXOvdOSs.jpg](https://i.imgur.com/yXOvdOSs.jpg)" alt="Hedy Lamarr" class="photo"

<ul> ... </ul> </div>`

Se non vuoi aggiungere un extra <div>al tuo markup, puoi scrivere <>e </>invece:

`<> <h1>Hedy Lamarr's Todos</h1> <img src="[https://i.imgur.com/yXOvdOSs.jpg](https://i.imgur.com/yXOvdOSs.jpg)" alt="Hedy Lamarr" class="photo"

<ul> ... </ul> </>`

Questo tag vuoto è chiamato **Fragment**. I **Fragment** ti permettono di raggruppare le cose senza lasciare traccia nell'albero HTML del browser.

**2. Chiudi tutti i tag** JSX richiede che i tag siano chiusi esplicitamente: i tag auto-chiudenti come `<img>`devono diventare `<img />`, e i tag di wrapping come `<li>`orange devono essere scritti come `<li>`oranges`</li>.`

ESEMPIO: `<> <img src="<https://i.imgur.com/yXOvdOSs.jpg>" alt="Hedy Lamarr" class="photo" /> <ul> <li>Invent new traffic lights</li> <li>Rehearse a movie scene</li> <li>Improve the spectrum technology</li> </ul> </>`

**3. camelCase per la maggior parte delle cose**

JSX si trasforma in JavaScript e gli attributi scritti in JSX diventano chiavi di oggetti JavaScript. Nei tuoi componenti, spesso vorrai leggere quegli attributi in variabili. Ma JavaScript ha delle limitazioni sui nomi delle variabili. Ad esempio, i loro nomi non possono contenere trattini o essere parole riservate come class.

Ecco perché, in React, molti attributi HTML e SVG sono scritti in camelCase. Ad esempio, invece di stroke-widthsi usa strokeWidth. Poiché classè una parola riservata, in React si scrive classNameinvece, denominata in base alla proprietà DOM corrispondente :

`<img src="<https://i.imgur.com/yXOvdOSs.jpg>" alt="Hedy Lamarr" className="photo" />`

# **Passaggio di stringhe con virgolette**

Quando si desidera passare un attributo stringa a JSX, è necessario inserirlo tra virgolette singole o doppie:

`export default function Avatar() { return ( <img className="avatar" src="<https://i.imgur.com/7vQD0fPs.jpg>" alt="Gregorio Y. Zara" /> ); }`

Ma cosa succede se vuoi specificare dinamicamente il testo src or alt? Puoi usare un valore da JavaScript sostituendo "and "con {and}

`export default function Avatar() { const avatar = '<https://i.imgur.com/7vQD0fPs.jpg>'; const description = 'Gregorio Y. Zara'; return ( <img className="avatar" src={avatar} alt={description} /> ); }`

# **Utilizzo delle parentesi graffe**

JSX è un modo speciale di scrivere JavaScript. Ciò significa che è possibile usare JavaScript al suo interno, con parentesi graffe { }.

`export default function TodoList() { const name = 'Gregorio Y. Zara'; return ( <h1>{name}'s To Do List</h1> ); }`

Qualsiasi espressione JavaScript funzionerà tra parentesi graffe, comprese le chiamate di funzione come `formatDate()`:

`const today = new Date();

function formatDate(date) { return new Intl.DateTimeFormat( 'en-US', { weekday: 'long' } ).format(date); }

export default function TodoList() { return ( <h1>To Do List for {formatDate(today)}</h1> ); }`

**Dove usare le parentesi graffe** È possibile utilizzare le parentesi graffe solo in due modi all'interno di JSX:

1. Come testo direttamente all'interno di un tag JSX: <h1>{name}'s To Do List</h1>funziona, ma <{tag}>Gregorio Y. Zara's To Do List</{tag}> non lo farà.
    
2. Poiché gli attributi seguono immediatamente il =segno: src={avatar}leggeranno la avatarvariabile, ma src="{avatar}"passeranno la stringa "{avatar}".
    

**Utilizzo di “doppi riccioli”: CSS e altri oggetti in JSX** Oltre a stringhe, numeri e altre espressioni JavaScript, puoi anche passare oggetti in JSX. Gli oggetti sono anche indicati con parentesi graffe, come `{ name: "Hedy Lamarr", inventions: 5 }`. Pertanto, per passare un oggetto JS in JSX, devi racchiudere l'oggetto in un'altra coppia di parentesi graffe: `person={{ name: "Hedy Lamarr", inventions: 5 }}`.

Potresti vedere questo con gli stili CSS inline in JSX. React non richiede di usare stili inline (le classi CSS funzionano benissimo nella maggior parte dei casi). Ma quando hai bisogno di uno stile inline, passi un oggetto all'attributo style:

`export default function TodoList() { return ( <ul style={{ backgroundColor: 'black', color: 'blue' }}> <li>Improve the videophone</li> <li>Prepare aeronautics lectures</li> <li>Work on the alcohol-fuelled engine</li> </ul> ); }`

# **oggetti JavaScript e le parentesi graffe**

È possibile spostare più espressioni in un unico oggetto e farvi riferimento nel JSX tra parentesi graffe:

`const person = { name: 'Gregorio Y. Zara', theme: { backgroundColor: 'black', color: 'pink' } };

export default function TodoList() { return ( <div style={person.theme}> <h1>{[person.name](http://person.name)}'s Todos</h1> <img className="avatar" src="[https://i.imgur.com/7vQD0fPs.jpg](https://i.imgur.com/7vQD0fPs.jpg)" alt="Gregorio Y. Zara" /> <ul> <li>Improve the videophone</li> <li>Prepare aeronautics lectures</li> <li>Work on the alcohol-fuelled engine</li> </ul> </div> ); }`

In questo esempio, l' person oggetto JavaScript contiene una namestringa e un themeoggetto:

JSX è un linguaggio di template molto minimale perché consente di organizzare dati e logica utilizzando JavaScript.

**Ricapitolare** JSX:

- Gli attributi JSX tra virgolette vengono passati come stringhe.
- Le parentesi graffe consentono di integrare la logica e le variabili JavaScript nel markup.
- Funzionano all'interno del contenuto del tag JSX o subito dopo =negli attributi.
- {{e }}non si tratta di una sintassi speciale: è un oggetto JavaScript racchiuso tra parentesi graffe JSX.