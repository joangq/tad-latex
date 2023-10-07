# TAD • LaTeX

Acá se encuentran archivos de estilo de $\LaTeX$ para poder escribir especificaciones algebraicas de tipos abstractos de datos (TAD) según el formato de [Algoritmos y Estructuras de Datos II (COMP930004).](https://github.com/joangq/exactas/tree/main/COMP930004-AED2) Es decir, de la siguiente manera:

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

En `tad.sty` se encuentra el formato a secas, y en `tad-hyperref.sty` se incluyen modificaciones para que se generen secciones, subsecciones, etc. según sea necesario para documentar los TADs en el índice.
