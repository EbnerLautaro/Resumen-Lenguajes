# Combo 05
1. Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ es llamado $\Sigma$-efectivamente computable y defina “el procedimiento efectivo $P$ decide la pertenencia a $S$”

--- 

Un conjunto $S\subseteq\omega^{n}\times\Sigma^{\ast m}$ sera llamado $\Sigma$-efectivamente computable cuando la funcion $\chi_{S}^{\omega^{n}\times\Sigma^{\ast m}}$ sea $\Sigma$-efectivamente computable. Notese que $S$ es $\Sigma$-efectivamente computable sii hay un procedimiento efectivo $P$, el cual computa $\chi_{S}^{\omega^{n}\times\Sigma^{\ast m}}$, es decir:
1. El conjunto de datos de entrada de $P$ es $\omega^{n}\times\Sigma^{\ast m}$, siempre termina y da como dato de salida un elemento de $\{0,1\}$.
2. Dado $(\vec{x},\vec{\alpha})\in\omega^{n}\times\Sigma^{\ast m}$, $P$ da como salida al numero $1$ si $(\vec{x},\vec{\alpha})\in S$ y al numero $0$ si $(\vec{x},\vec{\alpha})\notin S$.

Si $P$ es un procedimiento efectivo el cual computa a $\chi_{S}^{\omega^{n}\times\Sigma^{\ast m}}$, diremos que $P$ decide la pertenecia a $S$, con respecto al conjunto $\omega^{n}\times\Sigma^{\ast m}$.
