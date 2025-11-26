# Combo 16 de Definiciones y convenciones notacionales
1. Dado un predicado $P:D_{P}\subseteq\omega\times\Sigma^{\ast}\rightarrow\omega$ , describa que tipo de objeto es y que propiedades debe tener el macro: $$\left[\mathrm{IF}\;P(\mathrm{V}1,\mathrm{W}1)\;\mathrm{GOTO}\;\mathrm{A}1\right]$$

---

Dado un predicado $P:D_{P}\subseteq\omega\times\Sigma^{\ast}\rightarrow\omega$ , el macro $$\left[\mathrm{IF}\;P(\mathrm{V}1,\mathrm{W}1)\;\mathrm{GOTO}\;\mathrm{A}1\right]$$ es de tipo PALABRA y cumple las siguientes propiedades:
1. Las variables oficiales son $\mathrm{V}1,\mathrm{W}1$
2. $\mathrm{A}1$ es el único label oficial
3. Si reemplazamos:
	1. Las variables oficiales (i.e. $\mathrm{V}1,\mathrm{W}1)$ por variables concretas $\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}}$ con $k_{1},j_{1} \in\mathbf{N}$
	2. El label oficial $\mathrm{A}1$ por el label concreto $\mathrm{L}\bar{k}$
	3. Las variables auxiliares por variables concretas (distintas de a dos) y NO pertenecientes a la lista $\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}}$
	4. Los labels auxiliares por labels concretos (distintos de a dos) y ninguno igual a $\mathrm{L}\bar{k}$

Entonces la palabra asi obtenida es un programa de $\mathcal{S}^{\Sigma}$, salvo por la ley de los GOTO respecto de $\mathrm{L}\bar{k}$, que denotaremos con $\left[\mathrm{IF\ }P(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\ \mathrm{GOTO\ L}\bar{k}\right]$ el cual debe tener la siguiente propiedad:
1. Si hacemos correr $\left[\mathrm{IF\ }P(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\ \mathrm{GOTO\ L}\bar{k}\right]$ partiendo de un estado $e$ que le asigne a las variables $\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}}$ valores $x_{1},\alpha_{1}$, entonces independientemente de los valores que les asigne e al resto de las variables se dará que
	1. Si $(x_{1},\alpha_{1})\notin D_{P}$, entonces $\left[\mathrm{IF\ }P(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\ \mathrm{GOTO\ L}\bar{k}\right]$ no se detiene
	2. Si $(x_{1},\alpha_{1})\in D_{P} y P(x_{1},\alpha_{1})=1$, entonces luego de una cantidad finita de pasos, $\left[\mathrm{IF\ }P(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\ \mathrm{GOTO\ L}\bar{k}\right]$ direcciona al label $\mathrm{L}\bar{k}$ quedando en un estado $e^{\prime}$ el cual solo puede diferir de $e$ en los valores que le asigna a las variables que fueron a reemplazar a las variables auxiliares. Al resto de las variables, no las modifica
	3. Si $(x_{1},\alpha_{1})\in D_{P} y y P(x_{1},\alpha_{1})=0$, entonces luego de una cantidad finita de pasos, $\left[\mathrm{IF\ }P(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\ \mathrm{GOTO\ L}\bar{k}\right]$ se detiene quedando en un estado $e^{\prime}$ el cual solo puede diferir de $e$ en los valores que le asigna a las variables que fueron a reemplazar a las variables auxiliares

La palabra $\left[\mathrm{IF\ }P(\mathrm{N}\overline{k_{1}},\mathrm{P}\overline{j_{1}})\ \mathrm{GOTO\ L}\bar{k}\right]$ es llamada la expansion del macro con respecto a la eleccion de variables y labels realizada.