
# Raccolta Esercizi di Algoritmi e Flowchart

---

## SEZIONE 1: Algoritmi Sequenziali e Condizionali Semplici

### Esercizio 1: Calcolo dell'Area di un Rettangolo
Algoritmo che, dati i due lati di un rettangolo, calcola e fornisce in output l'area.
* **Dati di input:** base, altezza
* **Dati di output:** area

```mermaid
graph TD
    START([START]) --> INPUT[/IN B<br>IN A/]
    INPUT --> PROCESS[AREA = B * A]
    PROCESS --> OUTPUT[/OUT AREA/]
    OUTPUT --> STOP([STOP])

```

### Esercizio 2: Area e Perimetro del Cerchio

Algoritmo che riceve in ingresso il raggio di un cerchio e calcola sia l'area che il perimetro.

* **Dati di input:** raggio
* **Dati di output:** area, perimetro

```mermaid
graph TD
    START([START]) --> INPUT[/IN R/]
    INPUT --> PROCESS["A = pi * R^2<br>P = 2 * pi * R"]
    PROCESS --> OUTPUT_A[/OUT A/]
    PROCESS --> OUTPUT_P[/OUT P/]
    OUTPUT_A --> STOP([STOP])
    OUTPUT_P --> STOP

```

### Esercizio 3: Il Maggiore tra Due Numeri

Algoritmo che, dati due numeri diversi, restituisce il valore maggiore.

* **Dati di input:** due numeri x e y
* **Dati di output:** il numero maggiore

```mermaid
graph TD
    START([START]) --> INPUT[/IN X<br>IN Y/]
    INPUT --> COND{"X > Y"}
    COND -- V --> OUT_X[/OUT X/]
    COND -- F --> OUT_Y[/OUT Y/]
    OUT_X --> STOP([STOP])
    OUT_Y --> STOP

```

### Esercizio 4: Calcolo Costo Visita Museo e Controllo Budget

Algoritmo che calcola il costo totale della visita per un gruppo di studenti. Nel caso in cui il costo sia superiore a 100, segnala un avviso di "Over Budget".

* **Dati di input:** numero studenti (n), prezzo biglietto (p)
* **Dati di output:** costo totale (c), avviso

```mermaid
graph TD
    START([START]) --> INPUT[/IN n<br>IN p/]
    INPUT --> PROCESS[c = n * p]
    PROCESS --> COND{"c > 100"}
    COND -- V --> OUT_WARN[/OUT "Over Budget"/]
    COND -- F --> OUT_C[/OUT c/]
    OUT_WARN --> OUT_C
    OUT_C --> STOP([STOP])

```

---

### Esercizio 5: Differenza o Somma con Convalida dell'Input

Dati in ingresso due valori diversi, l'algoritmo calcola e fornisce in output la loro differenza se il primo è maggiore del secondo, altrimenti la loro somma. Include una deviazione di controllo per verificare che i valori inseriti non siano uguali.

* **Dati di input:** x e y
* **Dati di output:** d (differenza) oppure s (somma)

```mermaid
graph TD
    START([START]) --> INPUT[/IN x<br>IN y/]
    INPUT --> CHK{"x == y"}
    CHK -- V --> ERR[/OUT "Attenzione, inserisci due valori diversi"/]
    ERR --> INPUT
    CHK -- F --> COND{"x > y"}
    COND -- V --> DIFF[d = x - y]
    COND -- F --> SOMMA[s = x + y]
    DIFF --> OUT_D[/OUT d/]
    SOMMA --> OUT_S[/OUT S/]
    OUT_D --> STOP([STOP])
    OUT_S --> STOP

```

### Esercizio 6: Moltiplicazione o Selezione Valore in Base al Segno

Dati in ingresso due valori, se il primo valore è positivo l'algoritmo fornisce in output la loro moltiplicazione, altrimenti se il primo valore è negativo manda in output direttamente il secondo valore.

* **Dati di input:** x e y
* **Dati di output:** m (moltiplicazione) oppure y

```mermaid
graph TD
    START([START]) --> INPUT[/IN x<br>IN y/]
    INPUT --> COND{"x > 0"}
    COND -- V --> MULT[m = x * y]
    COND -- F --> OUT_Y[/OUT y/]
    MULT --> OUT_M[/OUT m/]
    OUT_M --> STOP([STOP])
    OUT_Y --> STOP

```

### Esercizio 7: Controllo Pari o Dispari

Dato in ingresso un valore che deve essere diverso da 0, l'algoritmo restituisce se tale numero è pari o dispari.

* **Dati di input:** un valore x
* **Dati di output:** messaggio "Pari" o "Dispari"

```mermaid
graph TD
    START([START]) --> INPUT[/IN x/]
    INPUT --> CHK{"x == 0"}
    CHK -- V --> ERR[/OUT "Inserisci un numero != da 0"/]
    ERR --> INPUT
    CHK -- F --> COND{"x % 2 == 0"}
    COND -- V --> PARI[/OUT "Pari"/]
    COND -- F --> DISPARI[/OUT "Dispari"/]
    PARI --> STOP([STOP])
    DISPARI --> STOP

```

---

### Esercizio 8: Somma Valori Esclusivamente Positivi

Dati in ingresso due valori qualsiasi, l'algoritmo fornisce in output i valori sommati solo se entrambi sono maggiori di 0, altrimenti segnala errore.

* **Dati di input:** X, Y
* **Dati di output:** Somma o messaggio "Errore"

```mermaid
graph TD
    START([START]) --> INPUT[/IN X<br>IN Y/]
    INPUT --> COND{"X > 0 AND Y > 0"}
    COND -- V --> PROCESS[S = X + Y]
    COND -- F --> ERR[/OUT "Errore"/]
    PROCESS --> OUT_S[/OUT S/]
    ERR --> INPUT
    OUT_S --> STOP([STOP])

```

### Esercizio 9: Somma Selettiva dei Valori Pari

Dati in ingresso due valori, l'algoritmo analizza i singoli elementi inseriti e ne accumula il valore solo se si tratta di numeri pari.

* **Dati di input:** X, Y
* **Dati di output:** Somma totale dei valori pari S

```mermaid
graph TD
    START([START]) --> INPUT[/IN X<br>IN Y/]
    INPUT --> INIT[S = 0]
    INIT --> CHK_X{"X % 2 == 0"}
    CHK_X -- V --> ADD_X[S = S + X]
    CHK_X -- F --> CHK_Y{"Y % 2 == 0"}
    ADD_X --> CHK_Y
    CHK_Y -- V --> ADD_Y[S = S + Y]
    CHK_Y -- F --> OUTPUT[/OUT S/]
    ADD_Y --> OUTPUT
    OUTPUT --> STOP([STOP])

```

---

### Esercizio 10: Output Esclusivo di Valori Dispari

Dati in ingresso due valori, l'algoritmo esegue un controllo di disparità e fornisce in output solo i valori che risultano dispari.

* **Dati di input:** due valori (x, y)
* **Dati di output:** i singoli valori dispari identificati

```mermaid
graph TD
    START([START]) --> INPUT[/IN x<br>IN y/]
    INPUT --> CHK_X{"x % 2 == 1"}
    CHK_X -- V --> OUT_X[/OUT x/]
    CHK_X -- F --> CHK_Y{"y % 2 == 1"}
    OUT_X --> CHK_Y
    CHK_Y -- V --> OUT_Y[/OUT y/]
    CHK_Y -- F --> STOP([STOP])
    OUT_Y --> STOP

```

### Esercizio 11: Calcolo Somma dei Valori Dispari

Dati in ingresso due valori, l'algoritmo effettua una verifica e restituisce la somma cumulativa dei soli valori inseriti che risultano dispari.

* **Dati di input:** due valori (x, y)
* **Dati di output:** la somma dei valori dispari sd

```mermaid
graph TD
    START([START]) --> INPUT[/IN x<br>IN y/]
    INPUT --> INIT[sd = 0]
    INIT --> CHK_X{"x % 2 == 1"}
    CHK_X -- V --> ADD_X[sd = sd + x]
    CHK_X -- F --> CHK_Y{"y % 2 == 1"}
    ADD_X --> CHK_Y
    CHK_Y -- V --> ADD_Y[sd = sd + y]
    CHK_Y -- F --> OUTPUT[/OUT sd/]
    ADD_Y --> OUTPUT
    OUTPUT --> STOP([STOP])

```

---

### Esercizio 12: Il Maggiore tra Tre Numeri

Dati tre numeri in ingresso, l'algoritmo analizza le relazioni d'ordine tramite condizioni logiche e fornisce in output il valore massimo.

* **Dati di input:** tre valori (x, y, z)
* **Dati di output:** il valore massimo max

```mermaid
graph TD
    START([START]) --> INPUT[/IN X<br>IN Y<br>IN Z/]
    INPUT --> COND1{"X > Y AND X > Z"}
    COND1 -- V --> OUT_X[/OUT X/]
    COND1 -- F --> COND2{"Y > X AND Y > Z"}
    COND2 -- V --> OUT_Y[/OUT Y/]
    COND2 -- F --> COND3{"Z > X AND Z > Y"}
    COND3 -- V --> OUT_Z[/OUT Z/]
    COND3 -- F --> STOP([STOP])
    OUT_X --> STOP
    OUT_Y --> STOP
    OUT_Z --> STOP

```

### Esercizio 13: Somma dei Numeri Pari Maggiori di Zero

Dati tre numeri, l'algoritmo verifica per ciascuno se rispetta contemporaneamente la condizione di essere maggiore di zero e un numero pari, calcolandone e restituendone la somma cumulativa.

* **Dati di input:** tre numeri
* **Dati di output:** la somma dei numeri conformi alle specifiche

```mermaid
graph TD
    START([START]) --> INPUT[/IN X<br>IN Y<br>IN Z/]
    INPUT --> INIT[S = 0]
    INIT --> CHK_X{"X > 0 AND X % 2 == 0"}
    CHK_X -- V --> ADD_X[S = S + X]
    CHK_X -- F --> CHK_Y{"Y > 0 AND Y % 2 == 0"}
    ADD_X --> CHK_Y
    CHK_Y -- V --> ADD_Y[S = S + Y]
    CHK_Y -- F --> CHK_Z{"Z > 0 AND Z % 2 == 0"}
    ADD_Y --> CHK_Z
    CHK_Z -- V --> ADD_Z[S = S + Z]
    CHK_Z -- F --> OUTPUT[/OUT S/]
    ADD_Z --> OUTPUT
    OUTPUT --> STOP([STOP])

```

---

## SEZIONE 2 - Strutture Iterattive

### Esercizio 1: Iterazione Numeri da 0 a 3

Esempio base di applicazione di un ciclo definito tramite una variabile contatore per inviare in output i numeri in sequenza da 0 a 3 compreso.

* **Dati di input:** nessuno
* **Dati di output:** i singoli numeri da 0 a 3

```mermaid
graph TD
    START([START]) --> INIT[i = 0]
    INIT --> COND{"i <= 3"}
    COND -- V --> OUTPUT[/OUT i/]
    OUTPUT --> INC[i = i + 1]
    INC --> COND
    COND -- F --> STOP([STOP])

```

### Esercizio 2: Output Numeri Pari da 0 a 5

L'algoritmo esegue un ciclo da 0 a 5 integrando un controllo interno per individuare e stampare in output esclusivamente i valori pari incontrati durante l'iterazione.

* **Dati di input:** nessuno
* **Dati di output:** i numeri pari compresi nell'intervallo esaminato

```mermaid
graph TD
    START([START]) --> INIT[i = 0]
    INIT --> COND{"i <= 5"}
    COND -- V --> CHK{"i % 2 == 0"}
    CHK -- V --> OUTPUT[/OUT i/]
    CHK -- F --> INC[i = i + 1]
    OUTPUT --> INC
    INC --> COND
    COND -- F --> STOP([STOP])

```

---

### Esercizio 3: Somma Progressiva dei Numeri da 0 a 10

L'algoritmo esegue un ciclo iterativo per calcolare e restituire la somma cumulativa di tutti i numeri interi compresi nell'intervallo tra 0 e 10.

* **Dati di input:** nessuno
* **Dati di output:** la somma complessiva s

```mermaid
graph TD
    START([START]) --> INIT["i = 0<br>s = 0"]
    INIT --> COND{"i <= 10"}
    COND -- V --> PROCESS[s = s + i]
    PROCESS --> INC[i = i + 1]
    INC --> COND
    COND -- F --> OUTPUT[/OUT s/]
    OUTPUT --> STOP([STOP])

```

### Esercizio 4: Somma dei Numeri Dispari da 5 a 15

L'algoritmo esegue un conteggio ciclico a partire dal valore iniziale 5 fino al limite 15, verificando la disparità di ogni elemento e accumulandone il valore della somma.

* **Dati di input:** nessuno
* **Dati di output:** la somma finale dei numeri dispari sd

```mermaid
graph TD
    START([START]) --> INIT["i = 5<br>sd = 0"]
    INIT --> COND{"i <= 15"}
    COND -- V --> CHK{"i % 2 == 1"}
    CHK -- V --> PROCESS[sd = sd + i]
    CHK -- F --> INC[i = i + 1]
    PROCESS --> INC
    INC --> COND
    COND -- F --> OUTPUT[/OUT sd/]
    OUTPUT --> STOP([STOP])

```

---

### Esercizio 5: Somma Iterativa Fino a un Limite x Definito dall'Utente

Dato un numero positivo in ingresso, l'algoritmo esegue un ciclo per calcolare e stampare in output la somma di tutti i valori compresi tra 0 e quel numero. Include un ciclo di validazione iniziale (ciclo while) per garantire la positività dell'input.

* **Dati di input:** un valore x
* **Dati di output:** la somma progressiva calcolata s

```mermaid
graph TD
    START([START]) --> INPUT[/IN x/]
    INPUT --> CHK{"x < 0"}
    CHK -- V --> ERR[/OUT "Inserisci un numero positivo"/]
    ERR --> INPUT
    CHK -- F --> INIT["i = 0<br>s = 0"]
    INIT --> COND{"i <= x"}
    COND -- V --> PROCESS[s = s + i]
    PROCESS --> INC[i = i + 1]
    INC --> COND
    COND -- F --> OUTPUT[/OUT s/]
    OUTPUT --> STOP([STOP])

```

---

## SEZIONE 3 - Ripasso Generale

### Esercizio 1: Algoritmo Sequenziale Puro

Esempio di struttura lineare in sequenza che riceve due valori in ingresso, calcola contemporaneamente la loro somma e la loro moltiplicazione, emettendo entrambi i risultati in output.

* **Dati di input:** due valori (x, y)
* **Dati di output:** somma (s) e moltiplicazione (m)

```mermaid
graph LR
    START([START]) --> INPUT[/IN x<br>IN y/]
    INPUT --> PROCESS["s = x + y<br>m = x * y"]
    PROCESS --> OUTPUT[/OUT s<br>OUT m/]
    OUTPUT --> STOP([STOP])

```

### Esercizio 2: Algoritmo di Selezione Condizionale

Struttura a selezione condizionale che valuta il valore di un'età inserita in ingresso per stabilire e comunicare testualmente se la persona è maggiorenne o minorenne.

* **Dati di input:** età
* **Dati di output:** stringa di messaggio "Maggiorenne" o "Minorenne"

```mermaid
graph TD
    START([START]) --> INPUT[/IN età/]
    INPUT --> COND{"età >= 18"}
    COND -- V --> OUT_MAG[/OUT "Maggiorenne"/]
    COND -- F --> OUT_MIN[/OUT "Minorenne"/]
    OUT_MAG --> STOP([STOP])
    OUT_MIN --> STOP

```

### Esercizio 3: Algoritmo di Ciclo Definito (Tabellina)

Dato un numero x inserito in input, l'algoritmo calcola e restituisce in sequenza i valori della corrispondente tabellina moltiplicando l'input per un contatore che si incrementa da 0 a 10.

* **Dati di input:** un numero x
* **Dati di output:** i singoli valori calcolati della tabellina t

```mermaid
graph TD
    START([START]) --> INPUT[/IN x/]
    INPUT --> INIT[i = 0]
    INIT --> COND{"i <= 10"}
    COND -- V --> PROCESS[t = x * i]
    PROCESS --> OUTPUT[/OUT t/]
    OUTPUT --> INC[i = i + 1]
    INC --> COND
    COND -- F --> STOP([STOP])

```

### Esercizio 4: Algoritmo di Ciclo Indefinito (Somma ad Oltranza)

L'algoritmo riceve e somma numeri inseriti dall'utente in modo indefinita fino a quando la somma progressiva calcolata supera il valore limite di 100, mostrando poi il risultato finale della somma.

* **Dati di input:** una serie indefinita di valori inseriti x
* **Dati di output:** la somma complessiva finale s

```mermaid
graph TD
    START([START]) --> INIT[s = 0]
    INIT --> INPUT[/in x/]
    INPUT --> PROCESS[s = s + x]
    PROCESS --> COND{"s <= 100"}
    COND -- V --> INPUT
    COND -- F --> OUTPUT[/out s/]
    OUTPUT --> STOP([STOP])

```

```

```
