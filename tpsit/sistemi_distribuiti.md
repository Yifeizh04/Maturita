# Sistemi distribuiti 

- ## **Sistemi centralizzati:**
    - applicazioni che girano su 1 $ host/processore$ (dati risiedono solo su esso)
- ## ***Sistema distribuito:***
    - ## **Definizione**
    - insieme di **applicazione logicamente indipendenti** che collaborano tra di loro per compiere un obbiettivo in comune attraverso un **infrastruttura** hardware/sofware
    - deve verificarsi almeno una delle $2$ condizioni:
        - **elaborazione distribuita:** applicazione che risiede su più host che collaborano tra loro
        - **base dati distribuiti:** informazioni risiedono su più host

- ## **Ruoli applicazioni**
    - ***CLIENT:*** utilizzatore servizi messi a disposizione da altre applicazioni
    - ***SERVER:*** fornitore servizi che vengono utilizzate da altre applicazioni
    - ***ACTOR:*** applicazioni che in certi momenti fanno da client e in altri da server

- ## ***Vantaggi***
    - ***Affidabilità***:
        - se HOST A muore, il servizio non si blocca ma c'è un'altro HOST che sostituisce HOST A (intanto lo si ripara)
    - ***Integrazione***:
        - si possono integrare dispositivi (solitamente $eterogenee$ per HARDWARE [^1] e per S.O). Potendo aggiungere, prestazioni migliorano perché si può supportare un carico maggiore richieste.
        - Risolve il problema che sistema centralizzato ha risorsa limitata, qui è "$infinita$", se ci consente di espandere
        - Per favorire la comunicazione tra essi (per la question eterogenee), sono stati creati linguaggi come **XML** e notazioni **JSON**
        - **Cenni veloci su XML e JSON**
            - ***XML***:
                - **eXtensible Markup Language**
                - E' un linguaggio markup, leggibile per gli essere umani e macchine e usa i tag. E' molto flessibile e viene utilizzato per memorizzazione e scambi di dati strutturati/complessi
            - ***JSON***:
                - **JavaScript Object Notation**
                - E' un linguaggio basato javascript, comprensibile per gli umani e macchine e usa i tag. I dati vengono rappresentati sotto una forma di **chiave valore (simile mappa)**.
            
            - **Quando usare uno o l'altro?**
                - XML essendo più flessibile, conviene usarlo se ci sono strutture dati complesse 
                - JSON è più leggero e semplice da utilizzare e vengono utilizzati generalmente nelle applicazioni WEB
    
    - ***Economicità***:
        - generalmente è più economico rispetto a un sistema centralizzato
        - se voglio raggiungere potenza X, con 1 PC spendo 10k, se ne compro tante ma meno potenti sicuramente spendo di meno (forse è più veloce). Anche ripararlo costa meno (e pure più facile trovare i pezzi)

    - ***Trasparenza***:
        - vedere il sistema come un unico SISTEMA di ELABORAZIONE e non come un insieme di componenti
        - TIPI:
            - **ACCESSO:** 
                - La modalità d'accesso alle risorse deve essere lo stesso per tutti 
            - **LOCAZIONE:**
                - Nascondere localizzazione della risorsa ${\to}$ non dobbiamo conoscere ***IP*** o ***URL*** della risorsa
            - **CONCORRENZA:**
                - se i processi lavorano in maniera concorrente sulla RISORSA, quest'ultima deve essere in uno stato CONSISTENTE applicando tecniche come **semafori Dijktra**
            - **REPLICAZIONE:**
                - gli utenti non si devono accorgere che stiamo duplicando dati (aumentare affidabilità)
            - **GUASTI:**
                - l'utente non deve accorgersi del GUASTO e della RECOVERY della risorsa ${\to}$ servizio continua, al massimo è più lento rispondere (GUASTO PARZIALE). Due modi per attuare questa strategia:
                    - 1. Creare una ***macchina gemella***: uguale identica, ma costa di più però più efficiente
                    - 2. salvarsi le varie versioni così da poterli ripristinare (simile Git) (più lento, ma economico)


- ## ***Svantaggi***
    - **Complessità**:
        - è più difficile da mantenere visto che ci sono tante tecnologie di diverso tipo e quindi tecnico deve avere una competenza approfondito su tutto
    - **Sicurezza**:
        - Visto che i dispositivi si devono comunicare tra loro (via internet???) ci possono essere problemi (Man in the middle)




[^1]: tablet, computer, telefono

