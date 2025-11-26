# Combo 10 de Definiciones y convenciones notacionales
Defina relativo al lenguaje $S^{\Sigma}$:
1. ”Estado”
2. ”Descripcion instantanea”
3. $S_{\mathcal{P}}$
4. ”Estado obtenido luego de $t$ pasos, partiendo del estado $(\vec{s},\vec{\sigma})$”
5. ”$P$ se detiene (luego de $t$ pasos), partiendo desde el estado $(\vec{s},\vec{\sigma})$”

--- 

1. Un estado es un par $$(\vec{s},\vec{\sigma})=((s_{1},s_{2},...),(\sigma_{1},\sigma_{2},...))\in\omega^{\left[\mathbf{N}\right]}\times\Sigma^{\ast\left[\mathbf{N}\right]}$$ Si $i\geq1$, entonces diremos que $s_{i}$ es el contenido o valor de la variable $\mathrm{N}\bar{\imath}$ en el estado $(\vec{s},\vec{\sigma})$ y $\sigma_{i}$ es el contenido o valor de la variable $\mathrm{P}\bar{\imath}$ en el estado $(\vec{s},\vec{\sigma})$. Es decir, intuitivamente hablando, un estado es un par de infinituplas que contiene la informacion de que valores tienen alojados las distintas variables.

---

2. Una descripcion instantanea es una terna $(i,\vec{s},\vec{\sigma})$ tal que $(\vec{s},\vec{\sigma})$ es un estado e $i\in\omega$ . Es decir que $\omega\times\omega^{\left[\mathbf{N}\right]}\times\Sigma^{\ast\left[\mathbf{N}\right]}$ es el conjunto formado por todas las descripciones instantaneas.

---

3. Dado un programa $\mathcal{P}$ definiremos la funcion $S_{\mathcal{P}}:\omega\times\omega^{\left[\mathbf{N}\right]}\times\Sigma^{\ast\left[\mathbf{N}\right]}\rightarrow\omega\times\omega^{\left[\mathbf{N}\right]}\times\Sigma^{\ast\left[\mathbf{N}\right]}$ la cual le asignara a una descripcion instantanea $(i,\vec{s},\vec{\sigma})$ la descripcion instantanea sucesora de $(i,\vec{s},\vec{\sigma})$ con respecto a $\mathcal{P}$. Cuando $i\in\{1,...,n(\mathcal{P})\}$, intuitivamente hablando, $S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})$ sera la descripcion instantanea que resulta luego de realizar $I_{i}^{\mathcal{P}}$ estando en el estado $(\vec{s},\vec{\sigma})$. Definicion matematica de $S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})$, segun casos:
	1. Caso $i\notin\{1,...,n(\mathcal{P})\}$. Entonces $$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i,\vec{s},\vec{\sigma})$$ 
	2. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{N}\bar{k}\leftarrow\mathrm{N}\bar{k}\dot{-}1.$ Entonces $$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,(s_{1},...,s_{k-1},s_{k}\dot{-}1,s_{k+1},...),\vec{\sigma})$$ 
	3. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{N}\bar{k}\leftarrow\mathrm{N}\bar{k}+1.$ Entonces $$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,(s_{1},...,s_{k-1},s_{k}+1,s_{k+1},...),\vec{\sigma})$$
	4. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{N}\bar{k}\leftarrow\mathrm{N}\bar{n}$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,(s_{1},...,s_{k-1},s_{n},s_{k+1},...),\vec{\sigma})$$
	5. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{N}\bar{k}\leftarrow0$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,(s_{1},...,s_{k-1},0,s_{k+1},...),\vec{\sigma})$$
	6. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{IF} \mathrm{N}\bar{k} \neq0 \mathrm{GOTO} \mathrm{L}\bar{m}$. Entonces tenemos dos subcasos.
		1. Subcaso a. El valor de $\mathrm{N}\bar{k}$ en $(\vec{s},\vec{\sigma})$ es $0$. Entonces $$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},\vec{\sigma})$$
		2. Subcaso b. El valor de $\mathrm{N}\bar{k} en (\vec{s},\vec{\sigma})$ es no nulo. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(\min\{l:I_{l}^{\mathcal{P}}\ \mathrm{tiene\ label\ L}\bar{m}\},\vec{s},\vec{\sigma})$$
	7. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{P}\bar{k}\leftarrow  ^{\curvearrowright}\mathrm{P}\bar{k}$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},(\sigma_{1},...,\sigma_{k-1},^{\curvearrowright}\sigma_{k},\sigma_{k+1},...))$$
	8. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{P}\bar{k}\leftarrow\mathrm{P}\bar{k}.a$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},(\sigma_{1},...,\sigma_{k-1},\sigma_{k}a,\sigma_{k+1},...))$$
	9. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{P}\bar{k}\leftarrow\mathrm{P}\bar{n}$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},(\sigma_{1},...,\sigma_{k-1},\sigma_{n},\sigma_{k+1},...))$$
	10. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{P}\bar{k}\leftarrow\varepsilon$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},(\sigma_{1},...,\sigma_{k-1},\varepsilon,\sigma_{k+1},...))$$
	11. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{IF}\;\mathrm{P}\bar{k}\;\mathrm{BEGINS}\;a\;\mathrm{GOTO}\;\mathrm{L}\bar{m}$. Entonces tenemos dos subcasos.
		1. Subcaso a. El valor de $\mathrm{P}\bar{k} en (\vec{s},\vec{\sigma})$ comiensa con $a$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(\min\{l:I_{l}^{\mathcal{P}}\ \mathrm{tiene\ label\ L}\bar{m}\},\vec{s},\vec{\sigma})$$
		2. Subcaso b. El valor de $\mathrm{P}\bar{k}$ en $(\vec{s},\vec{\sigma})$ no comienza con $a$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},\vec{\sigma})$$
	12. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{GOTO}\;\mathrm{L}\bar{m}$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(\min\{l:I_{l}^{\mathcal{P}}\ \mathrm{tiene\ label\ L}\bar{m}\},\vec{s},\vec{\sigma})$$
	13. Caso $Bas(I_{i}^{\mathcal{P}})=\mathrm{SKIP}$. Entonces$$S_{\mathcal{P}}(i,\vec{s},\vec{\sigma})=(i+1,\vec{s},\vec{\sigma})$$

---

4. Diremos que$$\overset{t\text{ veces}}{\overbrace{S_{\mathcal{P}}(...S_{\mathcal{P}}(S_{\mathcal{P}}(}}1,\vec{s},\vec{\sigma}))...)$$es la descripcion instantanea obtenida luego de $t$ pasos, partiendo del estado $(\vec{s},\vec{\sigma})$. Si$$\overset{t\text{ veces}}{\overbrace{S_{\mathcal{P}}(...S_{\mathcal{P}}(S_{\mathcal{P}}(}}1,\vec{s},\vec{\sigma}))...)=(j,\vec{u},\vec{\eta})$$diremos que $(\vec{u},\vec{\eta})$ es el estado obtenido luego de t pasos, partiendo del estado $(\vec{s},\vec{\sigma})$.

---

5. Cuando la primer coordenada de$$\overset{t\text{ veces}}{\overbrace{S_{\mathcal{P}}(...S_{\mathcal{P}}(S_{\mathcal{P}}(}}1,\vec{s},\vec{\sigma}))...)$$sea igual a $n(\mathcal{P})+1$, diremos que $\mathcal{P}$ se detiene (luego de $t$ pasos), partiendo desde el estado $(\vec{s},\vec{\sigma}).$ 