1. Defina cuando un conjunto $S\subseteq \omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-recursivo (no hace falta que defina "función $\Sigma$-recursiva")
2. Defina $\langle s_1,s_2\dots\rangle$  
3. Defina "$f$ es una función $\Sigma$-mixta"
4. Defina "familia $\Sigma$-indexada de funciones"
5. Defina $R(f,\mathcal{G})$ 
---
- ##### NOTACIÓN
	Si $\mathcal{G}$ es una familia $\Sigma$-indexada de funciones, entonces para $a \in \Sigma$ escribiremos $\mathcal{G}_a$ en lugar de $\mathcal{G}(a)$
	
- ### Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-recursivo
	Un conjunto sera llamado $S$ sera llamado $\Sigma$-recursivo cuando la función $\chi ^{\omega^{n}\times\Sigma^{*m}}_S$ sea $\Sigma$-recursiva.
- ### Defina $\langle s_1,s_2\dots\rangle$
	Dada una infinitupla $(s_1,s_2\dots)\in\omega^{[N]}$  usaremos $\langle s_1,s_2\dots\rangle$ para denotar al numero  $\prod_{i=1}^{\infty}pr(i)^{s_i}$.
- ### Defina "$f$ es una funcion $\Sigma$-mixta"
	Sea $\Sigma$ un alfabeto finito. Dada una funcion $f$ diremos que es $\Sigma$-mixta si cumple las siguientes propiedades:
		**(M 1)** Existen $n,m\geq0$, tales que $D_f\subseteq\omega^{n}\times\Sigma^{*m}$ 
		**(M 2)** Ya sea $I_f\subseteq\omega$ o $I_f\subseteq\Sigma^*$ 
- ### Defina "familia $\Sigma$-indexada de funciones"
	Dado un alfabeto $\Sigma$, una familia $\Sigma$-indexada de funciones sera una funcion $\mathcal{G}$ tal que $D_{\mathcal{G}}=\Sigma$ y para cada $a\in D_\mathcal{G}$ se tiene que $\mathcal{G}(a)$ es una funcion.
- ### Defina $R(f,\mathcal{G})$
	- #### Recursion primitiva sobre variable numérica con valores alfabéticos
	Supongamos $\Sigma$ es un alfabeto finito. Sean entonces $$
		f: S _{1}\times \dots\times S_{n}\times L _{1}\times\dots\times L_{m}\rightarrow \Sigma^{*}
		$$ con $S_{1}, \dots, S_{n}\subseteq \omega$ y  $L_{1},\dots, L_{m}\subseteq \Sigma^{*}$ conjuntos no vacíos y sea $\mathcal{G}$ una familia $\Sigma$ indexada de funciones tales que 
	$$
	\mathcal{G}_{a}: \omega \times S _{1}\times \dots\times S_{n}\times L _{1}\times\dots\times L_{m}\times\Sigma^{*}\rightarrow \Sigma^{*}
	$$
	para  $a \in \Sigma$. Definamos 
	$$
	R(f,\mathcal{G}): S _{1}\times \dots\times S_{n}\times L _{1}\times\dots\times L_{m}\times \Sigma^{*}\rightarrow \omega
	$$
	de la siguiente manera:
	1. $R(f,\mathcal{G})(\vec{x},\vec{\alpha},\epsilon)=f(\vec{x},\vec{\alpha})$
	2. $R(f,\mathcal{G})(\vec{x},\vec{\alpha},\alpha a)=\mathcal{G}_{a}(R(f,\mathcal{G})(\vec{x},\vec{\alpha},\alpha),\vec{x},\vec{\alpha},\alpha)$
	Diremos que $R(f,\mathcal{G})$ es obtenida por recursion primitiva a partir de $f$ y $\mathcal{G}$
- #### Recursion primitiva sobre variable alfabética con valores alfabéticos
	Supongamos $\Sigma$ es un alfabeto finito. Sea
	$$
	f: S _{1}\times \dots\times S_ n\times L _{1}\times\dots\times L_{m}\rightarrow \omega 
	$$
	con $S_{1}\times \dots\times S_{n}\subseteq\omega$  y  $L_{1}\times\dots\times L_{n} \subseteq\Sigma^{*}$ conjuntos no vacíos y sea $\mathcal{G}$ una familia $\Sigma$-indexada de funciones tal que  
	$$
	\mathcal{G}_{a}: S _{1}\times \dots\times S_{n}\times L _{1}\times\dots\times L_{m} \times \Sigma^{*}\times \Sigma^{*}\rightarrow \omega
	$$
	para cada $a\in\Sigma$. Definimos
	$$
	R(f,\mathcal{G}): S _{1}\times \dots\times S_{n}\times L _{1}\times\dots\times L_{m}\times\Sigma^*\rightarrow \Sigma^{*}
	$$
	de la siguiente manera
	1. $R(f,\mathcal{G})( \vec{x},\vec{\alpha}, \epsilon)=f(\vec{x},\vec{\alpha})$
	2. $R(f,\mathcal{G})(\vec{x},\vec{\alpha},\alpha a)=\mathcal{G}_{a}(\vec{x},\vec{\alpha},\alpha,R(f,\mathcal{G})(\vec{x},\vec{\alpha},\alpha))$
