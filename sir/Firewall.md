- **dispositivo fisico o un software che filtra il traffico di rete sia in entrata che in uscita in base ad un insieme di regole stabilite durante la fase di configurazione.**
- lavora dal 3 - 7 livello e viene svolto principalmente dal router 
- Essi migliorano la sicurezza della rete e si basano su ==3 principi==:
    1) *deve essere l'unico punto di "contatto" tra rete interna ed esterna (altrimenti è inutile)*
    2) *solo il traffico autorizzato può attraversare il firewall* 
    3) *il firewall stesso deve essere un sistema sicuro* 
- ***==Classificazioni==***:
    -  ***==Natura==***:
         - software 
         - hardware 
    -  ==***Direzione traffico***==: 
        -  ***incoming***: gestisce il traffico che arriva dall'esterno verso i server nel DMZ  
        - ***egres***: gestisce il traffico che va dalla LAN all'esterno (quelli non autorizzati non escono) 
  -  ***==Tipologia==***:
       1) ***packet filter***: firewall che appena riceve il pacchetto controlla alcune informazioni dell'header (parte del pacchetto dove c'è IP e altre cose). Controlla se l'IP sorgente/destinazione, porta sorgente/destinazione e il protocollo siano possibile dalle regole definiti nel firewall. 
            - generalmente è già implementato nei router (*più economici*), ma sono meno sicuri --> non controllano il payload (dati) --> mandare virus
       2) ***application/proxy***: oltre a fare le cose del packet filter, controlla anche il payload (più sicurezza). Inoltre funge anche da server proxy --> *"maschera il mittente"* ovvero il pacchetto in uscita ha l'IP del server. Essendo che controlla è più lento 
- Quest'ultimo per controllare usa gli [[ACL]]

