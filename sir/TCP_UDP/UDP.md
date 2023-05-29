- User datagram protocol 
- È un protocollo ***connectionless*** cioè non serve fare handshake 🤝 (stabilire la connessione)
- Il PDU si chiama Datagram ed ha un header di 8 byte (< rispetto al TCP perché non ci sono campi controllo) 
- È più veloce del TCP perché non c'è il sistema stop and wait (aspetto ACK) 
- È meno affidabile perché non ho garanzia che arrivi (no ack)
- Protocolli:
	- DNS 
		- Domain name system 
		- protocollo che traduce i nomi in IP (dobbiamo conoscere l'IP per raggiungere --> è più Easy ricordare nomi) 
		- All'interno dei server c'è una tabella dove ci sono le traduzioni (record)--> ci sono 3 tipi di record:
			1. A record: traduzione nome ad IP 
			2. CNAME: alias del nome 
			3. NS record: l'IP del server di riferimento per alcuni "domini (es: .it, .com)"
		- La struttura del DNS è gerarchica --> se il mio server non conosce la traduzione, lo chiede a qualcun'altro. Appena qualcuno lo sa, ritorna indietro con le informazioni (quest'ultimo se lo salva nella cache così da non rifare tutto il giro). 
		- Struttura:
			1. Root (c'è ne sono 13 al mondo)
			2. 1 livello: .com, .org, ecc... 
			3. 2 livello: sotto-livello del 1 
			4. E via dicendo....

	- DHCP:
		- Dynamic host configuration protocol --> assegnare gli indirizzi IP dinamica
		- Usa la porta 67
		- Funzionamento: diviso 4 fasi
			- DHCP discover: il client manda una richiesta broadcast ai server in ascolto 
			- DHCP offer: il server ricevuto, mandano la loro offerta al richiedente 
			- DHCP request: il richiedente sceglie una offerta e manda la richiesta al server 
			- DHCP ack: il server inoltra un pacchetto che contiene IP, maschera, gateway --> associa il MAC del richiedente all'IP dato, e mette un lasso di tempo (se scade e non rinnova, l'IP diventa libero)
