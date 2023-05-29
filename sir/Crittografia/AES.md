# AES

- ## Infomrmazioni base

    - **Advanced Encryption Standard**
    - Nasce nel 2001 per sostituire il DES, ormai divenuto obsoleto per le potenze di calcolo dei pc. Creano una sfida posta ai matematici di creare un nuovo algoritmo ed è stato vinto da Joan e Vincent (Belgio) 

    - E' l'algoritmo più utilizzato ora ed è simmetrico

    - Esistono 3 versioni (il numero dice lunghezza chiave):
        - AES-128
        - AES-192
        - AES-256
    
    - Più è lungo la chiave, più è sicuro (ma sarà più lento)

- ## Funzionamento
    - Sia ha un messaggio $M$, e una chiave $K$. 
    - Ogni carattere lo converto in $HEX$ [^1] e divido il messaggio in blocchi grandi 4*4

    - Fatto ciò eseguo per ogni blocco, eseguo $X$ [^2] volte questo processo/round:
        - ***SubBytes***
            - Si ha un $SBOX$ grande $16*16$ $(0 - f)$. Lo scopo è trasformare un $HEX$ in un'altro. Per ogni $HEX$ del blocco, la prima lettera indica la riga, la seconda per la colonna (es: 0a --> riga 0 e 10 colonna). Lo facciamo per ogni $HEX$ del blocco
        - ***ShiftRows***
            - Per ogni riga i (partendo da 0), sposto il pezzo in cima di ogni riga infondo e lo faccio i volte.
            - **ES:**
                - i = 2:
                - stato iniziale: d4 e0 b8 1a
                - shift 1:
                    - e0 b8 1a $d4$
                - shift 2: 
                    - b8 1a d4 $e0$
        - ***MixColumns***:
            - Questo step non viene fatto nell'ultimo round
            - Si ha un'altra matrice e per ogni colonna i, si fa il **dot-product** con la riga i:
            - **ES:**
                - matrice:
                    ```
                    01 02 02 01  
                    01 12 02 01
                    01 30 00 01
                    41 12 11 01
                    ```
                - blocco:
                    ```
                    aa ba 10 12  
                    01 12 02 01
                    01 30 00 01
                    41 12 11 01
                    ```
                
                - Per calcolare l'elemento in [0][2] (si prende la riga 0 della matrice e la colonna 2 del blocco):
                    ```
                    [01 02 02 01] * 
                    [ba 12 30 12]
                    // sta cosa si fa con dello shift e XOR (roba complicata) 
                    ```
        - ***AddRoundKey***
            - Prendo una sotto-chiave $K$ (diversa per ogni round), e faccio la $XOR$ con il blocco trasformato 


[^1]: ogni carattere posso trasformare in ASCII (byte), e posso dividere l'ASCII in due pezzi da 4 bit --> HEX visto che l'HEX è base 16 (0000 a 1111)

[^2]: X varia in base alla lunghezza della chiave
