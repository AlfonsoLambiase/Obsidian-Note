## OPERATORI LOGICI

- **&&** (AND): restituisce **vero** solo se entrambe le condizioni sono vere.
- **||** (OR): restituisce **vero** se almeno una condizione è vera.
- **!** (NOT): inverte il valore di una condizione.

## OPERATORI DI CONFRONTO

- `==`: verifica se i valori sono uguali (ignora il tipo).
- `===`: verifica se i valori sono uguali **e dello stesso tipo**.
- `!=`: verifica se i valori sono diversi.
- `!==`: verifica se i valori sono **diversi o di tipo diverso**.
- `>`: verifica se il primo valore è maggiore.
- `<`: verifica se il primo valore è minore.
- `>=`: verifica se il primo valore è maggiore o uguale.
- `<=`: verifica se il primo valore è minore o uguale.

## OPERATORI DI CASTING

- **String()**: converte un valore in stringa.
- **Number()**: converte un valore in numero.
- **Boolean()**: converte un valore in booleano (`true` o `false`).
- **+** (unario): se applicato a una stringa, converte il valore in numero; se applicato a un numero, lo lascia invariato.
- (unario): converte forzatamente un valore in numero, restituendo `NaN` se non è convertibile

## RISULTATI TRUE/FALSE

L'operatore **AND** restituisce **true** solo se **entrambi** gli operandi sono **true:**

|Operando 1|Operando 2|Risultato (AND: `&&`)|
|---|---|---|
|true|true|true|
|true|false|false|
|false|true|false|
|false|false|false|

L'operatore **OR** restituisce **true** se almeno uno dei due operandi è **true:**

- **true || true** → **true** (entrambi sono true)
- **true || false** → **true** (almeno uno è true)
- **false || true** → **true** (almeno uno è true)
- **false || false** → **false** (entrambi sono false)

## OPERATORE TERNARIO

L'operatore ternario è una forma abbreviata per scrivere una condizione if-else. Invece di scrivere l'intero blocco `if-else`, puoi usare una sola riga con questa sintassi:

```jsx

risultato = condizione ? valore_se_vero : valore_se_falso;

```

- **condizione**: è l'espressione che vuoi verificare.
- **valore_se_vero**: il valore che viene assegnato a `risultato` se la condizione è vera.
- **valore_se_falso**: il valore che viene assegnato a `risultato` se la condizione è falsa.

