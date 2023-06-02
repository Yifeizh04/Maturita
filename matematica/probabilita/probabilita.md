# Probabilita

- ## Definizione classica:
    - Definiamo $E$ l'evento da controllare, e $F$ i casi favorevoli, e $T$ i casi totali 
    - $P(E) = \frac{F}{T}$
    - La probabilità inversa $P(E') = 1 - P(E)$. 
    - **Spazio campionario $\Omega$**
        - insieme dei possibili risultati di un esperimento casuale (es: lancio del dado)
    - **Evento:**
        - **Insieme formato da tutti, nessuno o alcuni possibili esiti di un esperimento casuale**
        - Due eventi possono essere:
            - **compatibili o incompatibili** (possono avvenire assieme o no)
                - Siano due eventi $A$ e $B$ diversi tra loro allora:    
                - $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
                - Notare che $P(A \cap B) = 0$ se $A$ e $B$ sono incompatibili
            - **indipendenti o dipendenti** (se l'avvenire del primo evento altera o meno la probabilità che accada il secondo).

                - Si chiama probabilità condizionata $P(E2)$ se $E2$ dipende da $E1$ e si scrive $P(E2|E1)$ dove sappiamo che $E1$ è già accaduto e influenza $E2$ 

                - ### Teorema Bayes
                    - Abbiamo 2 casi A, B dove per ognuno di queste puo' essere C o D
                    - Sappiamo che è $C$, qual'è la probabilità che sia A
                    - $P(A | C) = \frac{P(A) * P(C | A)}{P(A) * P(C | A) + P(B) * P(C | B)}$


- ### Frequenza relativa:
    - $F = \frac{X}{N}$ dove $F$ è la frequenza relativa, $N$ il numero volte in cui si ripete l'esperimento e $X$ è quante volte l'evento $E$ si è avverato

- ### Legge dei grandi numeri
    - Più si fanno esperimenti ($N$ grande), più la frequenza relativa $F$ tende a $P(E)$

- ### Probabilità soggettiva:
    - misura del grado di fiducia che una persona attribuisce al verificarsi di un evento secondo la sua opinione: $P(E) = S / V$ dove $S$ quanto è disposto pagare e $V$ quanto riceverà se l'evento avviene 


- ### Nota
    - Perché dobbiamo definire più definizioni? A priori non si riesce a calcolare la probabilità e quindi lo faccio più volte l'evento. 
    - ES: 
        - Io contro 20 persone al tiro della fune $\to$ casi totali: 2 (vinco io o vincono loro). Casi favorevoli: 1.
        La probabilità dovrebbe essere $\frac{1}{2}$ che realmente è sbagliata. 


- ### Schema Bernulli:
    - usato per le prove ripetute
    - Sia $p$ la probabilità che avvenga l'evento $E$ e $K$ il numero di successi in $N$ prove allora:
    - $P(E) = \binom{N}{K} * p^k * (1 - p)^{n - k}$

