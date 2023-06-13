# Database
- ## Definizione
    - Collezione di informazioni che vengono memorizzati in un computer. Per lavorare con il database si usa il **DBMS**
    - **DBMS**
        - Database Management Systems
        - Software che ci permette di lavorare con il database. Le applicazioni che devono lavorare con il database (Amazon per rimuovere un prodotto perché è stato già comprato), deve interagire con il DBMS
        - Le operazioni che fa il DBMS sono 4 (C.R.U.D)
            - Creare, aggiungere informazioni
            - Leggere le informazioni
            - Aggiornare informazioni
            - eleminare le informazioni

- ## Relazionali (SQL)
    - I database relazionali organizzano i dati in delle tabelle: ci sono **righe** e **colonne**
    - Ogni campo rappresenta un campo e una riga rappresenta un record.
    - Per lavorare con questi database, si usa SQL

    - ### SQL
        - Structured Query Language
        - E' un linguaggio che è usato per manipolare i database relazionali (interroganodolo e modificarlo) 
        - Ci sono 4 operazioni fondamentali che ci consente di fare:
            - **SELECT**: ottenere delle informazioni
            - **INSERT**: inserire delle informazioni
            - **UPDATE**: aggiornare delle informazioni
            - **DELETE**: eliminare delle informazioni

    - Alcuni famosi sistemi databse SQL:
        - Oracle
        - MySQL

- il **No** sta per **Not Only**
- ## Non relazionali (NoSQL)
    - Sono tutti i database che non usano le tabelle tradizionali (divisi con colonne e righe) per salvare i dati ma usano altri modelli come:
        - **Key-Value**: salvare le informazioni sotto-forma di una coppia chiave-valore: 
            - chiave è l'indice, usato per accedere al contenuto 
            - valore è il contenuto
        - **Document**: Memorizza le informazioni sotto-forma documento dove le informazioni vengono rappresentati generalmente in JSON (**MongoDB** è un esempio) 
        - **Grafo**: modello composto dai nodi (informazioni) e per creare delle relazioni si usano degli archi

- ## Differenze tra i due
    - **NoSQL** è più flessibile del **SQL** perché ci sono più modelli che posso utilizzare per rappresentare i dati 

    - **NoSQL** generalmente è più veloce perché rappresentare i dati sotto-forma di tabella non sempre è la scelta più efficiente 
    - es: social network dove dobbiamo salvare utenti, chi è amico di chi, i commenti $\to$ tante connessioni tra i dati $\to$ usando **SQL** le query potrebbe diventare lento perché è strutturato come tabella. Se si rappresenta come grafo è molto più comodo $\to$ un esempio magari è cercare il percorso più breve tra due utenti (suggerire degli utenti come possibile futuro amico $\to$ i nodi sono gli utenti, e l'arco è per indicare che c'è un'amicizia tra due utenti. Devo trovare l'utente più vicino possibile (magari l'amico dell'amico))

    - La sintassi dei linguaggi **SQL** sono molto simili mentre in **NoSQL** non c'è un modello universale


    - **SQL** supporta query più complesse e consente il **JOIN**