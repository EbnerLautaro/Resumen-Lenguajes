# Combo 06 de Definiciones y convenciones notacionales
1. Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ es llamado $\Sigma$-efectivamente enumerable y defina: "el procedimiento efectivo $P$ enumera a $S$"

---

Un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ sera llamado $\Sigma$-efectivamente enumerable cuando sea vacio o haya una funcion $F:\omega\rightarrow\omega^{n}\times\Sigma^{\ast m}$ tal que $I_{F}=S$ y $F_{(i)}$ sea $\Sigma$-efectivamente computable, para cada $i\in\{1,...,n+m\}$.
#### Lemma
Un conjunto no vacio $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ es $\Sigma$-efectivamente enumerable sii hay un procedimiento efectivo $P$ tal que:
	1. El conjunto de datos de entrada de $P$ es $\omega$
	2. $P$ se detiene para cada $x\in\omega$ 
	3. El conjunto de datos de salida de $P$ es igual a $S$. (Es decir, siempre que $P$ se detiene, da como salida un elemento de S, y para cada elemento $(\vec{x},\vec{\alpha})\in S$, hay un $x\in\omega$  tal que $P$ da como salida a $(\vec{x},\vec{\alpha})$ cuando lo corremos con $x$ como dato de entrada) 

Cuando un procedimiento $P$ cumpla $(1), (2)$ y $(3)$ del lema anterior, diremos que $P$ enumera a $S$.