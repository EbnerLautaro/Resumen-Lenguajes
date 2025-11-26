# Combo 03
1. Defina cuándo un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-recursivamente enumerable (no hace falta que defina “función $\Sigma$-recursiva)
Diremos que un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ sera llamado $\Sigma$-recursivamente enumerable cuando sea vacio o haya una funcion $F:\omega\rightarrow\omega^{n}\times\Sigma^{\ast m}$ tal que $I_{F}=S$ y $F_{(i)}$ sea $\Sigma$-recursiva, para cada $i\in\{1,...,n+m\}$.

---

2. Defina $s^{\leq}$
Sea $\Sigma$  un alfabeto no vacio y supongamos $\leq$  es un orden total sobre $\Sigma$. Definimos s$^{\leq}:\Sigma^{\ast}\rightarrow\Sigma^{\ast}$ de la siguiente manera:
	1. $s^{\leq}((a_{n})^{m})=(a_{1})^{m+1}$, para cada $m\geq0$
	2. $s^{\leq}(\alpha a_{i}(a_{n})^{m})=\alpha a_{i+1}(a_{1})^{m}$, cada vez que $\alpha\in\Sigma^{\ast}, 1\leq i<n$ y $m\geq0$

---
3. Defina $*^{\leq}$

Sea $\Sigma$  un alfabeto no vacio y supongamos $\leq$  es un orden total sobre $\Sigma$ . Definamos $\ast^{\leq}:\omega\rightarrow\Sigma^{\ast}$ recursivamente de la siguiente manera:
	1. $\ast^{\leq}(0)=\varepsilon$
	2. $\ast^{\leq}(i+1)=s^{\leq}(\ast^{\leq}(i))$

---

4. Defina $\#^{\leq}$
Sea $\Sigma$  un alfabeto no vacio y supongamos $\leq$  es un orden total sobre $\Sigma$ . Definimos la funcion $\#^{\leq}$ de la siguiente manera:
$$
\begin{array}[t]{rll}
\#^{\leq}:\Sigma^{\ast} & \rightarrow & \omega\\
\varepsilon & \rightarrow & 0\\
a_{i_{k}} \dots a_{i_{0}} & \rightarrow & i_{k}n^{k}+\dots+i_{0}n^{0}
\end{array}
$$