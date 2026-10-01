# Raccolta Esercizi di Algoritmi e Flowchart

Introduzione alla programmazione: dai diagrammi di flusso a Python.

---

## Come usare questa raccolta

1. Leggi con attenzione il testo dell'esercizio.
2. Prima di disegnare, scrivi i **dati di input** e i **dati di output**.
3. Disegna il flowchart.
4. Solo a questo punto apri la sezione **Caso prova** sotto l'esercizio e verifica la soluzione: il tuo flowchart deve produrre esattamente quei risultati.

Alcuni esercizi hanno anche un **Suggerimento** (leggilo solo se sei bloccato) e una nota **Verso Python**, che indica il costrutto Python corrispondente a ciò che stai disegnando.

Gli esercizi sono indicati con un codice univoco: **S1-E7** significa *Sezione 1, Esercizio 7*.

### Convenzione sugli intervalli

In tutta la raccolta, "da *a* a *b*" significa **estremi inclusi**. Esempio: "da 0 a 3" → 0, 1, 2, 3.

> ⚠️ In Python `range(0, 3)` produce 0, 1, 2: il secondo estremo è **escluso**. Per arrivare a 3 serve `range(0, 4)`.

### Simboli dei flowchart

| Simbolo | Forma | Uso |
|---|---|---|
| Inizio / Fine | Ovale | Primo e ultimo blocco dell'algoritmo |
| Input / Output | Parallelogramma | Leggere un dato, mostrare un risultato |
| Elaborazione | Rettangolo | Calcoli e assegnazioni (`area ← base * altezza`) |
| Decisione | Rombo | Condizione con due uscite: Vero / Falso |
| Flusso | Freccia | Ordine di esecuzione |

Strumenti consigliati: [diagrams.net](https://app.diagrams.net) (da browser)

### Tre parole da conoscere

- **Contatore**: variabile che conta *quante volte* succede qualcosa (`conta ← conta + 1`).
- **Accumulatore**: variabile che somma *dei valori* (`somma ← somma + x`).
- **Flag**: variabile Vero/Falso che ricorda *se* è successo qualcosa (`trovato ← Vero`).

Contatori e accumulatori vanno sempre **inizializzati** (di solito a 0) prima di essere usati.

---

## SEZIONE 1 – Sequenza e Selezione

### S1-E1: Area di un Rettangolo

Algoritmo che, dati la base e l'altezza di un rettangolo, calcola e fornisce in output l'area.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 4, 3 | 12 |
| 2.5, 2 | 5 |

</details>

**Verso Python:** `input()`, `float()`, operatore `*`, `print()`.

---

### S1-E2: Area e Lunghezza della Circonferenza

Algoritmo che riceve in ingresso il raggio di un cerchio e calcola sia l'area del cerchio sia la lunghezza della circonferenza.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso (arrotondato) |
|---|---|
| 1 | area 3.14 · circonferenza 6.28 |
| 2 | area 12.57 · circonferenza 12.57 |

</details>

**Suggerimento:** area = π · r², circonferenza = 2 · π · r.

**Verso Python:** `import math`, `math.pi`, `round(valore, 2)`.

---

### S1-E3: Il Maggiore tra Due Numeri

Algoritmo che, dati due numeri, restituisce il valore maggiore. Se i due numeri sono uguali, l'algoritmo lo segnala con il messaggio "I numeri sono uguali".

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 7, 3 | 7 |
| -2, 5 | 5 |
| 4, 4 | I numeri sono uguali |

</details>

**Verso Python:** `if` / `elif` / `else`.

---

### S1-E4: Costo Visita al Museo e Controllo Budget

Una classe organizza una visita al museo. Conoscendo il numero di studenti e il prezzo del biglietto per ciascuno, l'algoritmo calcola e mostra il costo totale della visita. Se il costo supera il budget di 100 €, segnala anche un avviso di "Over Budget".

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 20, 4.50 | 90 |
| 25, 4.50 | 112.5 · Over Budget |
| 20, 5 | 100 *(non supera il budget)* |

</details>

**Suggerimento:** salva il budget in una variabile (`BUDGET ← 100`) invece di scrivere 100 direttamente nella condizione. "Supera" significa `>`, non `>=`.

**Verso Python:** costanti in maiuscolo (`BUDGET = 100`), `if` senza `else`.

---

### S1-E5: Differenza o Somma con Convalida dell'Input

Dati in ingresso due valori, l'algoritmo calcola e fornisce in output la loro differenza se il primo è maggiore del secondo, altrimenti la loro somma. Prima del calcolo, l'algoritmo controlla che i due valori non siano uguali: in quel caso mostra il messaggio "Errore: i valori devono essere diversi" e termina.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 9, 4 | 5 |
| 3, 8 | 11 |
| 5, 5 | Errore: i valori devono essere diversi |

</details>

**Verso Python:** `if` / `elif` / `else`, operatore `==`.

---

### S1-E6: Moltiplicazione o Selezione in Base al Segno

Dati in ingresso due valori, se il primo è positivo l'algoritmo fornisce in output il loro prodotto; se invece il primo è negativo, manda in output direttamente il secondo valore. Se il primo valore è zero, l'algoritmo mostra il messaggio "Il primo valore è zero".

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3, 4 | 12 |
| -2, 7 | 7 |
| 0, 5 | Il primo valore è zero |

</details>

**Per riflettere:** lo zero non è né positivo né negativo. Cosa farebbe il tuo algoritmo se ti fossi dimenticato di questo caso?

**Verso Python:** `if` / `elif` / `else` con tre rami.

---

### S1-E7: Pari o Dispari

Dato in ingresso un numero intero positivo, l'algoritmo stabilisce se è pari o dispari. Se il numero inserito non è positivo, l'algoritmo mostra un messaggio di errore.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 8 | pari |
| 7 | dispari |
| -4 | Errore: inserire un numero positivo |

</details>

**Suggerimento:** un numero è pari se il **resto** della divisione per 2 è 0. Nota: anche 0 è pari; qui il vincolo "positivo" serve solo per esercitare il controllo dell'input.

**Verso Python:** operatore resto `%`, `int()`.

---

### S1-E8: Somma di Valori Esclusivamente Positivi

Dati in ingresso due valori qualsiasi, l'algoritmo fornisce in output la loro somma solo se entrambi sono maggiori di 0, altrimenti segnala un errore.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3, 4 | 7 |
| 3, -1 | Errore |
| 0, 5 | Errore *(0 non è maggiore di 0)* |

</details>

**Verso Python:** operatore logico `and`.

---

### S1-E9: Somma dei Valori Pari (accumulatore)

Dati in ingresso due valori, l'algoritmo analizza un valore alla volta e lo aggiunge alla somma solo se è pari. Alla fine mostra la somma ottenuta.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 4, 6 | 10 |
| 4, 7 | 4 |
| 3, 5 | 0 |

</details>

**Suggerimento:** usa un **accumulatore** `somma ← 0`, poi controlla un valore alla volta e, se è pari, aggiungilo.

**Verso Python:** `somma += a`, due `if` separati (non `elif`!).

---

### S1-E10: Mostrare Solo i Valori Dispari (flag)

Dati in ingresso due valori, l'algoritmo mostra in output solo quelli che risultano dispari. Se nessuno dei due è dispari, mostra il messaggio "Nessun valore dispari".

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3, 8 | 3 |
| 5, 9 | 5, 9 |
| 2, 4 | Nessun valore dispari |

</details>

**Suggerimento:** usa un **flag** `trovato ← Falso` e mettilo a Vero quando mostri un valore.

**Verso Python:** variabili booleane `True` / `False`, `if not trovato:`.

---

### S1-E11: Contare i Valori Dispari (contatore)

Dati in ingresso due valori, l'algoritmo conta quanti di essi sono dispari e mostra il risultato (0, 1 oppure 2).

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3, 8 | 1 |
| 5, 9 | 2 |
| 2, 4 | 0 |

</details>

**Per riflettere:** confronta con S1-E9. Qual è la differenza tra un contatore e un accumulatore?

**Verso Python:** `conta += 1`.

---

### S1-E12: Il Maggiore tra Tre Numeri

Dati tre numeri in ingresso, l'algoritmo ne confronta i valori e fornisce in output il massimo.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3, 9, 5 | 9 |
| 8, 2, 6 | 8 |
| 7, 7, 2 | 7 |

</details>

**Sfida:** risolvi l'esercizio in due modi: con selezioni annidate e con condizioni composte (`and`). Quale flowchart è più leggibile?

**Verso Python:** `if` annidati, `and`. *(Esiste anche `max(a, b, c)`, ma qui l'obiettivo è costruire la logica.)*

---

### S1-E13: Somma dei Numeri Pari e Positivi

Dati tre numeri, l'algoritmo verifica per ciascuno se è **contemporaneamente** maggiore di zero e pari; i numeri che rispettano entrambe le condizioni vengono sommati e alla fine viene mostrata la somma.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 4, -2, 6 | 10 |
| 3, 5, 7 | 0 |
| -4, 2, 8 | 10 |

</details>

**Verso Python:** `if x > 0 and x % 2 == 0:`.

---

### S1-E14: Decine e Unità

Dato un numero intero di due cifre (da 10 a 99), l'algoritmo ricava e mostra la cifra delle decine, la cifra delle unità e la loro somma. Se il numero inserito non ha due cifre, mostra un messaggio di errore.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 47 | 4, 7, 11 |
| 90 | 9, 0, 9 |
| 105 | Errore |

</details>

**Suggerimento:** decine = divisione intera per 10; unità = resto della divisione per 10.

**Verso Python:** divisione intera `//`, resto `%`.

---

## SEZIONE 2 – Strutture Iterative

### Parte A – Cicli a conteggio

### S2-E1: Numeri da 0 a 3

Usando un ciclo con una variabile contatore, l'algoritmo mostra in sequenza i numeri da 0 a 3.

<details>
<summary>Caso prova</summary>

**Risultato atteso:** 0, 1, 2, 3

</details>

**Verso Python:** `for i in range(0, 4):` (il 4 è escluso!).

---

### S2-E2: Numeri Pari da 0 a 5

L'algoritmo esegue un ciclo da 0 a 5 e mostra in output solo i numeri pari incontrati.

<details>
<summary>Caso prova</summary>

**Risultato atteso:** 0, 2, 4

</details>

**Sfida:** risolvilo in due modi: (1) ciclo di passo 1 con controllo del resto; (2) ciclo di passo 2, senza controllo. Quale fa meno operazioni?

**Verso Python:** `range(0, 6)` con `if`, oppure `range(0, 6, 2)`.

---

### S2-E3: Somma dei Numeri da 0 a 10

L'algoritmo esegue un ciclo per calcolare e mostrare la somma di tutti i numeri interi da 0 a 10.

<details>
<summary>Caso prova</summary>

**Risultato atteso:** 55

</details>

**Per riflettere:** la formula di Gauss n·(n+1)/2 dà lo stesso risultato. Usala per verificare il tuo algoritmo.

**Verso Python:** accumulatore dentro un `for`.

---

### S2-E4: Somma dei Numeri Dispari da 5 a 15

L'algoritmo esegue un ciclo da 5 a 15, controlla per ogni numero se è dispari e, in quel caso, lo aggiunge alla somma. Alla fine mostra la somma ottenuta.

<details>
<summary>Caso prova</summary>

**Risultato atteso:** 60 *(5 + 7 + 9 + 11 + 13 + 15)*

</details>

**Verso Python:** `range(5, 16)`.

---

### S2-E5: Quanti Multipli di 3?

L'algoritmo conta quanti numeri da 1 a 30 sono multipli di 3 e mostra il risultato.

<details>
<summary>Caso prova</summary>

**Risultato atteso:** 10

</details>

**Verso Python:** contatore dentro un `for`, `if i % 3 == 0:`.

---

### S2-E6: Il Massimo tra N Numeri

L'utente indica quanti numeri vuole inserire, poi li inserisce uno alla volta. Al termine, l'algoritmo mostra il più grande tra i numeri inseriti.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 4 numeri: 3, 9, 2, 5 | 9 |
| 3 numeri: -7, -2, -5 | -2 |

</details>

**Suggerimento:** non inizializzare il massimo a 0: con il secondo caso prova otterresti un risultato sbagliato. Usa il **primo numero inserito** come massimo iniziale.

**Verso Python:** `for` con `input()` dentro il ciclo.

---

### Parte B – Cicli indefiniti

Un ciclo indefinito si ripete **finché una condizione è vera**: non si sa in anticipo quante volte verrà eseguito. È lo strumento giusto per controllare l'input dell'utente.

### S2-E7: Somma da 0 a x con Validazione

Dato un numero intero positivo inserito dall'utente, l'algoritmo calcola e mostra la somma di tutti i numeri da 0 a quel numero. Se il numero inserito non è positivo, l'algoritmo lo richiede finché l'utente non ne inserisce uno valido.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 4 | 10 |
| -3, poi 0, poi 4 | (richiesta ripetuta due volte) 10 |

</details>

**Verso Python:** `while x <= 0:` per la validazione, poi `for i in range(0, x + 1):`.

---

### S2-E8: C'è un Numero Negativo?

L'utente indica quanti numeri vuole inserire, poi li inserisce uno alla volta. Al termine, l'algoritmo mostra "Presente almeno un negativo" se tra i numeri inseriti ce n'è almeno uno negativo, altrimenti "Nessun negativo".

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 4 numeri: 3, -1, 5, 2 | Presente almeno un negativo |
| 3 numeri: 4, 0, 7 | Nessun negativo |

</details>

**Suggerimento:** usa un **flag**. Attenzione: una volta messo a Vero, non deve tornare Falso.

**Verso Python:** variabile booleana dentro un `for`.

---

## SEZIONE 3 – Ripasso: i Quattro Schemi Fondamentali

Questi quattro esercizi riassumono le strutture viste. Sono utili anche come **esempi modello** prima di affrontare le sezioni precedenti.

### S3-E1: Sequenza

Algoritmo in sequenza che riceve due valori in ingresso, ne calcola la somma e il prodotto e mostra entrambi i risultati.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3, 4 | somma 7 · prodotto 12 |

</details>

---

### S3-E2: Selezione

Algoritmo che, data l'età di una persona, stabilisce e comunica se è maggiorenne o minorenne.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 18 | Maggiorenne |
| 15 | Minorenne |

</details>

**Per riflettere:** la condizione è `età >= 18` oppure `età > 18`? Prova con 18.

---

### S3-E3: Ciclo Definito (Tabellina)

Dato un numero inserito dall'utente, l'algoritmo mostra la sua tabellina, moltiplicandolo per un contatore che va da 0 a 10.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 3 | 0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30 |

</details>

**Verso Python:** `for i in range(0, 11):`.

---

### S3-E4: Ciclo Indefinito (Somma a Oltranza)

L'utente inserisce numeri uno alla volta e l'algoritmo li somma, continuando finché la somma diventa **maggiore di 100**. Alla fine mostra la somma ottenuta e quanti numeri sono stati inseriti.

<details>
<summary>Caso prova</summary>

| Valori inseriti | Risultato atteso |
|---|---|
| 40, 50, 30 | somma 120 · numeri inseriti 3 |
| 60, 40, 1 | somma 101 · numeri inseriti 3 *(con 100 il ciclo continua)* |

</details>

**Per riflettere:** cosa succede se l'utente inserisce numeri negativi? Il ciclo potrebbe non terminare mai? Proponi una modifica per evitarlo.

**Verso Python:** `while somma <= 100:`.

---

## Appendice – Dal Flowchart a Python

| Nel flowchart | In Python |
|---|---|
| Input di un numero | `x = int(input("Numero: "))` oppure `float(...)` |
| Output | `print(x)` |
| Assegnazione `a ← 5` | `a = 5` |
| Uguaglianza nella condizione | `==` (un solo `=` è un'assegnazione!) |
| Diverso | `!=` |
| Resto della divisione | `%` |
| Divisione intera | `//` |
| Decisione con due uscite | `if ... :` / `else:` |
| Più decisioni in cascata | `if` / `elif` / `else` |
| E / O / NON | `and` / `or` / `not` |
| Ciclo con contatore da a a b | `for i in range(a, b + 1):` |
| Ciclo finché condizione vera | `while condizione:` |

> ⚠️ `input()` restituisce **sempre una stringa**: `"3" + "4"` dà `"34"`, non 7. Ricordati di convertire con `int()` o `float()`.

---

# Licenza

Questo progetto e i materiali al suo interno sono distribuiti con licenza **[CC BY-NC-SA 4.0](http://creativecommons.org/licenses/by-nc-sa/4.0/)** (Creative Commons Attribuzione - Non commerciale - Condividi allo stesso modo 4.0 Internazionale).

[![CC BY-NC-SA 4.0](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)
