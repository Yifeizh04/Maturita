# Integrali definiti

- **Nasce per calcolare l'area di figure curve (es: cerchi, trapezoidi)**

- Consideriamo di avere una funzione positiva e continua in $[a, b]$ e vogliamo calcolare l'area sotto la curva in $[a, b]$

- ## **Calcolo stimato**
    - Dividiamo l'intervallo $[a, b]$ in $n$ sottointervalli lunghi ${\triangle}x = \frac{b-a}{b}$   
    - Consideriamo il $m[i]$ come il minimo del sotto-intervallo i-esimo e $M[i]$ come il massimo
    - Creiamo dei sotto-rettangoli di base ${\triangle}x$ e altezza $m[i]$ e un'altro alto $M[i]$. Se li sommiamo avremo due somme:
        - ${\sum_{i=0}^{n} m[i] * {\triangle}x } = s $     
        - ${\sum_{i=0}^{n} m[i] * {\triangle}x } = S $ 
    - L'area sotto curva che indicheremo con ${\int_{a}^{b} f(x)}$ e vale questa disugaglianza:
        - ${s \leq {\int_{a}^{b} f(x)} \leq S}$

    - **Osservazione:**
        - Se rimpiccioliamo l'intervallo (aumentando N ${\to}$ abbassare ${{\triangle}x}$), $m[i]$ e $M[i]$ si avvicinano [^1] ${\to}$ la somma diventa più precisa ${\to}$ se facciamo N grandissimo, avremo la somma precisa.

    - ### ${\lim_{n\to\infty} \sum_{i=0}^{n} m[i] * {\triangle}x = \lim_{n\to\infty} \sum_{i=0}^{n} m[i] * {\triangle}x = \int_{a}^{b} f(x)}$

- ## **Proprietà**:
    - Valgono quelle di linearità
    - $\int_{a}^{a} f(x) = 0$ [^2] 
    - $\int_{a}^{b} f(x) = \int_{a}^{c} f(x) + \int_{c}^{b} f(x)$  dove $ a \lt c \lt b $ [^3]
    - se f(x) > g(x) allora $\int_{a}^{b} f(x) \gt  \int_{a}^{b} g(x)$ [^4]

- ## **Teorema del valor medio**
    - Sia f(x) una funzione continua in $[a, b]$ allora esiste almeno un punto $z$ tale che $f(z) * (b - a) = \int_{a}^{b} f(x)$
    - Si suppone che b > a [^5]
    - Proof:
        - sia $m$ il minimo e $M$ il massimo in $[a, b]$
        - allora vale la seguente disuguaglianza:
            - $\int_{a}^{b} m \leq \int_{a}^{b} f(x) \leq \int_{a}^{b} M$
        - Ma se abbiamo una costante come funzione, si può vederlo come rettangolo (la y è sempre uguale ${\to}$ altezza fissa):
            - $(b - a) * m \leq \int_{a}^{b} f(x) \leq (b - a) * M$
        - Dividiamo per $(b - a) \to$ i segni della disequazione non cambia visto che $\gt 0$
            - $ m \leq \frac{1}{b - a}\int_{a}^{b} f(x) \leq M$
        - Sappiamo che esiste questo valore per il teorema dei valori intermedi [^6]
        - Quindi esiste almeno un $z = \frac{1}{b - a}\int_{a}^{b} f(x)$

- ## **Teorema di Torricelli Barrow / teorema calcolo fondamentale**
    - ### **funzione integrale**:
        - sia f(x) una funzione continua in $[a, b]$, allora si definisce funzione integrale di $f(x)$ una funzione $F(x)$ = **${\int_{a}^{x}f(t)dt}$**
- **Enunciato**
    - sia $f(x)$ una funzione continua in $[a, b]$ e $F(x)$ la funzione integrale di $f(x)$, allora esiste la derivata di $F(x)$ per ogni x in [a, b] ed è $f(x)$.
        - $F'(x) = f(x) \forall x \in [a, b]$  quindi $F(x)$ è $primitiva$ di $f(x)$

    - Proof:
        - Definizione di derivata:
            - $F'(x) = {\lim_{h\to 0^+} \frac{F(x + h) - F(x)}{h}}$
            
        - Scegliamo un $h$ tale che valga $a \lt x + h \lt b$
            - ${F(x + h) - F(x)}$
        
        - Ma $F(x)$ è funzione integrale quindi:    
            - ${F(x + h) - F(x) = \int_{a}^{x + h} f(t)dt - \int_{a}^{x} f(t)dt}$
        - Per la proprietà additività (splittare il range):
            - ${\int_{a}^{x + h} f(t)dt = \int_{a}^{x} f(t)dt + \int_{x}^{x + h} f(t)dt}$
        - Quindi: 
            - ${\int_{a}^{x + h} f(t)dt - \int_{a}^{x} f(t)dt = \int_{x}^{x + h} f(t)dt}$
          
        - Ma per l'interpretazione geometrica del teorema del valor medio vale:
            - $\int_{x}^{x + h} f(t)dt = f(z) * h$ 
        - ${F(x + h) - F(x) = f(z) * h}$ 
        
        - Dividiamo per $h$
        - ${\frac{F(x + h) - F(x)}{h} = f(z)}$ 
        
        - Studiamo il comportamento dell'uguaglianza per $\lim_{h \to 0^+}$
            - ${\lim_{h \to 0^+} \frac{F(x + h) - F(x)}{h} = \lim_{h \to 0^+} f(z)}$
            
        - Membro destro:
            - essendo che $z \in [x, x+h]$ se ${h \to 0^+}$ allora z tende x da destra quindi:
                - ${\lim_{h \to 0^+} f(z) = \lim_{z \to x^+} f(z) = f(x)}$
                
        - Membro sinitro:
            - E' la definizione di derivata
            
        - Quindi se sostituisco il tutto:
            -  $F'(x) = f(x)$

- **Risoluzione degli integrali definiti**
    - Sia $\phi(x)$ una primitiva qualsiasi di $f(x)$ $\to$ $\phi(x) = F(x) + c$ 
    
    - Sappiamo però, con il teorema Torricelli Barrow, che $F(x)$ [^7] è una primitiva
    
    - Definiamo $\phi(a)$:
        - $\phi(a) = F(a) + c = \int_{a}^{a} f(t)dt + c$
        - $\phi(a) = 0 + c$ ${\to}$ $\phi(a) = c$
    
    - Definiamo $\phi(b)$:
        - $\phi(b) = F(b) + c = \int_{a}^{b} f(t)dt + c$
        
    - Ma $c = \phi(a)$
    
    - $\phi(b) = \int_{a}^{b} f(t)dt + \phi(a)$ ${\to}$ $\int_{a}^{b} = \phi(b) - \phi(a)$
    
    - Quindi basta trovare una primitiva qualsiasi di $f(x)$ e sostituire $a$ e $b$   

[^1]: principio dei due carabinieri
[^2]: proof: teorema valor medio --> base * altezza = (a - a) * f(z) = 0 * f(z) = 0
[^3]: proof: pensare somma prefissi
[^4]: proof: se f(x) > g(x), allora l'area è maggiore
[^5]: proof: se b < a, allora l'integrale diventa < 0 e i segni disequazioni sono capovolti, quindi mi riconduco ad avere b > a
[^6]: proof: se voglio tracciare una linea tra minimo e massimo, l'unico modo di non passare per alcune y tra questo range è ammettere punti di discontinuità, ma ciò non può avvenire visto che f(x) è continuo
[^7]: funzione integrale di f(x)
