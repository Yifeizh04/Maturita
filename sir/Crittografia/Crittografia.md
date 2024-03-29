# Crittografia
- **Tecnica** **per proteggere i dati rendendo un messaggio incomprensibile alle persone non autorizzate**
- *Per comprendere il significato serve conoscere la chiave (informazione per decriptare le cose) e deve essere conosciuta solo da chi è autorizzato*
- **Caratteristiche di una crittografia sicura**
    - Il funzionamento deve essere noto   
- esistono ***2 tipi***:
    -  ***simmetrica***: *una chiave per criptare/decifrare* 
    - ***asimmetrica***: *una chiave per criptare (pubblica), una per decifrare (privata)*
 - Esempio di simmetrica:
    - DES:
        - ricevo testo e chiave da 64 bit (della chiave me ne servono solo 56 --> gli ultimi 8 di ogni byte sono di controllo )
        - permuto il messaggio inziale 
        - Divido il messaggio in due blocchi L ed R 
        - Eseguo fiestel per 16 volte:
           -  Genero una sub-key (48 bit)
           -  **Blocco E** $\to$ espando il blocco R da 32 a 48 così da poter fare la XOR con sub-key --> si può prendere gli ultimi bit della riga prima inserendoli all'inizio di ogni riga 
           - **Blocco F** $\to$ si crea MAT = R (espanso) XOR sub-key 
           - MAT deve passare da 48 a 32 per fare XOR con L $\to$ SBOX (matrice di 4 * 16) $\to$ per ogni riga, si comprime in un numero da 4 bit $\to$ primo e ultimo bit mi dà la riga del SBOX, quelli in mezzo la colonna 
           - Compresso il tutto, faccio la XOR con L. Quest'ultimo diventa il nuovo blocco R, e il vecchio blocco R diventa il nuovo blocco L. E si riesegue fiestel alternando (per comodità faccio swap(L, R) così lavoro solo con R)
    - Finito i 16 round, ripermuto nuovamente ed ho il nuovo messaggio 
 -  RSA 
    - Rivest, Shamir, Adleman
    - si scelgono due numeri primi $P$ e $Q$ grandi e definiamo $N = P * Q$, e $\phi(N) = (P - 1) * (Q - 1)$
    - si sceglie un certo numero $E$ (chiave pubblica) dove:
       - E < $\phi(N)$  e gcd(E, $\phi(N)$) = 1 (comprimo) 
   - si sceglie $D$ tale che $(E*D) % \phi(N) = 1 \to$  $D$ è *l'inverso modulare*, oltre che essere chiave privata. Sappiamo che esiste questo inverso perché abbiamo scelto un certo $E$ tale che $gcd(E, \phi(N)) = 1$ 
   - Sia $M$ il messaggio cifrato e $C$ il messaggio criptato allora:
       - criptare: $M^{E} mod N = C$ 
       - decifrare: $C^{D} mod N = M$   
 
 - Enigma
    - Macchina per cifrare i messaggi dei nazisti durante la seconda guerra mondiale
    - Ci 3 rotori dove ognuno ha 26 lettere rotore è connesso alla successiva con molti circuiti che fa funzionare il meccanismo di convertire una lettera in un'altra
    - Quando digito una lettera, il primo rotore gira, e appena fa un giro completo (26 volte), il secondo rotore gira di 1 e via dicendo...
    - La chiave viene cambiato ogni giorno e ci sono dei libretti dove vengono scritti le chiavi da utilizzare ogni giorno
