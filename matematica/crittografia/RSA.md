# RSA

- **Funzione Eulero**
    - Un numero $a$ ha un inverso in $Z_n$ $\iff$ $\gcd(a, n) = 1$
    - In particolare l'insieme degli elementi invertibili in $Z_n$ lo indichiamo con $Z_n^{*}$ 
    - La funzione di Eulero o toziente indicato con $\phi(n) = \# {1 \leq x \lt n | \gcd(x, n) = 1}$ [^1]

    - **Proprietà**
        - $\phi(a * b) = \phi(a) * \phi(b) \iff \gcd(a, b) = 1$ [^2] 
        - $\phi(p) = p - 1$ dove $p$ è primo
        - $\phi(p^{k}) = p^{k} - p^{k - 1}$

- **Teorema Eulero**
    - Per ogni $n \ge 2$ e per ogni $a \in Z_n^{*}$ (cioè $\gcd(a, n) = 1$) vale la seguente uguaglianza:
        - $a^{\phi(n)} \equiv 1 $ mod $n$ 
    - dove $\phi(n)$ è la funzione di Eulero

    - **Corollario** [^3]:
        - Per ogni $n \gt 2$ e per ogni $a \in Z_n^{*}$ l'inverso di $a$ è $a^{\phi(n) - 1}$
        - Proof:
            - $a^{\phi(n)} \equiv 1 $ mod $n$ 
            - $a * a^{\phi(n) - 1} \equiv 1 $ mod $n$ 
            - Ma per definizione di inverso cioè l'inverso di x modulo n è un certo numero y t.c $x * y \equiv 1$ mod $n$, 
            abbiamo dimostrato l'inverso

- **Funzionamento RSA**
    - Rivest, Shamir, Adleman
    - si scelgono due numeri primi $P$ e $Q$ e definiamo $N = P * Q$, e $\phi(N) = (P - 1) * (Q - 1)$
    - si sceglie un certo numero $E$ (chiave pubblica) dove:
       - E < $\phi(N)$  e gcd(E, $\phi(N)$) = 1 (comprimo) 
   - si sceglie $D$ tale che $(E*D)$ mod $\phi(N) = 1$ dove $D$ è *l'inverso modulare*, oltre che essere chiave privata. Sappiamo che esiste questo inverso perché abbiamo scelto un certo $E$ tale che $gcd(E, \phi(N)) = 1$ 
   - Sia $M$ il messaggio cifrato e $C$ il messaggio criptato allora:
       - criptare: $M^{E} mod N = C$ 
       - decifrare: $C^{D} mod N = M$   

    - Proof del funzionamento:
        - Si suppone che $M$ e $N$ siano coprimi
        - Vogliamo dimostrare che $M^{ed}$ mod $N = M$ dove $C^{d} = M^{ed}$

        - Sappiamo che $ed \equiv 1$ mod $N$ e quindi per definizione di congruenza, possiamo riscriverlo come $ed = 1 + k*\phi(N)$ con $k \in \Z$
        - Quindi:
            - $M^(1 + k*\phi(N))$ mod $N$ = $M * M^{k*\phi(N)}$ mod $N$ = $M * (M^{\phi(N)})^{k}$ mod $N$ 
        - Ma per la supposizione inziale, vale il teorema di Eulero visto che $\gcd(M, N) = 1$ e quindi $M^\phi(N) \equiv 1$ mod $N$ ma $1^k$ fa sempre 1 e quindi:
            - $M$ mod $N = M$  


[^1]: la cardinalità dell'insieme dei elementi invertibili in Zn
[^2]: è moltiplicativo se i due numeri sono comprimi

[^3]: un corollario è dato un teorema, ne consegue alcune proprietà che sono ovvie


