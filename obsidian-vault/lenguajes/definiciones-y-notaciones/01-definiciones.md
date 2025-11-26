# Combo 01 de Definiciones y convenciones notacionales
1. Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $Σ-recursivo$ (no hace falta que defina ”funcion $Σ-recursiva$”)
Un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ $\Sigma-recursivo$ si y solo si su función característica: $\chi_{S}^{\omega^{n}\times\Sigma^{*m}}$ es $\Sigma-recursiva$

---

2. Defina $\langle s_{1},s_{2},\dots,\rangle$ 
Usamos $\langle s_{1},s_{2},\dots\rangle$  para denotar al numero $\prod_{i=1}^{\infty}Pr(i)^{s_{i}}$

---

3. Definicion de funcion $\Sigma-mixta$ 
Sea $\Sigma$  un alfabeto finito. Dada una funcion $f$, diremos que $f$ es $\Sigma -mixta$ si cumple las siguientes propiedades
	1. Existen $n,m\geq0$, tales que $D_{f}\subseteq\omega^{n}\times\Sigma^{\ast m}$
	2. Ya sea $I_{f}\subseteq\omega$  o $I_{f}\subseteq\Sigma^{\ast}$ 

---

4. Defina ”familia Σ -_indexada_ de funciones”
Dado un alfabeto $\Sigma$ , una familia $\Sigma -indexada$ de funciones sera una funcion $\mathcal{G}$ tal que $D_{\mathcal{G}}=\Sigma$  y para cada $a$ $\in D_{\mathcal{G}}$ se tiene que $\mathcal{G}(a)$ es una funcion. 

--- 

5. Defina $R ( f , G )$
Sea
$$f:S_{1}\times...\times S_{n}\times L_{1}\times...\times L_{m}\rightarrow\omega $$
con $S_{1},...,S_{n}\subseteq\omega$  y $L_{1},...,L_{m}\subseteq\Sigma^{\ast}$ conjuntos no vacios y sea $\mathcal{G}$ una familia $\Sigma -indexada$ de funciones tal que
$$\mathcal{G}_{a}:\omega\times S_{1}\times...\times S_{n}\times L_{1}\times...\times L_{m}\times\Sigma^{\ast}\rightarrow\omega$$
para cada $a\in\Sigma$. Definamos 
$$R(f,\mathcal{G}):S_{1}\times...\times S_{n}\times L_{1}\times...\times L_{m}\times\Sigma^{\ast}\rightarrow\omega $$ de la siguiente manera
	1. $R(f,\mathcal{G})(\vec{x},\vec{\alpha},\varepsilon)=f(\vec{x},\vec{\alpha})$
	2. $R(f,\mathcal{G})(\vec{x},\vec{\alpha},\alpha a)=\mathcal{G}_{a}(R(f,\mathcal{G})(\vec{x},\vec{\alpha},\alpha),\vec{x},\vec{\alpha},\alpha)$
Diremos que $R(f,\mathcal{G})$ es obtenida por recursion primitiva a partir de $f$ y $\mathcal{G}$.