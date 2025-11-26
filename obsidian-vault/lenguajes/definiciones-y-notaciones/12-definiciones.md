# Combo 12 de Definiciones y convenciones notacionales
1. Defina cuándo un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-computable, cuándo es llamado $\Sigma$-enumerable y defina “el programa $\mathcal{P}$ enumera a $S$”.

--- 

- Un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ será llamado $\Sigma$-computable cuando la función $\chi_{S}^{\omega^{n}\times\Sigma^{\ast m}}$ sea $\Sigma$-computable.
- Un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ será llamado $\Sigma$-enumerable cuando sea vacío o haya una función $F:\omega\rightarrow\omega^{n}\times\Sigma^{\ast m}$ tal que $I_{F}=S y F_{(i)}$ sea $\Sigma$-computable, para cada $i\in\{1,...,n+m\}$.
- Sea $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ un conjunto no vacio. Entonces son equivalentes:
	1. $S$ es $\Sigma$-enumerable
	2. Hay un programa $\mathcal{P}\in\mathrm{Pro}^{\Sigma}$ tal que:
		1. Para cada $x\in\omega$ , tenemos que $\mathcal{P}$ se detiene partiendo desde el estado $\left\Vert x\right\Vert$  y llega a un estado de la forma $((x_{1},...,x_{n},y_{1},...),(\alpha_{1},...,\alpha_{m},\beta_{1},...))$, donde $(x_{1},...,x_{n},\alpha_{1},...,\alpha_{m})\in S$.
		2. Para cada $(x_{1},...x_{n},\alpha_{1},...,\alpha_{m})\in S$ hay un $x\in\omega$ tal que $\mathcal{P}$ se detiene partiendo desde el estado $\left\Vert x\right\Vert$ y llega a un estado de la forma $((x_{1},...,x_{n},y_{1},...),(\alpha_{1},...,\alpha_{m},\beta_{1},...))$.
	
	En este caso, decimos que el programa $\mathcal{\mathcal{P}}$ descripto enumera a $S$.