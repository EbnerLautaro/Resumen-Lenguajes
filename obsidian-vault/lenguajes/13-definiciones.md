# Combo 13
1. Defina $i^{n,m}, E_{\#}^{n,m}$ y $E_{\ast}^{n,m}$
Sean $n,m\in\omega$ , fijos. Definamos 
$$
\begin{aligned}
i^{n,m} &:\omega\times\omega^{n}\times\Sigma^{\ast m}\times\mathrm{Pro}^{\Sigma}\rightarrow\omega \\
E_{\#}^{n,m} &:\omega\times\omega^{n}\times\Sigma^{\ast m}\times\mathrm{Pro}^{\Sigma}\rightarrow\omega^{\lbrack\mathbf{N}]}\\
E_{\ast}^{n,m} &:\omega\times\omega^{n}\times\Sigma^{\ast m}\times\mathrm{Pro}^{\Sigma}\rightarrow\Sigma^{\ast\lbrack\mathbf{N}]}
\end{aligned}
$$
de la siguiente manera
	1. $(i^{n,m}(0,\vec{x},\vec{\alpha},\mathcal{P}),E_{\#}^{n,m}(0,\vec{x},\vec{\alpha},\mathcal{P}),E_{\ast}^{n,m}(0,\vec{x},\vec{\alpha},\mathcal{P}))$ $=$ $(1,(x_{1},...,x_{n},0,...),(\alpha_{1},...,\alpha_{m},\varepsilon,...))$
	2. $(i^{n,m}(t+1,\vec{x},\vec{\alpha},\mathcal{P}),E_{\#}^{n,m}(t+1,\vec{x},\vec{\alpha},\mathcal{P}),E_{\ast}^{n,m}(t+1,\vec{x},\vec{\alpha},\mathcal{P}))$ $=$ $S_{\mathcal{P}}(i^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P}),E_{\#}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P}),E_{\ast}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P}))$
Notese que $$(i^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P}),E_{\#}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P}),E_{\ast}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P}))$$ es la descripcion instantanea que se obtiene luego de correr P una cantidad t de pasos partiendo del estado $$((x_{1},...,x_{n},0,...),(\alpha_{1},...,\alpha_{m},\varepsilon,...))$$

---

2. Defina $E_{\#j}^{n,m}$ y $E_{\ast j}^{n,m}$
Definamos para cada $j\in\mathbf{N}$, funciones 
$$
\begin{aligned}
E_{\#j}^{n,m}	&:\omega\times\omega^{n}\times\Sigma^{\ast m}\times\mathrm{Pro}^{\Sigma}\rightarrow\omega \\
E_{\ast j}^{n,m}	&:\omega\times\omega^{n}\times\Sigma^{\ast m}\times\mathrm{Pro}^{\Sigma}\rightarrow\Sigma^{\ast}
\end{aligned}
$$
de la siguiente manera $$
\begin{aligned}
E_{\#j}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P})	&=j\text{-esima coordenadade }E_{\#}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P})\\
E_{\ast j}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P})	&=j\text{-esimacoordenada de }E_{\ast}^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P})
\end{aligned}
$$

---

3. Defina $Halt^{n,m}$
Dados $n,m\in\omega$, definamos:
$$Halt^{n,m}=\lambda t\vec{x}\vec{\alpha}\mathcal{P}\left[i^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P})=n(\mathcal{P})+1\right]$$
$Halt^{n,m}$ tiene una descripcion muy intuitiva, ya que dado $(t,\vec{x},\vec{\alpha},\mathcal{P})\in\omega\times\omega^{n}\times\Sigma^{\ast m}\times\mathrm{Pro}^{\Sigma}$, tenemos que $Halt^{n,m}(t,\vec{x},\vec{\alpha},\mathcal{P})=1$ si y solo si el programa $\mathcal{P}$ se detiene luego de $t$ pasos partiendo desde el estado $\left\Vert x_{1},...,x_{n},\alpha_{1},...,\alpha_{m}\right\Vert$.

---

4. Defina $T^{n,m}$
Definimos $T^{n,m}=M(Halt^{n,m})$. Notar que para $(\vec{x},\vec{\alpha},\mathcal{P})\in D_{T^{n,m}}$ tenemos que $T^{n,m}(\vec{x},\vec{\alpha},\mathcal{P})=$ cantidad de pasos necesarios para que $\mathcal{P}$ se detenga partiendo de $\left\Vert x_{1},...,x_{n},\alpha_{1},...,\alpha_{m}\right\Vert$.

---

5. Defina $AutoHalt^{\Sigma}$
Cuando $\Sigma\supseteq\Sigma_{p}$, podemos definir $$AutoHalt^{\Sigma}=\lambda\mathcal{P}\left[(\exists t\in\omega)\;Halt^{0,1}(t,\mathcal{P},\mathcal{P})\right]$$Notar que para cada $\mathcal{P}\in\mathrm{Pro}^{\Sigma}$ tenemos que $AutoHalt(\mathcal{P})=1$ sii $\mathcal{P}$ se detiene partiendo del estado $\left\Vert \mathcal{P}\right\Vert$.

---

6. Defina los conjuntos $A$ y $N$
Supongamos que $\Sigma\supseteq\Sigma_{p}$. Entonces definimos los conjuntos $$
\begin{align}
A &=\left\{ \mathcal{P}\in\mathrm{Pro}^{\Sigma}:AutoHalt^{\Sigma}(\mathcal{P})=1\right\} \\

N &=\left\{ \mathcal{P}\in\mathrm{Pro}^{\Sigma}:AutoHalt^{\Sigma}(\mathcal{P})=0\right\} 
\end{align}
$$
