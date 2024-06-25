1. Defina $d\overset{n}{\vdash}d'$ (no hace falta que defina $\vdash$)
2. Defina $L(M)$
3. Defina $H(M)$
4. Defina "$f$ es una funcion del tipo $(n,m,s)$"
5. Defina $(x)$
6. Defina $(x)_{i}$
---
### Defina $d\overset{n}{\vdash}d'$ (no hace falta que defina $\vdash$)
Para $d, d'\in Des$ y $n\geq 0$ escribiremos $d \overset{n}{\vdash} d'$ si existen $d_{1},\dots,d_{n+1} \in Des$ tales que:
$$
\begin{align*}
&d=d_{1}\\
&d'=d_{n+1}\\
&d_{i}\vdash d_{i+1}, &\text{para } i=1,\dots, n
\end{align*}
$$
Notese que $d\overset{0}{\vdash}d'$ $\text{sii}$ $d=d'$. Finalmente definimos
$$
d\overset{*}{\vdash}d'\ \text{sii}\ (\exists n\in \omega) \ d\overset{n}{\vdash}d'
$$
### Defina $L(M)$
Diremos que una palabra $\alpha\in \Sigma^{*}$ es aceptada por $M$ por alcance de estado final cuando
$$
\lfloor q_{0}B\rfloor \overset{*}{\vdash}d, \text{con}\ d \ \text{tal que}\ St(d)\in F.
$$
El lenguaje aceptado por $M$ por alcance de estado final se define de la siguiente manera
$$
L(M) =\{\alpha \in \Sigma^{*}: \alpha \ \text{es aceptada por $M$ pora alcance de estado final} \}
$$
### Defina $H(M)$
Diremos que una palabra $\alpha\in \Sigma^{*}$ es aceptada por $M$ por detención cuando $M$ se detiene partiendo de $\lfloor q_{0}B\rfloor$. El lenguaje aceptado por $M$ por detención se define de la siguiente manera
$$
H(M)=\{\alpha \in\Sigma^{*}: \alpha \ \text{es aceptada por $M$ por detencion}\}
$$
### Defina "$f$ es una funcion del tipo $(n,m,s)$"
Dada una funcion $\Sigma$-mixta $f$, si $n, m\in \omega$ son tales que $D_{f}\subseteq\omega^{n}\times\Sigma^{*m}$ y ademas $I_{f}\subseteq \omega$, entonces diremos que $f$ es de una funcion de tipo $(n,m,\#)$. 
Similarmente si $n, m\in \omega$ son tales que $D_{f}\subseteq\omega^{n}\times\Sigma^{*m}$ y ademas $I_{f}\subseteq \Sigma^{*}$, entonces diremos que $f$ es de una funcion de tipo $(n,m,*)$.
Notese que si $f \neq \emptyset$, entonces hay únicos $n, m\in \omega$ y $s\in \{\#,*\}$ tales que $f$ es una funcion de tipo $(n, m, s)$. Sin embargo $\emptyset$ es una funcion de tipo $(n,m,s)$ cualesquiera sean $n, m\in \omega$ y $s\in \{\#, *\}$.
De esta forma, cuando $f\neq \emptyset$ hablaremos de "el tipo de $f$" para referirnos a esta única terna $(n,m,s)$.
### Defina $(x)$
Dado $x\in N$ usaremos $(x)$ para denotar a la única infinitupla $(s_{1},s_{2},\dots)\in \omega^{[N]}$  tal que 
$$
x=\langle s_1, s_2\dots\rangle=\prod_{i=1}^{\infty}pr(i)^{s_i}
$$
Es decir, $(x)=((x)_{1}, (x)_{2},\dots)$ 
### Defina $(x)_{i}$
Para $i\in N$ usaremos $(x)_{i}$ para denotar a $s_{i}$ de la infinitupla $(x)$.
Es decir, $(x)_i$ es el exponente $pr(i)$ en la (única posible) factorizacion de $x$ como producto de primos.