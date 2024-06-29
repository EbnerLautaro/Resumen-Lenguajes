1. Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-recursivamente enumerable ( no hace falta que defina "funcion $\Sigma$-recursiva")
2. Defina $s^{\leq}$ 
3. Defina $*^{\leq}$ 
4. Defina $\#^{\leq}$
--- 
- ##### *NOTACIÓN*
	Supongamos que $k,l,n,m\in \omega$ y que $F:D_F\subseteq\omega^{k}\times \Sigma^{*l} \rightarrow \omega^{n}\times\Sigma^{*m}$. Supongamos ademas que $n+m\geq 1$. Entonces denotaremos con $F_(i)$ a la funcion $p_{i}^{n,m} \circ F$. 
	Notar que:
	$$
	\begin{align*}
	F _{(i)}: D_F\subseteq\omega^{k}\times \Sigma^{*l} \rightarrow \omega, &\ &\text{para cada $i=1,\dots n$}\\
	F _{(i)}: D_F\subseteq\omega^{k}\times \Sigma^{*l} \rightarrow \Sigma^{*}, &\ &\text{para cada $i=n+1,\dots m$}\\
	\end{align*}
	$$
	Por lo cual cada una de las funciones $F_{(i)}$ son $\Sigma$-mixtas.

- ### Defina cuando un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ es llamado $\Sigma$-recursivamente enumerable ( no hace falta que defina "funcion $\Sigma$-recursiva")
	Diremos que un conjunto $S\subseteq\omega^{n}\times\Sigma^{*m}$ sera llamado $\Sigma$-recursivamente enumerable cuando sea vació o haya una funcion $F:\omega \rightarrow \omega^{n}\times\Sigma^{*m}$ tal que $I_{F}=S$ y $F_{(i)}$ sea $\Sigma$-recursiva para cada $i\in \{1,\dots,(n+m)\}$.
- ### Defina $s^{\leq}$
	Sea $\Sigma$ un alfabeto no vacío y supongamos $\leq$ es un orden total sobre $\Sigma$. Definimos $s^{\leq}:\Sigma^{*}\rightarrow \Sigma^{*}$ de la siguiente forma:
	- $s^{\leq}((a_{n})^{m})=(a_{1})^{m+1}$, para cada $m\geq 0$
	- $s^{\leq}(\alpha a_{i}(a_{n})^{m})=\alpha a_{i+1}(a_{1})^{m}$, cada vez que $\alpha\in \Sigma^{*}, 1\leq i \le n$ y $m\geq 0$
- ### Defina $*^{\leq}$
	Definimos $*^{\leq}(0):\omega\rightarrow \Sigma^{*}$ recursivamente de la siguiente manera
	- $*^{\leq}(0)=\epsilon$
	- $*^{\leq}(i+1)=s^{\leq}(*^{\leq}(i))$
	Es claro entonces que $*^{\leq}$ nos da el $(i+1)$-esimo elemento de la lista, o lo que es lo mismo el $i$-esimo elemento de la lista contando desde el $0$.
- ### Defina $\#^{\leq}$
	Sea $\Sigma$ un alfabeto no vacio y supongamos $\leq$ es un orden total sobre $\Sigma$. Supongamos que $\Sigma=\{a_{1},\dots, a_{n}\}$ con $a_{1} \leq a_{2}\leq \dots \leq a_{n}$. Entonces para cada $\alpha \in \Sigma^{*}-\{\epsilon\}$ hay únicos $k\in\omega$ y $i_{0}, \dots, i_{k} \in \{1,\dots,n\}$ tales que 
	$$\alpha=a _{i_{k}}\dots a _{i_{0}}$$ Notar que $k$ del lema anterior es $|\alpha|-1$ y los números $i_{0}, \dots, i_{k}$ van dando el numero de orden de cada símbolo de $\alpha$ yendo de izquierda a derecha. Por ejemplo si $\Sigma=\{\%,!,@\}$  y $\leq$ es el orden total dado por $\%\leq \ !\leq@$ (aquí $a_{1}=\%, a_{2}=\ !, a_{3}=@$) entonces para la palabra $!\%@\%@$ tenemos $k=4$ y $i_{4}=2,i_{3}=1, i_{2}=3, i_{1}=1, i_{0}=3$.
	Ahora podemos definir la funcion $\#^{\leq}:\Sigma^{*}\rightarrow \omega$ de la siguiente manera
	- $\#^{\leq}(\epsilon)=0$
	-  $\#^{\leq}(a_{i_{k}}\dots a_{i_{0}})=i_{k}n^{k}+\dots+i_{0}n^{0}$

