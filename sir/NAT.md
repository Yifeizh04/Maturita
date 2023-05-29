- network address translation $\to$ tradurre indirizzi IP 🌍
- Perché è stato creato? Per navigare su internet, usiamo un identificativo univoco per distinguerci (si usa il nome cognome per riferirsi alla gente) che è IP. 
     -  IP è una sequenza di 4 numeri che vanno da 0-255 $\to$ numero è un byte (8 bit $\to$ 2$^{8}$). Quest'ultimo serve per identificarci in una rete e può essere classificato per in 5 classi (si può capire la classe in base alla posizione del primo bit del primo byte da sx a dx):
               -   A, B, C (queste 3 vengono usati principalmente), D (multicast), E (scopi militari)
               -   pubblico (univoco nel mondo), privato (univoco nella sotto rete)
 - Essendo che sono pochi gli indirizzi pubblici in confronto al totale dei dispositivi al mondo, si usano gli IP privati $\to$ per comunicare mi serve pubblico $\to$ tradurre IP privato a pubblico.
 - **Tipologie:**
	1. **Statico:** 
		- Ad ogni IP privato ne corrisponde uno pubblico. 
		- Questo viene utilizzato per i server:
			- ip non deve mai cambiare altrimenti il DNS non lo trova $\to$ si decide di usare NAT statico e dare direttamente un IP pubblico perché se faccio la seconda opzione, dovrei comprare più indirizzi (es: una rete con un solo server devo comprare 4 indirizzi pubblici come minimo (rete, broadcast, gateway e server)
			- sono accessi spesso dall'esterno e lo statico è più veloce 
			- È più costoso ma più veloce perché non c'è attesa
	 2. **Dinamico:**
		 - Abbiamo un pool di indirizzi pubblici e il numero di quest'ultimi è < al numero di IP privati. 
				- È più lento (si può formare coda attesa) ma più cheap 

	3. **Pat:**
		- Port address translation 
		- Abbiamo un solo IP pubblico e ci si distingue con la porta utilizzata. L'unica cosa è associare per ogni pacchetto la porta utilizzata e in una tabella ci mappiamo IP privato - porta usata. 
