# Socket
- ## Definizione
    - Punto finale di una connessione di rete bidirezionale. E' un oggetto che rappresenta la connessione tra due computer
- ## Caratteristiche:
    - Composto da **IP** che identifica il PC nella rete, e dal numero **porta** che identifica l'applicazione che è in esecuzione su quel computer

- ## Utilizzo:
    - Generalmente viene utilizzato un'architettura **client-server** dove si deve creare una connessione tra due computer:
        - server usufruisce dei servizi ai client o soddisfa le richieste fatte da quest'ultimi
        - client richiede un servizio o dei dati dal server

    - Vengono utilizzati nel TCP e nell'UDP 

- ## Implementazioni del TCP:
    - In Java si usa la classe "java.net.Socket"
    - Prima si esegue il Server e poi si esegue i client
    - Si istanzia il server con un oggetto SocketServer passando IP e porta
    - Poi si crea un oggetto Socket di cui invochiamo il metodo serverSocket.accept() per accettare le richieste dei client che vogliono comunicare
    - Il client deve conoscere l'IP e porta del server  
    - Per comunicare entrambi usano un BufferReader per leggere e DataOutputStream per stampare


- ## Implementazioni del UDP:
    - In Java si usa la classe "java.net.DataGramSocket"
    - L'implementazione è uguale (per entrambi) solo che l'ordine cambia (prima client scrive, e poi sarà il server)
    - Per comunicare entrambi istanziano un DatagramSocket e per inviare usano un DatagramPacket. Quando si manda il messaggio, si inserisce il contenuto e l'IP + porta del destinatario. Colui che lo riceve, è in grado di ricavare l'IP e porta di colui che ha mandato 
    - riceive (per fare get) e send (inviare)

    - Tramite UDP si può implementare multicast:
        - Il socket è un oggetto MulticastSocket 
        - ho un ip di gruppo ed entrano in questo gruppo facendo il join 
        - il modo di comunicare è lo stesso dell'UDP 
