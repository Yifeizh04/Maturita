# Normalizzazione 

- ## Cos'è?
    - Tecnica che riduce la ridondanza dei dati [^1] e cercando di eliminare le possibili anomalie causate dalle operazioni di $insert$, $update$ e $delete$. Le tabelle normalizzate sono più facili da capire, elaborare (estenderla, migliorarla). [^2] Ci sono varie forme che sono un insieme di regole / condizioni che ci permettono di capire se una tabella è normalizzata, in particolare c'è ne sono 6 ma nella pratica vengono solo utilizzate i primi 3. Meno è il livello, meno è """sicuro""". 

    - ## Anomalie:
        - insert:
            - Inserisco dei dati incompleti (es: senza chiave) nei campi che mi richiedono 
        - update:
            - Ho una tabella dove ci sono più di 1 entry di Mario rossi e supponiamo di aggiornare la sua residenza. Se aggiorno, devo aggiornare tutte le entry di Mario Rossi ma se per qualche motivo non dovessi aggiornare un entry, io ho un incosistenza ovvero ho che Mario Rossi ha due residenze (perché una entry non è stata aggiornata) e quindi è un'anomalia
        - delete:
            - E' una anomalia quando eliminando un certo entry, non intenzionalemnte elimino dei dati
            - ES: ho una entry ("Mario Rossi", "Pergine") e suppongo che solo lui abita a Pergine. Eliminando Mario Rossi, elimino anche Pergine e quindi perdo l'informazione di Pergine (per fixare sarebbe da separare Pergine in un'altra tabella e collegarmi con l'id).

- ## 3 forme normali
    - ## I forma
        - Ogni valore deve essere ***atomico*** 
            - Il vantaggio di avere valori atomici è quello di non avere dei campi con tanti valori perché sono poco leggibili e sono poco performanti:
            - ES: c'è un campo dove viene salvato "nome, cognome, altezza, data", intanto è poco leggibile perché ho tante informazioni in un campo e magari a me interessa solo un speficifico campo. Se devo cercare chi è nato in una certa data o voglio avere la lista sortata per altezza, dovrei fare uno "split" per ottenere l'informazione. Alla fine è sempre meglio scomporre così da essere più leggibile e anche più performante
        - **Ogni record deve essere univoco**
            - Per identificare un record nella tabella in maniera univoca, si usa un valore chiamato ***KEY***- Esso è una colonna (***PRIMARY KEY***) o una combinazione di colonne (***COMPOSITE KEY***)

            - Caratteristica della chiave:
                - Non può essere NULL
                - Deve essere UNIQUE 
                - Deve essere raramente (meglio mai) cambiato
    
    - ## II forma
        - **Bisogna essere già nella I forma**
        - **I campi non chiave devono dipendere dalla chiave**
        - ES:
            - Tabella KEY(Giocatore e Tipo oggetto) e non chiave (Quantita_oggetto, punteggio)
            - Quantita_oggetto dipende completamente da giocatore e tipo oggetto mentre punteggio dipende solo da giocatore $\to$ dividere la tabella in due tabelle giocatori (così che il punteggio sia legato solo al giocatore) e giocatore_oggetto
    
    - ## III forma
        - **Bisogna essere già nella II forma**
        - **Nessun attributo non chiave, deve dipendere transitivamente da campi non chiave** [^3]
        - ES:
            - Abbiamo la tabella giocatore KEY(nome) e non chiave (livello e grado)
            - Esistono 3 livelli (base, medio e avanzato) e il grado varia in base al livello (base $\in [1, 4]$, medio $\in [5, 8]$, avanzato $\in [9, 10]$)
            - In questo caso il livello dipende transitivamente da grado (se cambia il grado, devo anche aggiornare il livello e viceversa)
            - Se io aggiorno il grado da $4$ a $8$ perchè uno diventa molto bravo, dovrei cambiare anche il livello da $base$ a $medio$ e se ciò non avviene, ho un incosistenza. 
            - Per fixare:
                - Spezzo la tabella dove uno ha (nome_giocatore e grado), l'altro che fa da tabella di traduzione (grado, livello) dove ogni grado viene tradotto con livello


[^1]: dividere la tabella più grande in più piccoli e collegarli usando delle relazioni
[^2]: possiamo vedere queste regole come quando si va a creare un'opera di ingegneria (es: creare una casa). Prima si crea una base e ci sono delle regole per capire se una base è fatta bene o no, poi si crea le mura (ci saranno altre regole) e poi il tetto
[^3]: ogni attributo non chiave dipende solo e soltano dalla chiave 