# Combo 11 de Definiciones y convenciones notacionales
1. Defina $\Psi_{\mathcal{P}}^{n,m,\#}$
Dado $\mathcal{P}\in\mathrm{Pro}^{\Sigma}$, definamos para cada par $n,m\geq0$, la funcion $\Psi_{\mathcal{P}}^{n,m,\#}$ de la siguiente manera:
$$
\begin{array}{l} D_{\Psi_{\mathcal{P}}^{n,m,\#}}=\{(\vec{x},\vec{\alpha})\in\omega^{n}\times\Sigma^{\ast m}:\mathcal{P}\text{ termina, partiendo del}\\ \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\text{estado }\left\Vert x_{1},...,x_{n},\alpha_{1},...,\alpha_{m}\right\Vert \} \end{array}$$

$$\begin{array}{l}
\Psi_{\mathcal{P}}^{n,m,\#}(\vec{x},\vec{\alpha})=\text{valor de }\mathrm{N}1\text{ en el estado obtenido cuando }\mathcal{P}\text{ termina,}\\
\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\text{partiendo de }\left\Vert x_{1},...,x_{n},\alpha_{1},...,\alpha_{m}\right\Vert 
\end{array}
$$

---

2. Defina “$f$ es $\Sigma$-computable” y “$\mathcal{P}$ computa a $f$”
Una funcion $\Sigma$-mixta $f:S\subseteq\omega^{n}\times\Sigma^{\ast m}\rightarrow\omega$  sera llamada $\Sigma$-computable si hay un programa $\mathcal{P}$ de $\mathcal{S}^{\Sigma}$ tal que $f=\Psi_{\mathcal{P}}^{n,m,\#}$. En tal caso diremos que la funcion $f$ es computada por $\mathcal{P}$ y que $\mathcal{P}$ computa a $f$.
Analogamente una funcion $\Sigma$-mixta $f:S\subseteq\omega^{n}\times\Sigma^{\ast m}\rightarrow\Sigma^{\ast}$ sera llamada $\Sigma$-computable si hay un programa $\mathcal{P}$ de $\mathcal{S}^{\Sigma}$ tal que $f=\Psi_{\mathcal{P}}^{n,m,\ast}$. En tal caso diremos que la funcion f es computada por $\mathcal{P}$ y que $\mathcal{P}$ computa a $f$.

---

3. Defina $M^{\leq}(P)$
Supongamos que $\Sigma\neq\emptyset$ . Sea $\leq$ un orden total sobre $\Sigma^{*}$. Sea $P:D_{P}\subseteq\omega^{n}\times\Sigma^{\ast m}\times\Sigma^{\ast}\rightarrow\omega$  un predicado. Cuando $(\vec{x},\vec{\alpha})\in\omega^{n}\times\Sigma^{\ast m}$ es tal que existe al menos un $\alpha\in\Sigma^{\ast}$ tal que $P(\vec{x},\vec{\alpha},\alpha)=1$, usaremos $\min_{\alpha}^{\leq}P(\vec{x},\vec{\alpha},\alpha)$ para denotar al menor $\alpha\in\Sigma^{\ast}$ tal que $P(\vec{x},\vec{\alpha},\alpha)=1$.

Definimos $$\begin{array}{c}
M^{\leq}(P)=\lambda\vec{x}\vec{\alpha}\left[\min_{\alpha}^{\leq}P(\vec{x},\vec{\alpha},\alpha)\right]\end{array}$$
