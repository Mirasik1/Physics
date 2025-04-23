```tikz
\begin{document}

\begin{tikzpicture}[scale=2/3]


	\pgfmathsetmacro{\startx}{-7}
	\pgfmathsetmacro{\radius}{2}

    % Medium separation
    \draw[red, opacity=0.3] (\startx + \radius,-6.5) -- (\startx + \radius,6.5);
    \draw[red] (\startx,-6.5) -- (\startx,6.5);
    \draw[->, thick] (\startx - 3, 0) -- (\startx,0) node[midway, above] {$\vec V$};
    \draw[-, thick] (\startx, 0.5) -- (\startx + \radius,0.5) node[midway, above] {$V\Delta t$};

	\foreach \x in {-1,0, 1, 2, 3} {
		\draw[gray, dashed, thick] (\startx, 2*\x) arc[start angle=90, delta angle = -180, radius=\radius];
    }



	\draw[gray, dashed, thick] (4,0) circle (2);
	\draw[gray, dashed, thick] (3.5,1.93649) circle (2);
	\draw[gray, dashed, thick] (2.125, 3.38886) circle (2);
	\draw[gray, dashed, thick] (3.5,-1.93649) circle (2);
	\draw[gray, dashed, thick] (2.125, -3.38886) circle (2);

	\draw[red, fill=white] (0, \radius*2) arc[start angle=90, delta angle = -180, radius=\radius*2];
	\draw[red, opacity=0.3] (0, \radius*3) arc[start angle=90, delta angle = -180, radius=\radius * 3] ;

	\draw[->, thick] (0, 0) -- (4, 0) node[midway, above] {$\vec V$};
    \draw[-, thick] (3.96863, 0.5) -- (5.97913,0.5) node[midway, above] {$V\Delta t$};


\end{tikzpicture}

\end{document}


```
