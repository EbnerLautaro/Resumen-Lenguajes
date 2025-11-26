# Combo 09
1. Defina “$I$ es una instrucción de $S^{\Sigma}$”
Una instruccion basica de $\mathcal{S}^{\Sigma}$ es una palabra de $(\Sigma\cup\Sigma_{p})^{\ast}$ la cual es de alguna de las siguientes formas:
	1. $\mathrm{N}\bar{k}\leftarrow\mathrm{N}\bar{k}+1$
	2. $\mathrm{N}\bar{k}\leftarrow\mathrm{N}\bar{k}\dot{-}1$
	3. $\mathrm{N}\bar{k}\leftarrow\mathrm{N}\bar{n}$
	4. $\mathrm{N}\bar{k}\leftarrow0$
	5. $\mathrm{P}\bar{k}\leftarrow\mathrm{P}\bar{k}.a$
	6. $\mathrm{P}\bar{k}\leftarrow  ^{\curvearrowright}\mathrm{P}\bar{k}$
	7. $\mathrm{P}\bar{k}\leftarrow\mathrm{P}\bar{n}$
	8. $\mathrm{P}\bar{k}\leftarrow\varepsilon$
	9. $\mathrm{IF}\;\mathrm{N}\bar{k}\neq0\;\mathrm{GOTO}\;\mathrm{L}\bar{n}$
	10. $\mathrm{IF}\;\mathrm{P}\bar{k}\;\mathrm{BEGINS}\;a\;\mathrm{GOTO}\;\mathrm{L}\bar{n}$
	11. $\mathrm{GOTO}\;\mathrm{L}\bar{n}$
	12. $\mathrm{SKIP}$
donde $a\in\Sigma$  y $k,n\in\mathbf{N}$. Una instruccion de $\mathcal{S}^{\Sigma}$ es ya sea una instruccion basica de $\mathcal{S}^{\Sigma}$ o una palabra de la forma $\alpha I$, donde $\alpha\in\{\mathrm{L}\bar{n}:n\in\mathbf{N}\}$ y $I$ es una instruccion basica de $\mathcal{S}^{\Sigma}$.

---

2. Defina “$\mathcal{P}$ es un programa de $S^{\Sigma}$”
Un programa de $\mathcal{S}^{\Sigma}$ es una palabra de la forma $$I_{1}I_{2}...I_{n}$$
donde $n\geq1, I_{1},...,I_{n}\in\mathrm{Ins}^{\Sigma}$ y ademas se cumple la siguiente propiedad, llamada la ley de los $GOTO$,
	1. Para cada $i\in\{1,...,n\}, si \mathrm{GOTOL}\bar{m}$ es un tramo final de $I_{i}$, entonces existe $j\in\{1,...,n\}$ tal que $I_{j}$ tiene label $\mathrm{L}\bar{m}$ 

---

3.  Defina $I_{i}^{\mathcal{P}}$
Definimos $I_{i}^{\mathcal{P}}\in Ins^{\Sigma}\cup\{\varepsilon\}$ como la $i$-ésima instrucción de $\mathcal{P}$. En caso que $i=0$ o $i>n(\mathcal{P})$, se define  $$I_{i}^{\mathcal{P}}=\varepsilon $$ Luego, entonces, $\mathcal{P}=I_{1}^{\mathcal{P}}...I_{n(\mathcal{P})}^{\mathcal{P}}$

 --- 

4. Defina $n(\mathcal{P})$

Definimos $n(\mathcal{P})\in\omega$  como la cantidad de instrucciones del programa $\mathcal{P}$.

---

5. Defina $Bas$

La funcion $Bas:\mathrm{Ins}^{\Sigma}\rightarrow(\Sigma\cup\Sigma_{p})^{\ast}$, está dada por $$Bas(I)=\left\{ \begin{array}{ccl}
J &  & \text{si }I\text{ es de la forma }\mathrm{L}\bar{k}J\text{ con }J\in\mathrm{Ins}^{\Sigma}\\
I &  & \text{caso contrario}
\end{array}\right.$$
