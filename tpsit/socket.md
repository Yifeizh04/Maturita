# Socket
- ## Mini introduzione:
    - In una struttura client server c'è un client che usufruisce di un servizio che si basa su certi protocolli del 4 livello della pila ISO/OSI e un esempio magari è HTTP. Questi protocolli si basano sul TCP oppure UDP che si possono implementare tramite i socket.
- ## Definizione
    - Punto finale di una connessione bidirezionale 
- ## Caratteristiche:
    - Composto da **IP** che identifica il PC nella rete, e dal numero **porta** che identifica l'applicazione che è in esecuzione su quel computer

- TCP:
    - ***Transfer control protocol***
    - E' una famiglia di protocolli che si basano sulla connessione orientata $\to$ si deve creare una connessione per comunicare $\to$ handshake 
    - il pacchetto che si manda si chiama segmento 
    - È più affidabile perché garantisce che il pacchetto arrivi $\to$ *stop and wait* 🛑 $\to$ aspetto che mi arrivi un messaggio di conferma ricezione e se non mi arriva, rimando 
    - Esempio: chiamata $\to$ stabilire la connessione da entrambe le parti 
- ## Implementazioni del TCP:
    - Si istanzia il server con un oggetto SocketServer passando IP e porta
    - Poi si crea un oggetto Socket di cui invochiamo il metodo serverSocket.accept() per accettare le richieste dei client che vogliono comunicare
    - Il client deve conoscere l'IP e porta del server  
    - Per comunicare entrambi usano un BufferReader e DataOutputStream per leggere e scrivere che devono essere connessi al socket 
    - Bisogna eseguire prima il Server e poi i client
    
- UDP:
    - ***User datagram protocol***
    - È un protocollo ***connectionless*** (non bisogna stabilire la connessione per comunicare)
    - È più veloce del TCP perché non c'è il sistema stop and wait 
    - È meno affidabile perché non ho garanzia che arrivi ma faster
    - Esempio: video streaming $\to$ serve più velocità, anche se non arrivano tutti i pacchetti, comunque non influisce (l'occhio non si accorge di qualche perdita del frame)
- ## Implementazioni del UDP:
    - L'implementazione è uguale sia per server e sia per client.
    - Per comunicare entrambi istanziano un DatagramSocket e per inviare usano un DatagramPacket. Quando si manda il messaggio, si inserisce il contenuto e l'IP + porta del destinatario così che colui che lo riceve, è in grado di ricavare l'IP e porta del mittente 
    - Per ricevere il pacchetto si usa il metodo receive e per inviare si usa send (inviare)

    - Tramite UDP si può implementare multicast:
        - Ci sono tanti client che sono connessi in un gruppo e il server quando invia un messaggio la gruppo, lo ricevono tutti del gruppo 
        - Il socket è un oggetto MulticastSocket 
        - ho un ip di gruppo ed entrano in questo gruppo facendo il join 
        - il modo di comunicare è lo stesso dell'UDP 


