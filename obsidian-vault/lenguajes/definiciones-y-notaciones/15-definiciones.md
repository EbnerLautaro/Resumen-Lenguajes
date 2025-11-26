# Combo 15 de Definiciones y convenciones notacionales
1. Dada una función $f:D_{f}\subseteq\omega\times\Sigma^{*}\to\omega$, describa qué tipo de objeto es y qué propiedades debe tener el macro:
$$\left[\mathrm{V}2\leftarrow f(\mathrm{V}1,\mathrm{W}1)\right]$$

---

Dada una función $f:D_{f}\subseteq\omega\times\Sigma^{*}\to\omega$, usaremos $$\left[\mathrm{V}2\leftarrow f(\mathrm{V}1,\mathrm{W}1)\right]$$ para denotar un macro $M$ el cual cumpla las siguientes propiedades:
1. Las variables oficiales de $M$ son $\mathrm{V}1,\mathrm{V}2,\mathrm{W}1$
2. $M$ no tiene labels oficiales
3. Si reemplazamos:
	1. las variables oficiales de $M$ (i.e.$\mathrm{V}1,\mathrm{V}2,\mathrm{W}1$) por variables concretas $\mathrm{N}\overline{k_{1}},\mathrm{N}\overline{k_{2}},\mathrm{P}\overline{j_{1}}$ (elegidas libremente, es decir los números $k_{1},k_{2},j_{1}$son cualesquiera)
	2. Las variables auxiliares de $M$ por variables concretas (distintas de a dos) y NO pertenecientes a la lista $\mathrm{N}\overline{k_{1}},\mathrm{N}\overline{k_{2}},\mathrm{P}\overline{j_{1}}$
	3. Los labels auxiliares de $M$ por labels concretos (distintos de a dos) 

	Entonces la palabra asi obtenida es un programa de $\mathcal{S}^{\Sigma}$ (por lo tanto, el TIPO de objeto es PALABRA) que denotaremos con $$\left[\mathrm{N}\overline{k_{2}}\leftarrow f(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\right]$$ el cual debe tener la siguiente propiedad:

Si hacemos correr $\left[\mathrm{N}\overline{k_{2}}\leftarrow f(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\right]$ partiendo de un estado e que le asigne a las variables $\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}}$ valores $x_{1},\alpha_{1}$, entonces independientemente de los valores que les asigne $e$ al resto de las variables (incluidas las que fueron a reemplazar a las variables auxiliares de $M$) se dará que
	1. Si $(x_{1},\alpha_{1})\notin D_{f}$, entonces $\left[\mathrm{N}\overline{k_{2}}\leftarrow f(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\right]$ no se detiene
	2. Si $(x_{1},\alpha_{1})\in D_{f}$, entonces $\left[\mathrm{N}\overline{k_{2}}\leftarrow f(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\right]$se detiene (i.e. intenta realizar la siguiente a su última instrucción) y llega a un estado $e^{\prime}$ el cual cumple:
		1. $e^{\prime}$ le asigna a $\mathrm{N}\overline{k_{2}}$ el valor $f(x_{1},\alpha_{1})$
		2. $e^{\prime}$ solo puede diferir de e en los valores que le asigna a $\mathrm{N}\overline{k_{2}}$ o a las variables que fueron a reemplazar a las variables auxiliares de $M$. Al resto de las variables, incluidas $\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}}$ no las modifica (salvo en el caso de que alguna $\mathrm{N}\overline{k_{i}}$ sea la variable $\mathrm{N}\overline{k_{2}}$, situación en la cual el valor final de la variable $\mathrm{N}\overline{k_{i}}$ será $f(x_{1},\alpha_{1})$). 