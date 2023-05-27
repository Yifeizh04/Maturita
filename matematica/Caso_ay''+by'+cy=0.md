# Risoluzione  **_ay'' + by' + cy = 0_**

Si assume che **$a$ $\neq$ 0** altrimenti si ha un equazione differenziale di primo ordine. Assunto cio', si puo' dividere da tutte le parti per **_a_** $\to$  **_y'' + $\frac{by'}{a}$ + $\frac{cy'}{a}$ = 0_**

Per comodita' chiamiamo **_m = $\frac{b}{a}$_** ed **_n = $\frac{c}{a}$_**. Quindi si ha questa equazione differenziale $\to$ **_y'' + m * y' + n * y = 0_**

Per risolvere cio', si suppone che **_y = e$^{kx}$_** sia una soluzione.

Quindi si avra' che:
- **_y = e$^{kx}$_**
- **_y' = k * e$^{kx}$_**
- **_y'' = k$^{2}$ * e$^{kx}$_**

Avendo cio', si riscrive l'equazione di prima sostituendo questi valori che conosciamo:

**_y'' + m * y' + n * y = 0_**

**_k$^{2}$ * e$^{kx}$ + m * k * e$^{kx}$ + n * e$^{kx}$ = 0_**

Qui si puo' raccogliere **_e$^{kx}$_** $\to$  **_e$^{kx}$ * (k$^{2}$ + m * k + n) = 0_**

Per la legge dell'annullamento del prodotto, questa quantita' **_e$^{kx}$ * (k$^{2}$ + n * k + m)_** e' 0 $\iff$ **_k$^{2}$ + m * k + n = 0_**     
(**_e$^{kx}$ > 0 $\forall$ x $\in$ $\R$  $\to$ per forza di cose deve essere il secondo membro a far 0_**)

### **Definizioni:**

**_(k$^{2}$ + m * k + n) $\to$ equazione caratteristica dell'equazione differenziale_**

**_$\triangle$ = m$^{2}$ - 4n $\to$ discriminante dell'equazione differenziale (ci dice gia' che casistica/come dobbiamo risolverlo)_**

Abbiamo 3 casi:
- **_$\triangle$_ > 0** 
  - Si hanno **2** soluzioni chiamate k$_{1}$ e k$_{2}$ dove sono distinte e k$_{1}$, k$_{2}$ $\in$ $\R$. Quindi si puo' affermare (non ancora dimostrato):
      - **_(Per comodita' chiamo i = k$_{1}$, j = k$_{2}$)_**
      - e$^{ix}$ e' una soluzione dell'equazione differenziale
    -  e$^{-ix}$ e' una soluzione dell'equazione differenziale  
    -  Quindi **_y=c$_{1}$*e$^{ix}$ + c$_{2}$*e$^{-jx}$_** e' la soluzione dell'equazione differenziale dove c$_{1}$, c$_{2}$ $\in$ $\R$   (Si puo' dimostrare anche per questa che vale il teorme del caso y'' + cy = 0)
    
- **_$\triangle$_ = 0** 
  - Si hanno **2** soluzioni chiamate k$_{1}$ e k$_{2}$ che sono coincidenti k$_{1}$ = k$_{2}$ = z e z $\in$ $\R$. Quindi si puo' affermare (non ancora dimostrato):
    - e$^{zx}$ e' una soluzione dell'equazione differenziale
    -  x*e$^{zx}$ e' una soluzione dell'equazione differenziale  
    - Quindi **_y=c$_{1}$*e$^{zx}$ + c$_{2}$*xe$^{zx}$_** e' la soluzione dell'equazione differenziale dove c$_{1}$, c$_{2}$ $\in$ $\R$   (Si puo' dimostrare anche per questa che vale il teorme del caso y'' + cy = 0)

- **_$\triangle$_ < 0**



