1. Defina cuando una funcion $f: D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\rightarrow \omega$ es llamada $\Sigma$-efectivamente computable y defina "el procedimiento $P$ computa la funcion $f$ " 
 
--- 
Una funcion $\Sigma$-mixta $f:D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\rightarrow \omega$ sera llamada $\Sigma$-efectivamente computable si hay un procedimiento efectivo $P$ tal que
1. El conjunto de datos de entrada de $P$ es $\omega^{n}\times\Sigma^{*m}$
2. El conjunto de datos de salida es $\omega$ 
3. Si $(\vec{x}, \vec{\alpha})\in D_{f}$, entonces $P$ se detiene partiendo de $(\vec{x}, \vec{\alpha})$, dando como dato de salida $f(\vec{x}, \vec{\alpha})$
4. Si $(\vec{x}, \vec{\alpha})\in (\omega^{n}\times\Sigma^{*m}) - D_{f}$, entonces $P$ no se detiene partiendo de $(\vec{x}, \vec{\alpha})$

Análogamente una funcion $\Sigma$-mixta $f:D_{f}\subseteq\omega^{n}\times\Sigma^{*m}\rightarrow \Sigma^{*}$ sera llamada $\Sigma$-efectivamente computable si hay un procedimiento efectivo $P$ tal que
1. El conjunto de datos de entrada de $P$ es $\omega^{n}\times\Sigma^{*m}$
2. El conjunto de datos de salida es $\Sigma^{*}$ 
3. Si $(\vec{x}, \vec{\alpha})\in D_{f}$, entonces $P$ se detiene partiendo de $(\vec{x}, \vec{\alpha})$, dando como dato de salida $f(\vec{x}, \vec{\alpha})$
4. Si $(\vec{x}, \vec{\alpha})\in (\omega^{n}\times\Sigma^{*m}) - D_{f}$, entonces $P$ no se detiene partiendo de $(\vec{x}, \vec{\alpha})$
En ambos casos diremos que $P$ computa a la funcion $f$ 