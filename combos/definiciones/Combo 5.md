1.  Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-efectivamente computable y defina: "el procedimiento efectivo $\mathbb{P}$ decide la pertenencia a $S$ "
---
- ##### *NOTACIÓN*
	Sea $X$ un conjunto cualquiera y sea $S\subseteq X$. Usaremos $\chi_{S}^{X}$  para denotar a la funcion $$\begin{align*} \chi_S^X : X &\to \omega \\ x &\to \begin{cases} 1 & \text{si } x \in S \\0 & \text{si } x \notin S \end{cases} \end{align*}$$

Un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ sera llamado $\Sigma$-efectivamente computable cuando la funcion $\chi^{\omega^{n}\times\Sigma^{*m}}_{S}$ sea $\Sigma$-efectivamente computable. 
Notese que $S$ es $\Sigma$-efectivamente computable si y solo si hay un procedimiento efectivo $\mathbb{P}$ el cual computa a $\chi^{\omega^{n}\times\Sigma^{*m}}_{S}$, es decir
- El conjunto de datos de entrada de $\mathbb{P}$ es $\omega^{n}\times\Sigma^{*m}$, siempre termina y da como dato de salida un elemento de ${0,1}$.
- Dado $(\vec{x},\vec{\alpha})\in \omega^{n}\times\Sigma^{*m}$, $\mathbb{P}$ da como salida al numero $1$ si $(\vec{x},\vec{\alpha})\in S$ y al numero $0$ si $(\vec{x},\vec{\alpha}) \not \in S$
Si $\mathbb{P}$ es un procedimiento efectivo el cual computa a $\chi^{\omega^{n}\times\Sigma^{*m}}_{S}$, diremos que $\mathbb{P}$ decide la pertenencia a $S$, con respecto al conjunto $\omega^{n}\times\Sigma^{*m}$.
