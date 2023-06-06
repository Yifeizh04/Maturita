# Socket
- ## Mini introduzione:
    - In una struttura client server c'è un client che usufruisce di un servizio che si basa su certi protocolli del 4 livello della pila ISO/OSI e un esempio magari è HTTP. Questi protocolli si basano sul TCP oppure UDP che si possono implementare tramite i socket.
- ## Definizione
    - Punto finale di una connessione bidirezionale 
- ## Caratteristiche:
    - Composto da **IP** che identifica il PC nella rete, e dal numero **porta** che identifica l'applicazione che è in esecuzione su quel computer

- UDP:
    - ***User datagram protocol***
    - È un protocollo ***connectionless*** cioè non serve fare handshake 🤝 (non bisogna stabilire la connessione per comunicare)
    - Il PDU si chiama Datagram ed ha un header di 8 byte (< rispetto al TCP perché non ci sono campi controllo) 
    - È più veloce del TCP perché non c'è il sistema stop and wait 
    - È meno affidabile perché non ho garanzia che arrivi ma faster
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

- TCP:
    - ***Transfer control protocol***
    - E' una famiglia di protocolli che si basano sulla connessione orientata $\to$ si deve creare una connessione per comunicare $\to$ handshake 
    - il pacchetto che si manda si chiama segmento ed ha un header di 20 byte (ci sono dei campi per controlli)
    - È più sicuro perché garantisce che il pacchetto arrivi $\to$ *stop and wait* 🛑 $\to$ aspetto ack quando mando, se non ricevo niente, rimando 
    - Esempio: chiamata $\to$ stabilire la connessione da entrambe le parti 
- ## Implementazioni del TCP:
    - In Java si usa la libreria "java.net.Socket"
    - Si istanzia il server con un oggetto SocketServer passando IP e porta
    - Poi si crea un oggetto Socket di cui invochiamo il metodo serverSocket.accept() per accettare le richieste dei client che vogliono comunicare
    - Prima si esegue il Server e poi si esegue i client
    - Il client deve conoscere l'IP e porta del server  
    - Per comunicare entrambi usano un BufferReader e DataOutputStream per leggere e scrivere che devono essere connessi al socket 

