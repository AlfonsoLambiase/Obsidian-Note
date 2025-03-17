In un progetto `React,` i **componenti** sono come i **mattoncini Lego** che costruiscono la tua pagina web. Ogni componente è una piccola parte dell'interfaccia, come un bottone, un titolo, o una lista.

I componenti si mettono in una cartella chiamata **`components`** all'interno della cartella `src`.

Per usare un componente, lo **importiamo** nel file dove vogliamo usarlo e poi lo mettiamo dentro il nostro codice come un **mattoncino**.

Esempio di componente `Bottone.js`:

`// src/components/Bottone.js
```
function Bottone() {  
return <button>Click me!</button>; } 
export default Bottone;`
```

E nel componente principale `App.js`, lo usiamo così:

`import React from 'react';` 
`import Bottone from './components/Bottone';`

`function App() {` 
`return ( <div>` 
`<h1>Ciao, benvenuto!</h1>`
`<Bottone /> {/* Usiamo il componente Bottone */}` 
`</div> ); 
`}` 

`export default App;`

- I componenti vanno in **`src/components/`**.
- Li **importiamo** in altri file (come `App.js`) e li **usiamo** come mattoncini per costruire la UI.

`React` ti aiuta a costruire la tua app con componenti facili da organizzare e riutilizzare!