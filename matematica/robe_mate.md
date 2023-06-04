# Equazione differenziale

- Equazioni in cui l'incognita è una funzione e in cui sono presenti **1 o più derivate** della funzione incognita

- $f'(x) + f(x) = x$ $\to$ risolverla significa trovare la funzione che soddisfano l'equazione
- Si può riscriverlo con la $y$ per averla più compatta $y = f(x)$
- es: $y''' = y'' = 9x$

- Si può classificare l'equazione differenziale per:
  - ***ordine***: il massimo ordine di derivazione che compare (es: y''' + y' = x $\to$ è 3 perché il massimo grado derivazione è la derivata terza)
  
 
 - ## L'equazioni differenziali "elementari":
   - $y = f(x)$ dove $y$ può essere di qualsiasi ordine
   - L'idea è quello di integrale entrambe le parti fino ad arrivare y
   - Es:
     - $y'' = f(x)$
     - $\int{y''} = \int{f(x) } dx$
     - Sia $F(x) + c1 = \int{f(x) }dx$
     - $y' = \int{F(x) + c1 } dx$
     - $y = \int{F(x)} + c1 * x + c2 dx$
 
- Problema di Cauchy:
- equazione differenziali con delle condizioni generali $\to$ queste mi consentono di stabilire una soluzione specifica tra tutte le infiti soluzioni (stabilisco le c)

- ## L'equazione variabili separabili
  - $y' = f(x) * g(y)$
  - Es:
    - $y' = y * x^{2}$ dove $x^2$ è $f(x)$ e $y$ è $g(x)$
  -  Per risolverlo si sposta tutte le $y$ da una parte
  -  Proof:
    -  $y' = f(x) * g(y)$
    -  $\frac{y'}{g(y)} = f(x)$ ***assumendo che g(y) $\neq$ 0***
    -  la $y'$ è la $derivata$ quindi possiamo scriverlo come $\frac{dy}{dx}$
    -  $\frac{dy}{g(y)} = f(x) dx $
    -  Qui integro da entrambe le parti e da qui si può risolverlo
    -  $\int{\frac{dy}{g(y)}} = \int{f(x) dx} $
    -  Risolto ciò avremo $2$ c che lo chiamo c1 e c2, ed essendo che sono costanti posso sommarli e lo chiamo $c$
    -  Alla fine dobbiamo verificare se $g(y) = 0$ che era una soluzione che abbiamo escluso all'inizio e se l'uguaglianza rimane vera, allora g(y) = 0 è soluzione (generalmente è vera per esempio in questo caso, la sappaimo che se g(y) = 0 allora g(y) * f(x) = 0 e quindi dobbiamo verificare che $y'$ sia 0)

- ## Equazioni differenziali lineari primo ordine
 - $y' + a(x)*y = f(x)$ dove a(x) $\neq 0$ altrimenti diventerebbe una "elementare"  
    - Se f(x) è 0, si può risolverla usando variabili separabili portando $a(x)*y$ dall'altra parte
 - Modo risoluzione:
   - Si calcola il ***fattore integrante***
    - trovo una primitiva di a(x) $\to$ $A(x) = \int{a(x)}$
    - Moltiplico da entrambi i membri per $e^{A(x)}$
  - $e^{A(x)} * y' + e^{A(x)} * a(x)*y = e^{A(x)} * f(x)$
  - Ma si nota che $e^{A(x)} * y' + e^{A(x)} * a(x)*y =$ Derivata di ($y * e^{A(x)}$) dove indico la derivata con D[...]
  - $D[y * e^{A(x)}] = e^{A(x)} * f(x)$
  - Ora integro da entrambe le parti e la derivata si "semplifica"
  - $y * e^{A(x)} = \int{e^{A(x)} * f(x)}$
  - Ora so risolverlo perché ho y a sinistra e le x a destra
