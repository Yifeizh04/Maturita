## **Solido rotazione**

- Vogliamo calcolare il volume del solido che viene a formarsi ruotando una funzione $f(x)$ attorno all'asse $x$ nell'intervallo [a, b] (si suppone che sia continua in [a, b])

- ## Premessa
    - Vedere integrale indefinito dove le idee sono uguali

- Come calcolarlo?
    - Suddividere l'intervallo in $n$ sotto-intervalli lunghi ${\triangle}x = \frac{b - a}{n}$
    - Definiamo $m[i]$ come il minimo e $M[i]$ come il massimo del sotto-intervallo i-esimo
    - Fatto ciò, creiamo due rettangoli per ogni sotto-intervallo con base ${\triangle}x$ e l'altezza di uno sarà $m[i]$ e l'altro sarà $M[i]$
    - Essendo che ruoto $f(x)$, ruoto anche questi rettangoli riconducendomi al cilindro:
         - il raggio = altezza del rettangolo
         - l'altezza del cilindro = ${\triangle}x$)
    - Calcoliamo il volume per difetto (($v1$)) e per eccesso ($v2$):
        - ${\sum_{i=0}^{n} m[i]^2 * \pi * {\triangle}x } = v1 $     
        - ${\sum_{i=0}^{n} M[i]^2 * \pi * {\triangle}x } = v2 $
    - Sia $V$ il volume del solido di rotazione sappiamo che:
        - $v1 \leq V \leq v2$
    - Ma se suddividiamo in tantissmi sotto-intervalli avremo una somma più precisa:
        - ### ${\lim_{n\to\infty} \sum_{i=0}^{n} m[i]^2 * \pi * {\triangle}x = \lim_{n\to\infty} \sum_{i=0}^{n} M[i]^2 * \pi * {\triangle}x}$
    - Ma sappiamo che il $\pi$ possiamo portarlo fuori perchè è una costante, la $m[i] = M[i] = f(x)$, e ${\triangle}x$ essendo $0^+$, diventa dx quindi la formula diventa:
        - $V = \pi * {\int_{a}^{b} f(x)^2 dx}$ 

## ***Integrali improrpi***

