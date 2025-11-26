# Combo 08
1. Defina $M(P)$
Sea $\Sigma$  un alfabeto finito y sea $P:D_{P}\subseteq\omega\times\omega^{n}\times\Sigma^{\ast m}\rightarrow\omega$  un predicado. Dado $(\vec{x},\vec{\alpha})\in\omega^{n}\times\Sigma^{\ast m}$, cuando exista al menos un $t\in\omega$  tal que $P(t,\vec{x},\vec{\alpha})=1$, usaremos $\min_{t}P(t,\vec{x},\vec{\alpha})$ para denotar al menor de tales $t^{\prime}s$.
Definamos $$M(P)=\lambda\vec{x}\vec{\alpha}\left[\min\nolimits_{t}P(t,\vec{x},\vec{\alpha})\right]
$$

---
2. Defina $Lt$
Definamos la funcion $Lt:\mathbf{N}\rightarrow\omega$  de la siguiente manera: $$Lt(x)=\left\{ \begin{array}{lll}
\max_{i}\;(x)_{i}\neq0 &  & \text{si }x\neq1\\
0 &  & \text{si }x=1
\end{array}\right.$$

--- 
3. Defina conjunto rectangular
Sea $\Sigma$  un alfabeto finito. Un conjunto $\Sigma$-mixto $S$ es llamado rectangular si es de la forma
$$S_{1}\times...\times S_{n}\times L_{1}\times...\times L_{m}$$ con cada $S_{i}\subseteq\omega$  y cada $L_{i}\subseteq\Sigma^{\ast}$.

---

4. Defina “$S$ es un conjunto de tipo $(n,m)$”
Dado un conjunto $\Sigma$-mixto $S$, si $n,m\in\omega$  son tales que  $S \subseteq\omega^{n}\times\Sigma^{\ast m}$, entonces diremos que $S$ es un conjunto de tipo $(n,m)$.