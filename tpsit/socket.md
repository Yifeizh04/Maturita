# Socket
- ## Mini introduzione:
    - Quando siamo in una struttura client server, il client sta usufruendo dei servizi che si basano su certi protocolli come HTTP, che generalmente lavorano nel 4 livello della pila ISO/OSI e quindi si basano sul TCP e UDP che si possono implementare tramite i socket.
- ## Definizione
    - Punto finale di una connessione di rete bidirezionale. E' un oggetto che rappresenta la connessione tra due computer
- ## Caratteristiche:
    - Composto da **IP** che identifica il PC nella rete, e dal numero **porta** che identifica l'applicazione che è in esecuzione su quel computer

- ## Utilizzo:
    - Generalmente viene utilizzato un'architettura **client-server** dove si deve creare una connessione tra due computer:
        - server usufruisce dei servizi ai client o soddisfa le richieste fatte da quest'ultimi
        - client richiede un servizio o dei dati dal server

    - Vengono utilizzati nel TCP e nell'UDP 

- TCP:
    - ***Transfer control protocol***
    - Sono dei protocolli che si basano sulla connessione orientata --> si deve creare una connessione per comunicare --> handshake 
    - il pacchetto che si manda si chiama segmento ed ha un header di 20 byte (ci sono dei campi per controlli)
    - È più sicuro perché garantisce che il pacchetto arrivi --> *stop and wait* 🛑 --> aspetto ack quando mando, se non ricevo niente, rimando 
    - ### handshake 🤝(fase per stabilire la connessione inviandosi dei pacchetti)
    - Esempio: chiamata $\to$ stabilire la connessione da entrambe le parti 
- ## Implementazioni del TCP:
    - In Java si usa la classe "java.net.Socket"
    - Prima si esegue il Server e poi si esegue i client
    - Si istanzia il server con un oggetto SocketServer passando IP e porta
    - Poi si crea un oggetto Socket di cui invochiamo il metodo serverSocket.accept() per accettare le richieste dei client che vogliono comunicare
    - Il client deve conoscere l'IP e porta del server  
    - Per comunicare entrambi usano un BufferReader e DataOutputStream per leggere e scrivere che devono essere connessi al socket 

- UDP:
    - ***User datagram protocol***
    - È un protocollo ***connectionless*** cioè non serve fare handshake 🤝 (stabilire la connessione)
    - Il PDU si chiama Datagram ed ha un header di 8 byte (< rispetto al TCP perché non ci sono campi controllo) 
    - È più veloce del TCP perché non c'è il sistema stop and wait (aspetto ACK) 
    - È meno affidabile perché non ho garanzia che arrivi (no ack)
    - Esempio: video streaming $\to$ più velocità, anche se non arrivano tutti i pacchetti, comunque non influisce (l'occhio non si accorge di qualche perdita del frame)
- ## Implementazioni del UDP:
    - In Java si usa la classe "java.net.DataGramSocket"
    - L'implementazione è uguale (per entrambi) solo che l'ordine cambia (prima client scrive, e poi sarà il server)
    - Per comunicare entrambi istanziano un DatagramSocket e per inviare usano un DatagramPacket. Quando si manda il messaggio, si inserisce il contenuto e l'IP + porta del destinatario. Colui che lo riceve, è in grado di ricavare l'IP e porta di colui che ha mandato 
    - receive (per fare get) e send (inviare)

    - Tramite UDP si può implementare multicast:
        - Il socket è un oggetto MulticastSocket 
        - ho un ip di gruppo ed entrano in questo gruppo facendo il join 
        - il modo di comunicare è lo stesso dell'UDP 
        - solo il server manda i messaggi che verranno ricevuti dai client
