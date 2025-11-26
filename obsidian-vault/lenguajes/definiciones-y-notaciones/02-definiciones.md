# Combo 02 de Definiciones y convenciones notacionales
1. Defina $d\overset{n}{\vdash}d'$ (no hace falta definir $\vdash$ )
Para $d,d^{\prime}\in Des$ y $n\geq0$, escribiremos $d\overset{n}{\vdash}d^{\prime}$ si existen d$_{1},...,d_{n+1}\in Des$ tales que 
$$
\begin{aligned}
d&=d_{1} \\  
d^{\prime}&=d_{n+1} \\
d_{i} &\vdash d_{i+1} &\text{ para }i=1,...,n.
\end{aligned}
$$

---

2. Defina $L(M)$
Diremos que una palabra $\alpha\in\Sigma^{\ast}$ es aceptada por $M$ por alcance de estado final cuando $\left\lfloor q_{0}B\alpha\right\rfloor \overset{\ast}{\vdash}d$ , con $d$  tal que $St(d)\in F$. El lenguage aceptado por $M$ por alcance de estado final se define de la siguiente manera $$L(M)=\{\alpha\in\Sigma^{\ast}:\alpha\text{ es aceptada por }M\text{ por alcance de estado final}\}\text{.}$$

---

3. Defina $H(M)$ 
Diremos que una palabra $\alpha\in\Sigma^{\ast}$ es aceptada por $M$ por detencion cuando $M$ se detiene partiendo de $\left\lfloor q_{0}B\alpha\right\rfloor$ . El lenguage aceptado por $M$ por detencion se define de la siguiente manera
$$H(M)=\{\alpha\in\Sigma^{\ast}:\alpha\text{ es aceptada por }M\text{ por detencion}\}$$

--- 

4. Defina “$f$ es una función de tipo $(n,m,s)$”
Dada una funcion $\Sigma -mixta$ $f$,  si $n,m\in\omega$  son tales que $D_{f}\subseteq\omega^{n}\times\Sigma^{\ast m}$ y ademas $I_{f}\subseteq\omega$, entonces diremos que f es una funcion de tipo $(n,m,\#)$. Similarmente si $n,m\in\omega$  son tales que $D_{f}\subseteq\omega^{n}\times\Sigma^{\ast m}$ y ademas $I_{f}\subseteq\Sigma^{\ast}$, entonces diremos que f es una funcion de tipo $(n,m,\ast)$.

--- 

5. Defina $(x)$
Dado $x\in\mathbf{N}$, usaremos $(x)$ para denotar a la unica infinitupla $(s_{1},s_{2},...)\in\omega^{\left[\mathbf{N}\right]}$ tal que 
$$x=\left\langle s_{1},s_{2},...\right\rangle =\underset{i=1}{\overset{\infty}{\Pi}}pr(i)^{s_{i}}$$

--- 

6. Defina $(x)_{i}$
Para $i\in\mathbf{N}$, usaremos $(x)_{i}$ para denotar a $s_{i}$ de dicha infinitupla (la del anterior punto). Se le suele llamar la "bajada $i$-esima de $x$" al numero $(x)_{i}$. La idea de este nombre es que para obtener $(x)_{i}$ debemos bajar el exponente de $pr(i)$ en la factorizacion de $x$.
