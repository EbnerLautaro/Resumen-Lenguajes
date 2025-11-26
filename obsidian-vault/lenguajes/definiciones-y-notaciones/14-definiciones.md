# Combo 14 de Definiciones y convenciones notacionales
1. Explique en forma detallada la notación lambda

---
Una expresión es lambdificable con respecto a $\Sigma$ si cumple las siguientes características:
1. Involucra variables numéricas (que se valuaran en números de $\omega$), y variables alfabéticas (que se valuaran en palabras del alfabeto previamente fijado)
	- En cuanto a notación, las numéricas son con letras latinas minúsculas ($x,y,z$) y las alfabéticas con letras griegas minúsculas ($\alpha,\beta,\gamma$)
2. Para ciertas valuaciones de sus variables la expresión puede no estar definida (por ejemplo, $Pred(|\alpha|)$ para $\alpha=\varepsilon$) 
3. Sea $E$ la expresión, los valores que asuma cuando hayan sido asignados los valores de $\omega$  a sus variables numéricas y valores de $\Sigma^{*}$ a sus variables alfabéticas, deberán ser siempre elementos de $O\in\{\omega,\Sigma^{*}\}$ (es decir, no puede tomar valores mixtos) 
4. La expresión puede involucrar lenguaje coloquial castellano (i.e., no únicamente operaciones matemáticas). Por ejemplo, “el menor número primo que es mayor que $x$” 
5. A las expresiones booleanas (como $x=0$), se les considerará que asumen valores de $\{0,1\}\subseteq\omega$
 
Definición: sea $\Sigma$  un alfabeto finito fijo, $E$ una expresión lambdificable respecto a $\Sigma$ y $x_{1},..,x_{n},\alpha_{1},..,\alpha_{m}$ variables distintas tales que las numéricas que ocurren en $E$ están en $\{x_{1},..,x_{n}\}$ y las alfabéticas en $\{\alpha_{1},..,\alpha_{m}\}$, entonces $\lambda x_{1}..x_{n}\alpha_{1}..\alpha_{m}[E]$ denota la función definida por:
1. $D_{\lambda x_{1}..x_{n}\alpha_{1}..\alpha_{m}[E]}=\{(k_{1},..,k_{n},\beta_{1},..,\beta_{m})\in\omega^{n}\times\Sigma^{*m}:E$ está definida cuando asignamos a cada $x_{i}$ el valor $k_{i}$, y a cada $\alpha_{i}$, el valor $\beta_{i}\}$.
2. $\lambda x_{1}..x_{n}\alpha_{1}..\alpha_{m}[E](k_{1},..,k_{n},\beta_{1},..,\beta_{m})=$ valor que asume o representa $E$ cuando asignamos a cada $x_{i}$ el valor $k_{i}$, y a cada $\alpha_{i}$, el valor $\beta_{i}$ .
3. 