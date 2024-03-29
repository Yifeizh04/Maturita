- Access control list 🛂 
- È un insieme di regole che permette/nega l'accesso a qualcosa **(permit e deny)**
- Ciò viene applicato nel router in particolare nelle interfacce specificando se è di entrata o uscita
- All'inizio tutti possono passare se imposto nessuna regola, appena ne imposto una, il resto è deny all (faccio passare solo a chi lascio in base alle regole che imposto)
- L'ordine con cui inserisco le regole è importante visto che li legge/"esegue" in ordine in cui le ho messe $\to$ mettere le regole più deboli ("range più piccoli") prima.  
- Si usa un numero per identificarlo e lo classifica:
    - numero $\in$ [1, 99] o [1300, 1999] $\to$ standard 
          - si basa solo sull'IP sorgente 
    - numero $\in$ [100, 199] o [2000, 2699] $\to$ estese
          - si basa sull'IP sorgente e destinazione 
- Non viene solo utilizzato solo nel campo degli IP ma anche per i protocolli (come http, pop3, ecc...) e porte 
- Generalmente quando si scelgono gli indirizzi IP nelle ACL, sostanzialmente si sta facendo un Wildcard.  
- ## Wildcard 
    - È una maschera che ci permette, in base all'IP di partenza, di decidere quali IP possono / non possono entrare. Può essere visto come l'opposto della maschera di rete. 
    - Se ho un indirizzo di partenza A, e ho una Wildcard, un indirizzo B può "passare" $\iff$ $\forall$ i | Wildcard[i] = 0,  A[i] = B[i] 
