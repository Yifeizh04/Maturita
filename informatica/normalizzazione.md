# Normalizzazione 

- ## Cos'è?
    - Tecnica che riduce la ridondanza dei dati [^1] e cercando di eliminare le possibili anomalie causate dalle operazioni di $insert$, $update$ e $delete$. Ci sono varie forme che sono un insieme di regole / condizioni, in particolare c'è ne sono 6 ma nella pratica vengono solo utilizzate i primi 3.

    - ## Anomalie:

- ## 3 forme normali
    - ## I forma
        - Ogni valore deve essere ***atomico*** 
            - ES: 
        - Ogni record deve essere univoco
            - Per identificare un record nella tabella in maniera univoca, si usa un valore chiamato ***KEY***- Esso è una colonna (***PRIMARY KEY***) o una combinazione di colonne (***COMPOSITE KEY***)

            - Caratteristica della chiave:
                - Non può essere NULL
                - Deve essere UNIQUE 
                - Deve essere raramente (meglio mai) cambiato
    
    - ## II forma
        - Bisogna essere già nella I forma
        - Le 

- https://www.guru99.com/database-normalization.html
- https://www.javatpoint.com/anomalies-in-dbms

[^1]: dividere la tabella più grande in più piccoli e collegarli usando delle relazioni