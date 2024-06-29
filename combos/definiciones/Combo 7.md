1. Defina cuando una funcion $f: D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\to \omega$ es llamada $\Sigma$-Turing computable y defina "la maquina de Turing $M$ computa a la funcion $f$ "  
---
- ##### *NOTACIÓN*
	Para poder computar funciones mixtas con una maquina de Turing necesitaremos un símbolo para representar números sobre la cinta. Llamaremos a este símbolo unit y lo denotaremos con $\shortmid$. Mas formalmente una maquina de Turing con unit es una 8-tupla $M=(Q,\Sigma, \Gamma, \delta_{0}, B, \shortmid, F)$ tal que   $(Q,\Sigma, \Gamma, \delta_{0}, B, F)$ es una maquina de Turing y $\shortmid$ es un símbolo distinguido perteneciente a $\Gamma - (\{B\}\cup \Sigma)$.

Diremos que una funcion $f: D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\to \omega$  es $\Sigma$-Turing computable si existe una maquina de Turing con unit, $M=(Q,\Sigma, \Gamma, \delta_{0}, B, \shortmid, F)$ tal que
1. Si $(\vec{x},\vec{\alpha})\in D_{f}$, entonces hay un $p\in Q$ tal que:
   $$\lfloor q _{0}B \shortmid^{x_{1}}B\dots B \shortmid^{x _{n}}B\alpha_{1}B\dots \alpha_{m}\rfloor \overset{*}{\vdash} \lfloor p B \shortmid^{f(\vec{x},\vec{\alpha})} \rfloor$$
   y $\lfloor p B \shortmid^{f(\vec{x},\vec{\alpha})} \rfloor\not \vdash d$ para cada $d \in Des$
2.    Si $(\vec{x},\vec{\alpha})\in (\omega^{n}\times\Sigma^{*m}) - D_{f}$, entonces $M$ no se detiene partiendo desde $$\lfloor q _{0}B \shortmid^{x_{1}}B\dots B \shortmid^{x _{n}}B\alpha_{1}B\dots \alpha_{m}\rfloor $$
Cuando $M$ y $f$ cumplan los dos items de la definición anterior, diremos que la funcion $f$ es computada por $M$.