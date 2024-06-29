1. Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-efectivamente enumerable y defina: "el procedimiento efectivo $\mathbb{P}$ enumera a $S$ "
 ---
 Supongamos que $k, l, n, m \in \omega$ y que $F: D_{F}\subseteq \omega^{k}\times\Sigma^{*l} \to \omega^{n}\times\Sigma^{*m}$. Supongamos ademas que $n+m \geq 1$. Entonces denotaremos con $F_{(i)}$ a la funcion $p_{i}^{n,m}\circ F$.
Notar que 
$$
\begin{align*}
&F_{(i)} : D_{F}\subseteq\omega^{k}\times\Sigma^{*l} \to \omega, \text{ para cada } i=1, \dots, n \\

&F_{(i)} : D_{F}\subseteq\omega^{k}\times\Sigma^{*l} \to \Sigma, \text{ para cada } i=n+1, \dots, n+m 
\end{align*}
$$
Por lo cual cada una de las funciones $F_{(i)}$ son $\Sigma$-mixtas.

Un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ sera llamado $\Sigma$-efectivamente enumerable cuando sea vacio o hay una funcion  $F:\omega\to\omega^{n}\times\Sigma^{*m}$ tal que $I_{F}=S$ y $F_{(i)}$ sea $\Sigma$-efectivamente computable, para cada $i\in \{1,\dots, n+m\}$
