I componenti React usano le props per comunicare tra loro. Ogni componente padre può passare alcune informazioni ai suoi componenti figlio fornendo loro delle props. Le props potrebbero ricordarti gli attributi HTML, ma puoi passare qualsiasi valore JavaScript attraverso di esse, inclusi oggetti, array e funzioni.

I prop sono le informazioni che passi a un tag JSX. Ad esempio, className, src, alt, width, e height sono alcuni dei prop che puoi passare a un <img:


`function Avatar() { return ( <img className="avatar" src="[https://i.imgur.com/1bX5QH6.jpg](https://i.imgur.com/1bX5QH6.jpg)" alt="Lin Lanying" width={100} height={100} /> ); }
```
export default function Profile() { return ( <Avatar /> ); }`
```

###### **Passaggio di oggetti di scena a un componente**

In questo codice, il Profile componente non passa alcuna proprietà al suo componente figlio Avatar:

`export default function Profile() { return ( <Avatar /> ); }`

Puoi dare Avatar qualche sostegno in due passaggi:

###### **Passaggio 1: passare le proprietà al componente figlio**

Per prima cosa, passiamo alcuni prop a Avatar. Ad esempio, passiamo due prop: person(un oggetto) e size(un numero):

`export default function Profile() { return ( <Avatar person={{ name: 'Lin Lanying', imageId: '1bX5QH6' }} size={100} /> ); }`

###### **Passaggio 2: leggere le proprietà all'interno del componente figlio**

Puoi leggere queste prop elencandone i nomi person, size separati dalle virgole all'interno ({e })subito dopo function Avatar. Questo ti consente di usarle all'interno del Avatarcodice, come faresti con una variabile.

`function Avatar({ person, size }) { // person and size are available here }`

Aggiungi un po' di logica Avata rche utilizza le proprietà persone size per il rendering, e il gioco è fatto.

Ora puoi configurare Avatar il rendering in molti modi diversi con diversi prop. Prova a modificare i valori!

`import { getImageUrl } from './utils.js';`

`function Avatar({ person, size }) { return ( <img className="avatar" src={getImageUrl(person)} alt={[person.name](<http://person.name/>)} width={size} height={size} /> ); }`

`export default function Profile() { return ( <div> <Avatar size={100} person={{ name: 'Katsuko Saruhashi', imageId: 'YfeOqp2' }} /> <Avatar size={80} person={{ name: 'Aklilu Lemma', imageId: 'OKS67lh' }} /> <Avatar size={50} person={{ name: 'Lin Lanying', imageId: '1bX5QH6' }} /> </div> ); }`

i prop sono l'unico argomento per il tuo componente! Le funzioni dei componenti React accettano un singolo argomento, un props oggetto:

```
`function Avatar(props) {`

`let person = props.person;`

`let size = props.size;`

`// ...`

`}` 
```




