# Risoluzione  **_ay'' + by' + cy = 0_**

Si assume che **$a$ $\neq$ 0** altrimenti si ha un equazione differenziale di primo ordine. Assunto cio', si puo' dividere da tutte le parti per **_a_** $\to$  $y'' + \frac{by'}{a} + \frac{cy'}{a} = 0$

Per comodita' chiamiamo _m = $\frac{b}{a}$_ ed $n = $\frac{c}{a}$. Quindi si ha questa equazione differenziale $\to$ **_y'' + m * y' + n * y = 0_**

Per risolvere cio', si suppone che **_y = e$^{kx}$_** sia una soluzione.

Quindi si avra' che:
- $y = e^{kx}$
- $y' = k * e^{kx}$
- $y'' = k^{2} * e^{kx}$

Avendo cio', si riscrive l'equazione di prima sostituendo questi valori che conosciamo:

**_y'' + m * y' + n * y = 0_**

$k^{2} * e^{kx} + m * k * e^{kx} + n * e^{kx} = 0$

Qui si puo' raccogliere $e^{kx} \to  e^{kx} * (k^{2} + m * k + n) = 0$

Per la legge dell'annullamento del prodotto, questa quantita' $e^{kx} * (k^{2} + n * k + m)$ e' 0 $\iff$ $k^{2} + m * k + n = 0$     
($e^{kx} \gt 0 \forall x \in \R  \to$ per forza di cose deve essere il secondo membro a far 0)

### **Definizioni:**

$(k^{2} + m * k + n) \to$ equazione caratteristica dell'equazione differenziale

$\triangle = m^{2} - 4n \to$ discriminante dell'equazione differenziale (ci dice gia' che casistica/come dobbiamo risolverlo)

Abbiamo 3 casi:
- $\triangle \gt 0$ 
  - Si hanno **2** soluzioni chiamate $k_{1}$ e $k_{2}$ dove sono distinte e k$_{1}$, k$_{2}$ $\in$ $\R$. Quindi si puo' affermare (non ancora dimostrato):
      - (Per comodita' chiamo i = k1, j = k2)
      - $e^{ix}$ e' una soluzione dell'equazione differenziale
    -  $e^{-ix}$ e' una soluzione dell'equazione differenziale  
    -  Quindi $y=c_{1}*e^{ix} + c_{2}*e^{-jx}$ e' la soluzione dell'equazione differenziale dove c$_{1}$, c$_{2}$ $\in$ $\R$   (Si puo' dimostrare anche per questa che vale il teorme del caso y'' + cy = 0)
    
- $\triangle = 0$ 
  - Si hanno **2** soluzioni chiamate $k_{1}$ e k$_{2}$ che sono coincidenti k$_{1}$ = k$_{2}$ = z e z $\in$ $\R$. Quindi si puo' affermare (non ancora dimostrato):
    - e$^{zx}$ e' una soluzione dell'equazione differenziale
    -  x*e$^{zx}$ e' una soluzione dell'equazione differenziale  
    - Quindi $y=c_{1}*e$^{zx}$ + c_{2} * xe^{zx}$ e' la soluzione dell'equazione differenziale dove c$_{1}$, c$_{2}$ $\in$ $\R$   (Si puo' dimostrare anche per questa che vale il teorme del caso y'' + cy = 0)

- **_$\triangle$_ < 0**



