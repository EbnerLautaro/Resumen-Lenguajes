# Combo 07
1. Defina cuándo una función $f:D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\to\omega$  es llamada $\Sigma$-Turing computable y defina “la máquina de Turing $M$ computa a la función $f$”

---

Una funcion $f:D_{f}\subseteq\omega^{n}\times\Sigma^{\ast}{}^{m}\rightarrow\omega$ , es llamada $\Sigma$-Turing computable si existe una maquina de Turing con unit, $M=\left(Q,\Sigma,\Gamma,\delta,q_{0},B,\shortmid,F\right)$, tal que:
1. Si $(\vec{x},\vec{\alpha})\in D_{f}$, entonces hay un $p\in Q$ tal que   $$\left\lfloor q_{0}B\shortmid^{x_{1}}B...B\shortmid^{x_{n}}B\alpha_{1}B...B\alpha_{m}\right\rfloor \overset{\ast}{\vdash}\left\lfloor pB\shortmid^{f(\vec{x},\vec{\alpha})}\right\rfloor$$    y $\left\lfloor pB\shortmid^{f(\vec{x},\vec{\alpha})}\right\rfloor \nvdash d$, para cada $d\in Des$.
2. Si $(\vec{x},\vec{\alpha})\in\omega^{n}\times\Sigma^{\ast m}-D_{f}$, entonces $M$ no se detiene partiendo de    $$\left\lfloor q_{0}B\shortmid^{x_{1}}B...B\shortmid^{x_{n}}B\alpha_{1}B...B\alpha_{m}\right\rfloor $$
Cuando $M$ y $f$ cumplan los items $(1)$ y $(2)$ de la definicion anterior, diremos que la funcion $f$ es computada por $M$, y que la máquina de Turing $M$ computa a la función $f$.