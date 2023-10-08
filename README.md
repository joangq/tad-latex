# TAD • LaTeX

Acá se encuentran archivos de estilo de $\LaTeX$ para poder escribir especificaciones algebraicas de tipos abstractos de datos (TAD). 

El formato de [Algoritmos y Estructuras de Datos II (COMP930004).](https://github.com/joangq/exactas/tree/main/COMP930004-AED2) es el siguiente:

---

$$
\begin{aligned}
& \textbf{TAD Secuencia(T)} \\
& \qquad \textbf{géneros: }\text{secu} \\
& \qquad \textbf{observadores básicos} \\
& \qquad\qquad \text{vacía?} : \text{secu}(\alpha) \longrightarrow \text{bool} \\
& \qquad\qquad \text{fin} : \text{secu}(\alpha)\textit{ s} \longrightarrow \alpha \\{\neg \text{vacía?}(s)\\}\\
& \qquad\qquad \vdots \\
& \qquad \textbf{generadores} \\
& \qquad\qquad \langle\rangle : \longrightarrow \text{secu}(\alpha)\\
& \qquad\qquad \textunderscore\bullet\textunderscore : \alpha \times \text{secu}(\alpha) \longrightarrow \text{secu}(\alpha) \\
& \qquad\qquad \vdots \\
& \qquad \textbf{otras operaciones} \\
& \qquad\qquad \textunderscore\texttt{\\&}\textunderscore : \text{secu}(\alpha) \times \text{secu}(\alpha) \longrightarrow \text{secu}(\alpha) \\
& \qquad\qquad \vdots \\
& \qquad \textbf{axiomas} \\
& \qquad\qquad s \texttt{ \\& } t \equiv \textbf{if } \text{vacía?}(s) \textbf{ then } t \textbf{ else } \text{prim}(s) \bullet (\text{fin}(s)\texttt{ \\& } t) \\
& \qquad\qquad \vdots \\
\end{aligned}
$$

---

Sin embargo, en [el nuevo plan](https://computacion.dc.uba.ar/plan-de-estudios-2023/) el formato propuesto es el siguiente:

---

$$
\begin{aligned}
& \textbf{TAD Par $\langle$A, B$\rangle$} \\
& \qquad \textbf{obs }\text{first} : \text{A} \\
& \qquad \textbf{obs }\text{second} : \text{B} \\
& \qquad \textbf{obs }\text{select}(\textbf{in }x : \texttt{int}) \to res : \text{A} \cup \text{B} \\
& \\
& \qquad \textbf{proc }\text{sumarYdividir}(\textbf{in }t : \texttt{par$\langle$int,int$\rangle$}, \textbf{in }x : \texttt{int}) \to res : \texttt{int}\\
& \qquad\qquad \textbf{requiere } x \neq 0\\
& \qquad\qquad \textbf{asegura } res == \frac{\text{t}.first + \text{t}.second}{x}\\
& \\
\end{aligned}
$$

---

En `tad.sty` se encuentra el formato a secas, y en `tad-hyperref.sty` se incluyen modificaciones para que se generen secciones, subsecciones, etc. según sea necesario para documentar los TADs en el índice.
En `tadv2.sty` se encuentra el formato nuevo.
