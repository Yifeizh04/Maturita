# **Integrali definiti**
- Sia una funzione f(x) continua in [a, b], si definisce integrale definito la somma delle aree 

- ## Come stimarlo?
    - Si divide l'intervallo [a, b] in *n* sotto intervalli lunghi ${\frac{b - a}{n}}$ = ${\triangle}x$
    - Inoltre definiamo m[i] il minimo, M[i] come il massimo in un intervallo della funzione
    - ***${\sum_{i=0}^{n-1}}{\triangle}x m[i] <= {\int_{a}^{b} f(x)} <= {\sum_{i=0}^{n-1}}{\triangle}x M[i] $***
    - La prima somma è approssimata per difetto, la seconda per eccesso
- ## Osservazione:
    - se rimpiccioliamo il sotto intervallo: 
        - $\lim_{{\triangle}x\to 0^+}$ o  $\lim_{n\to\infty} $

    - si nota che m[i] e M[i] si avvicinano ${\to}$ prendendo sotto-intervalli piccolissimi, si trova anche l'area:
    - ***${\lim_{n\to\infty}} {\sum_{i=0}^{n-1}}{\triangle}x m[i] = {\lim_{n\to\infty}} {\sum_{i=0}^{n-1}}{\triangle}x M[i] = {\int_{a}^{b} f(x)} $***

- ## Proprietà
    - Valgono quelli dell'integrale indefinito
    - Splittare l'integrale:
        - ***${\int_{a}^{b} f(x)} = {\int_{a}^{c} f(x)} + {\int_{c}^{b} f(x)} $ con a < c < b***
        - ***${\int_{a}^{a} f(x)} = 0$ [^1] ***
        - ***${\int_{a}^{b} f(x)} = -{\int_{b}^{a} f(x)}$ ***

- ## Come trovarlo più velocemente?
    - **Teorema del valor medio**
        - Sia f(x) una funzione continua in [a, b], allora esiste almeno un punto z tale che *f(z) * (b - a) = ${\int_{a}^{b} f(x)}$*
        - **Proof:**
            - Definiamo m come il minimo in [a, b] e M come il massimo in [a, b]
            - Quindi:
                - ***m <= f(x) <= M ${\to}$ ${\int_{a}^{b} m dx}$ <= ${\int_{a}^{b} f(x)}$ <= ${\int_{a}^{b} M dx}$***

            - Notiamo che la base è (b - a), e l'altezza è una costante in [a, b] se consideriamo **m ed M**. Quindi possiamo riscrivere:
                - ***m * (b - a) <= ${\int_{a}^{b} f(x)}$ <= M * (b - a)***
            - Ma se b > a, allora (b - a) > 0, quindi dividendolo non cambia i versi della disequazione:  
                - ***m <= ${\frac{1}{(b - a)}}{\int_{a}^{b} f(x)}$ <= M***
            - Dobbiamo verificare se esiste un certo f(x) che ${\in}$ [m, M]. Questo è facile da dimostrare perché se f(x) è continua, per essere tale deve passare in tutti i f(x) ${\in}$ [m, M] dimostrando che esiste almeno un certo punto
            - Interpretazione geometrico:
                - Possiamo vedere l'area "sotto-curva" come un'area di un rettangolo con base (b - a) e altezza f(z) dove z è il valor medio. (Concettualmente: modello l'area sotto la curva in maniera da farlo diventare rettangolo)

    - **Teorema Torricelli Borrow**
        - **Funzione integrale**   
            - Si definisce *F(x)* funzione integrale di f(x) che è continua in [a, b], una funzione che è la somma dell'area sotto curva di f(x) da [a, x]
        - TODO: definizione bla bla

        - **Proof:**
            - Concetto ***derivata:***
                - F'(x) = $\lim_{h\to 0^+} {\frac{F(x + h) - F(x)}{h}}$
            - Scegliamo un certo h tale che a <= x + h <= b:
                - F(x + h) - F(x)

            - Ma F(x) è funzione integrale quindi:
                - ${\int_{a}^{x+h} f(x) dx}$ - ${\int_{a}^{x} f(x) dx}$
            
            - Ma per la proprietà dell'additività, splitto il primo membro:
                - ${\int_{a}^{x+h} f(x) dx}$ = ${\int_{a}^{x} f(x) dx}$ + ${\int_{x}^{x+h} f(x) dx}$
            - Quindi: [^2] 
                - ${\int_{a}^{x} f(x) dx}$ + ${\int_{x}^{x+h} f(x) dx}$ - ${\int_{a}^{x} f(x) dx}$ =  ${\int_{x}^{x+h} f(x) dx}$
            - Ma questo integrale possiamo riscriverlo per il teorema del valor medio:
                - ${\int_{x}^{x+h} f(x) dx}$ = f(z) * (x + h - x)
            - Quindi ritornando all'inizio abbiamo questa equazione:
                - F(x + h) - F(x) = f(z) * (x + h - x)
                - ${\frac{F(x + h) - F(x)}{h}} = f(z)$
            - Studiamo il comportamento di ciò con $\lim_{h\to0^+}$
                - $\lim_{h\to0^+}{\frac{F(x + h) - F(x)}{h}} = \lim_{h\to0^+}f(z)$
                - Sappiamo che z ${\in}$ [x, x+h]
                - Ma se $\lim_{h\to0^+} x + h = x$, allora anche z tende a z da destra
                - $\lim_{h\to0^+} f(z) = f(x) $
            - Riscrivendo il tutto:
                - $\lim_{h\to0^+}{\frac{F(x + h) - F(x)}{h}} = f(x)$
                - Ma il membro sinistro è la derivata quindi si dimostra che:
                    - $F'(x) = f(x)$


[^1]: proof: base è (a - a) = 0 e quindi l'area è 0

[^2]: idea intuitiva: vedere F(x) come somma per prefissi