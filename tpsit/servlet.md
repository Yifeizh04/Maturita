# Servlet

- ## Definizione
    - Servlet sono degli oggetti Java che vengono utilizzati dai web server quindi dalle applicazioni web.
    
- Il server web offre a questi oggetti un ambiente di esecuzione chiamato **container**.

- ## Container
    - Un servlet container è un componente del server web che si occupa:
        - **sessioni** 
        - **sicurezza** 
        - **controllo degli accessi** e **la gestione delle risorse**

        - **ciclo di vita del servlet**:   
            - $caricamento$
            - $inizializzazione$
                - Avviene con metodo init():
                    - inizializzare le variabili globali 
                    - viene invocato una volta
            - $esecuzione$
                - Avviene metodo service():
                    - gestire le richieste ed elaborlarle
                    - viene invocato ad ogni richiesta del client
            - $distruzione$
                - Avviene metodo destroy() 
                    - rilascia le risorse allocate dalla servlet

- Quando un client invia una richiesta HTTP a un web server che supporta le Servlet, il container riceverà la richiesta e deciderà a quale servlet deve essere eseguito per gestirla

- ## Funzionamento comunicazione client e servlet
    - Il servlet **incapsula le richieste HTTP** in una classe $HttpServletRequest$ e la passa nel metodo $doPost$ e $doGet$
        - **doGet** risponde alle richieste GET
        - **doPost** risponde alle richieste POST
    - Per accedere alle variabili che sono state mandate, si usa il metodo getParameter dell'oggetto ServletRequest e si passa il nome della variabile
    - Per rispondere si salva la risposta nella $HttpServletResponse$ che viene mandata al client dal web server via HTTP

    
- Possiamo ottenere una cosa equivalente ai Servlet usando il JSP

- ## JSP:    
    - **Java Server Page**
    - E' una teconlogia che ci consente di includere codice java all'interno di un codice HTML
    - Anche le JSP sono eseguiti all'interno di un container infatti quest'ultimo ha lo scopo di tradurre il JSP in servlet
    - Possiamo includere il JSP in un codice HTML utilizzando dei TAG come in PHP
    
- ## Differenze tra Servlet e JSP :
    - **JSP:**
        - veloce da implementare e più facile la manutenzione  $\to$ ci consente di separare la parte grafica (codice html) dalla parte logica/elaborazione (in Java)
        - Nel servlet non c'è questa cosa visto che per stampare dell'html bisogna invocare dei metodi della servlet 
    
    - **Servlet:**
        - E' più efficiente visto che il JSP viene tradotto in Servlet e quindi per avere più efficienza, conviene scrivere direttamente in Servlet
