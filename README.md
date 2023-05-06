# Tutorial Python in italiano

### Capitoli:
- [Data types](#data-types)
  - [str](#str)
  - [int](#int)
  - [float](#float)
  - [bool](#bool)
- [Variabili](#variabili)
- [Come funziona il codice](#come-funziona-il-codice)
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
## Come funziona il codice?
Finora ti ho solo spiegato in che modo giocare con dati all'interno del programma, ma in che modo funziona esattamente?
Un programma non è altro che un documento di testo, che viene letto da un altro programma che lo trasforma in azioni che il computer farà.

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
