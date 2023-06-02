# Combinatoria

- ## Definizione: 
    - branca della matematica che si occupa dello studio dei metodi per ***raggruppare un numero finito di elementi*** per poi ***contare il numero di possibili raggruppamenti degli elementi*** 

- ### Fattoriale:
    - Prodotto di tutti i numeri interi positivi $\le n$ 
        - $n! = n * (n - 1) * (n - 2) * ... * 1 $

- ## Metodi:
    
    - ## Permutazione:
        - Una permutazione di $N$ elementi che si indica con $P_{n}$ sono tutti i possibili raggruppamenti dove ogni raggruppamento:
            - contiene tutti gli $N$ elementi
            - ogni raggruppamento differisce da un'altro per ordine in cui vengono scelti
        - Esistono due tipi di permutazioni:
            - ***semplici***
                - modi possibili di ordinare $N$ elementi distinti 
                - $P_{n} = n!$
            - ***con ripetizione***
                - possibili modi di riordinare $N$ elementi dove alcuni elementi si possono ripetere più volte
                - Sia $f_{1}, f_{2}...f_{z}$ le frequenze con cui compare un certo elemento ($z$ = #{elementi distinti}), questo calcolo si fa:
                - ${P'_{n}}^{f_{1}, f_{2}...f_{z}} = \frac{n!}{f_{1}! * f_{2}! * ... * f_{z}!}$ 
                - Esempio: Anagrammi con lettere che si ripetono 

    - ## Disposizione:
        - Sequenza ordinata di $K$ elementi selezionati tra $N$ elementi. Notare che se K = N, diventa una permutazione perché prendiamo tutto l'insieme.
        - ***L'ordine in cui vengono scelte conta***

        - Esistono 2 tipi:
            - ***Disposizioni semplici / senza ripetizione:***
                - Una volta scelto l'elemento, non puo' essere piu' scelto
                - $D_{n, k} = \frac{n!}{(n - k)!}$
                - Esempio: classifica di una materia
            - ***Disposizioni con  ripetizione:***
                - Un elemento può essere scelto anche più volte
                - $D'_{n, k} = n^{k}$
                - Stilare classifica però più materie (una persona può uscire più volte)

    - ## Combinazioni:
        - Sono delle disposizioni ma l'ordine non è più importante. Si risolveno con il coefficiente binomiale

        - ### Coefficiente binomiale:
            - Dato due numeri $N$ e $K$ si definisce coefficiente binomiale di $N$ su $K$ come: $\binom{N}{K} = \frac{N!}{(N - K)! * K!}$
            - Consente di trovare il **numero di modi** in cui $K$ elementi distinti possono essere scelti tra $N$ numeri, indipendentemente dall'ordine $\to$ numero di **sottoinsiemi** di $K$ elementi che si possono estrarre in un insieme di $N$ elementi

            - Viene usato per calcolare il **binomio di Newton** $\to$ fare $(a - b)^n$
                - $\sum_{i=0}^{k}  \binom{n}{i} * a ^ {n-k} * b^{K}$ 

            - Proprietà (principali):
                - $\binom{N}{K} = 1$ con $K = 0$ o $K = N$ [^1]

                - $\binom{N}{K} = \binom{N}{N - K}$ 
                    - proof: Dimostrare $\frac{N!}{K! * (N - K)!} = \frac{N!}{(N - K)! * (N - (N - K))!}$
                    - Ma il denominatore a destra diventa $N - N + K = K$ dimostrando l'uguaglianza





[^1]: Per prendere 0 elementi ho 1 maniera ovvero non prendere niente e stessa cosa K=N, l'unica maniera è prenderli tutti
        
[^2]: 