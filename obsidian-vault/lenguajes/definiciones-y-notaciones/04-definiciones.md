# Combo 04 de Definiciones y convenciones notacionales
1. Defina cuando una funcion $f : Df\subseteq\omega^{n}\times\Sigma^{*m}\rightarrow\omega$  es llamada $Σ$-efectivamente computable y defina "el procedimiento $P$ computa a la funcion $f$ "

---

Una funcion $\Sigma$-mixta $f : D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\rightarrow\omega$  sera llamada $\Sigma$-efectivamente computable si hay un procedimiento efectivo $P$ tal que:
1. El conjunto de datos de entrada de $P$ es $\omega^{n}\times\Sigma^{*m}$
2. El conjunto de datos de salida de $P$ esta contenido en $ω$ .
3. Si $(\vec{x}\vec{\alpha})\in D_{f}P$ se detiene partiendo de $(\vec{x}\vec{\alpha})$ dando como dato de salida $f(\vec{x}\vec{\alpha})$.
4. Si $(\vec{x}\vec{\alpha})\in(\omega^{n}\times\Sigma^{*m}-D_{f}) P$ no se detiene partiendo de $(\vec{x}\vec{\alpha})$

Diremos que $P$ computa a la funcion $f$.