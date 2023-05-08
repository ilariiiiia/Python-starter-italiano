# Tutorial Python in italiano

### Capitoli:
- [Data types](#data-types)
  - [str](#str)
  - [int](#int)
  - [float](#float)
  - [bool](#bool)
- [Variabili](#variabili)
- [Come funziona il codice](#come-funziona-il-codice)
- [Operatori condizionali](#operatori-condizionali)
  * ==
  * !=
  * \>
  * <
  * \>=
  * <=
  * and
  * not
  * if
  * else
  * elif
  * while
- [Funzioni](#funzioni)
    - [Funzioni avanzate](#funzioni-avanzate)
    
## Data types

I computer, come forse sai, vengono usati per due principali motivi:
- mantenere dati
- fare calcoli
In questo caso, ci soffermeremo sul primo.

Tutti i dati di un computer sono rappresentabili con degli 0 e 1, che corrispondono alla presenza o meno di elettroni nella memoria del computer.

Non è necessario sapere in che modo si passa da `01100001` ad `a`, ma ti basta sapere che tutto è fatto allo stesso modo.

I data types sono dei modi di classificare i dati, ognuno dei quali ha particolari proprietà.

In Python specificamente, ci sono 15 data types, ma in questo momento te ne analizzerò solo 4.

#### str
Le stringhe (str) sono semplicemente del testo. In Python, questo può essere rappresentato avvolgendo del testo con ' o ".
Per esempio, 'Ciao!' è valido, e "Ciao!" pure; ma non si possono mescolare ' e " nella stessa stringa: "Ciao!' non è valido.
è però possibile inserire una all'interno dell'altra senza problemi. Cioè, "c'è" è valido e corrisponde al testo `c'è`.

Usare " o ' è completamente indifferente

#### int
Gli integers (int) sono i numeri interi. Si rappresentano scrivendo il numero direttamente, tipo `1` o `872364`.
Include i numeri negativi, tipo `-563` e `-105`.

#### float
I floating point numbers (float) sono dei numeri decimali, o comunque la rappresentazione decimale di un qualsiasi numero.
Per esempio, 0.5, -1.4 e 3.14 sono tutti dei float. Anche 3.0 è un float, seppur sia in realtà un numero intero.

#### bool
I booleani (bool) rappresentano vero o falso. In Python, questi sono rappresentati come `True` e `False`.

Esempi in codice:

```python
"Ciao!"
'Ciao!'
"C'è"

3
4
5
10
987682734

0.5
2.5
3.0
283746.76358

True
False
```

## Variabili
Le variabili sono semplicemente dei "contenitori" che contengono dei dati. Per definire una variabile, basta mettere il nome della variabile con l'operatore di assegnazione = e il valore della variabile.
Per esempio, per dare il valore "Ilaria" alla variabile nome, basta fare così:
```python
nome = "Ilaria"
```
Posso anche dare il valore di una variabile ad un altra variabile, per esempio
```python
nome = "Ilaria"
altronome = nome
```
In questo caso, sia `nome` che `altronome` avranno il valore di `"Ilaria"`

Le variabili possono cambiare il loro valore all'interno del programma, e possono diventare di altri data type.
Per esempio,
```python
i = "Ilaria"
i = 3
i = True
i = False
i = 3.56
```
P.S. sebbene sia possibile farlo, non è consigliato dare nomi a variabili con lettere diverse dall'alfabeto standard, cioè meglio usare solo lettere senza accenti.

## Come funziona il codice?
Finora ti ho solo spiegato in che modo giocare con dati all'interno del programma, ma in che modo funziona esattamente?
Un programma non è altro che un documento di testo, che viene trasformato in istruzioni che il computer eseguirà.

Senza stare a guardare i dettagli, di cui ci interessa ben poco, parliamo di ciò che ci interessa.

Un programma viene letto dalla prima riga all'ultima, ed eseguita in ordine.
Per esempio, se abbiamo un programma del tipo
```python
print("Io vengo prima!")

print("Io vengo dopo!")
```
la prima linea sarà letta ed eseguita per prima, poi la seconda, e poi la terza.

Se una linea non contiene codice, cioè è bianca o contiene commenti (poi ti faccio vedere), essa verrà ignorata.

#### Commenti

Spesso è difficile capire che cosa fa un pezzo di codice, anche se l'hai scritto tu.
Per questo, tanti linguaggi di programmazione hanno i commenti.
I commenti non sono altro che del testo che puoi mettere all'interno del codice per commentarlo.
Generalmente viene usato per spiegare in che modo funziona il codice o come usarlo.

In Python, i commenti vengono scritti con un # davanti. Tutto ciò che rimane dopo l'#, nella stessa linea, verrà ignorato.
Prima dell'#, se c'è del codice, esso verrà letto ed eseguito.

## Operatori condizionali

Per quanto i programmi vadano sempre dalla prima linea all'ultima, ci sono pezzi di codice che possono invece procedere in modi alternativi.
Questi succedono se avvengono delle particolari condizioni. Per testare queste condizioni, si usano gli operatori condizionali.

Prima di parlare di loro però, parliamo di valori Truthy e Falsy.
In Python, quasi tutto è Truthy, cioè considerato "vero" nelle operazioni condizionali.
Le uniche eccezioni sono gli oggetti vuoti, tipo stringhe vuote `''`, liste vuote `[]` e dizionari vuoti `{}`.
So che non ti ho spiegato che cosa siano gli ultimi due, ma ritenevo importante menzionarlo.

Gli operatori condizionali sono vari:
* ==
* !=
* \>
* <
* \>=
* <=
* and
* not

#### ==
Controlla se due valori sono uguali. Per esempio, `5==5` sarà `True`, ma `5=='5'` sarà False.
Se i due sono di diversi data type, sarà falso.

#### !=
Dà l'opposto di ==. Anche chiamato "non uguale a". `5!=2` dà `False`.

#### >
Dice se il primo è maggiore del secondo. Funziona solo su numeri, anche tra int e float.

#### <
Dice se il primo è minore del secondo. Funziona solo su numeri, anche tra int e float.

#### >=
Dice se il primo è maggiore o uguale al secondo. Funziona solo su numeri, anche tra int e float.

#### <=
Dice se il primo è minore o uguale al secondo. Funziona solo su numeri, anche tra int e float.

#### not
Dà l'opposto di quanto davanti. `not True` sarà `False`, mentre `not False` è `True`.

#### and
Ritorna vero solo se entrambe le condizioni sono vere.
Qui la tabella:

| -     | True  | False |
|-------|-------|-------|
| True  | True  | False |
| False | False | False |

si usa come `condizione and condizione`, tipo `5==3 and 3!=6`.

#### or
Ritorna vero se almeno una delle due condizioni è vera.
Qui la tabella:

| -     | True  | False |
|-------|-------|-------|
| True  | True  | True  |
| False | True  | False |

Questi operatori possono essere usati insieme ai dichiaratori condizionali `if`, `else`, `elif`, e `while`
per creare blocchi di codice che vengono eseguiti solo sotto particolari condizioni.

#### if

Gli if-statements fanno eseguire un particolare pezzo di codice solo se la condizione al loro interno è veritiera (Truthy). Altrimenti, lo salta interamente.

Per indicare quale codice è interno all'if-statement, come per tutti gli altri che vedremo, lo si *indenta*, cioè si aggiungono spazi o tab a sinistra del codice.

Per esempio, per print-are `Puoi bere!` solo se si è maggiorenni:

```python
if eta >= 18:
  print("Puoi bere!")
```

#### else

Come probabilmente avrai intuito, questi vengono messi dopo un blocco `if` per eseguire del codice nel caso in cui la condizione dell-`if` NON sia avvenuta.
Per espandere il problema di prima,

```python
if eta > 18:
  print("Puoi bere!")
else:
  print("Ti toccherà aspettare...")
```

#### elif

Sta per "else if". Con esso puoi far eseguire diverse linee di codice secondo varie condizioni, senza indentare troppo.
Per esempio, qui viene print-ato qualcosa di diverso a seconda dell'età dell'utente
```python
if eta > 65:
  print("Sei un senior!")
elif eta > 18:
  print("Sei un adulto!")
else:
  print("Sei un bambino!")
```

#### while

I while loop eseguono il codice al loro interno per quanto la condizione al loro interno sia vera.
Se questa condizione dovesse continuare ad essere vera per sempre, allora si parla di loop infinito.

Per esempio, questo codice print-a tutti i numeri dallo 0 al 10:

```python
counter = 0
while counter <= 10:
  print(counter)
  counter = counter + 1
```
