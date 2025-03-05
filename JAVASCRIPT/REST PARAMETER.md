Il **rest parameter** in JavaScript permette di raccogliere un numero indefinito di argomenti passati a una funzione e trattarli come un array. È utile quando non sai quanti argomenti verranno passati alla funzione.

**Ecco un esempio:**

```jsx

function mostraNumeri(...numeri) {
  console.log(numeri);
}

mostraNumeri(1, 2, 3, 4);
// Stampa: [1, 2, 3, 4]

```

In questo caso:

- `...numeri` è il **rest parameter**. Raccoglie **tutti** i numeri che vengono passati alla funzione e li mette dentro un array chiamato `numeri`.

### Cosa fa il rest parameter?

- Raccoglie tutti gli argomenti rimanenti dopo che sono stati definiti gli altri parametri della funzione.
- È particolarmente utile per funzioni che devono gestire un numero variabile di argomenti.