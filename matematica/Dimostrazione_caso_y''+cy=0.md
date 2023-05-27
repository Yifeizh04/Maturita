# Risoluzione  **_y'' + cy = 0_**

Abbiamo una equazione differenziale:
_**f(x)=a*y''+b*y = 0**_  con a $\neq$ 0 altrimenti non sarebbe un'equazione differenziale $\to$ _**f(x)= b*y = 0**_ $\to$ equazione di primo grado

Assunto ciò, possiamo dividere da entrambe le parti per **_a_**:

_**y''+$\frac{b*y}{a}$=0**_

Definiamo $\frac{b}{a}$ come **_c_** per comodita

Quindi alla fine abbiamo:

_**y''+c*y=0**_

## **Teorema:**

Sia **_f(x)_** e **_g(x)_** soluzione dell'equazione differenziale _**y''+c*y=0**_ tale che **_$\frac{f(x)}{g(x)}$_** $\neq$ k con k $\in$ $\mathbb{R}$, allora **c$_{1}$f(x) + c$_{2}$g(x)** e' una soluzione. In altre parole valgono queste equazioni:
- **_y = f(x)_**
- **_y = g(x)_**
- **_y = c$_{1}$f(x) + c$_{2}$g(x)_**

#### **Definizione**

**_$\frac{f(x)}{g(x)}$ $\neq$ k $\to$ f(x) e g(x) sono linearmente indipendenti_**


### **Perché **_$\frac{f(x)}{g(x)}$_** $\neq$ k con k $\in$ $\mathbb{R}$?**

Se il rapporto fosse un valore costante, cioe' **_$\frac{f(x)}{g(x)}$_** = k, allora possiamo riscrivere **_f(x) = g(x) * k_**.
 Quindi prendendo l'equazione di prima **_c$_{1}$f(x) + c$_{2}$g(x)_**, si avrebbe **_c$_{1}$g(x)*k + c$_{2}$g(x)_** e quindi solo **_g(x)_** sarebbe soluzione e non anche **_f(x)_**.

 ## Dimostrazione che **_c$_{1}$f(x) + c$_{2}$g(x)_** è una soluzione:

 Siamo in questa situazione (cose che sappiamo che sono vere):

- _**y''+c*y=0**_
- _**y = f(x)**_
- _**y = g(x)**_

Essendo che f(x) e g(x) sono delle soluzioni, possiamo scrivere le ultime due uguaglianze, ma se ciò è vero, possiamo sostituire le due funzioni nella prima equazione $\to$ l'uguaglianza sappiamo che vale quindi possiamo sostituire:


- _**f(x)''+c*f(x)=0**_

- _**g(x)''+c*g(x)=0**_

Fatto ciò non ci rimane altro che dimostrare che anche **_c$_{1}$f(x) + c$_{2}$g(x)_** e' una soluzione $\to$ **_y = c$_{1}$f(x) + c$_{2}$g(x)_** $\to$ se lo sostituisco in _**y''+c*y=0**_, vale l'uguaglianza.

**_y_** lo conosciamo, dobbiamo ricavare solo **_y''_**:

**_y'' = c$_{1}$f''(x) + c$_{2}$g''(x)_** $\to$ cio' e' vero perché c$_{1}$ e c$_{2}$ sono delle costanti quindi possiamo tirarlo fuori quando derivo $\to$ derivo solo le funzioni per due volte 

Sostituisco con cio' che ho trovato:

**y'' + c*y = _c$_{1}$f''(x) + c$_{2}$g''(x) + c * (c$_{1}$f(x) + c$_{2}$g(x))_**

Qui possiamo raccogliere molte cose:
**_c$_{1}$f''(x) + c$_{2}$g''(x) + c*c$_{1}$f(x) + c*c$_{2}$g(x)_** $\to$ **_c$_{1}$ * (f''(x) * c * f(x)) + c$_{2}$ * (g''(x) + c*g(x))_**

Ma per le condizioni dette all'inizio, **_f''(x) * c * f(x)_ = 0** e **_g''(x) * c * g(x)_ = 0** quindi:

**_c$_{1}$ * 0 + c$_{2}$ * 0 = 0 + 0 = 0_**

Ciò dimostra l'uguaglianza iniziale ovvero **_y'' = y + c * y_ = 0** quindi l'equazione descritta e' una soluzione


