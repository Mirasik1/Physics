
```tikz
\usepackage{tikz}
\begin{document}

\begin{tikzpicture}[scale=2]
    % Axes
    \draw[thick,->] (-1.3,0) -- (4.3,0) node[right, above] {$x$};
    \draw[thick,->] (0,-0.5) -- (0,4.5) node[above] {$y$};
    
    % Phasors
    \draw[thick, red, ->] (0,0) -- (3,4) node[right] {$V_0$} ;
    \draw[thick, red, ->] (0,0) -- (4,3) node[right] {$V_{R0}$};
    \draw[thick, red, ->] (0,0) -- (-1,1) node[above left] {$V_{L0} - V_{C0}$};
    
    % Current phasor
    \draw[thick, cyan, opacity=0.7, ->] (0,0) -- (1,0.75) node[below, xshift=5pt] {$I_0$};
    
    % Projection lines
    \draw[dashed] (-1,2-1) -- (3,4) -- (4,3);
    \draw[dashed] (2,2) ;
    
    % Angle phi

	\pgfmathsetmacro{\theta}{asin(3/5)} % Compute the angle 
	\path (0,0) --++ (\theta:0.5) coordinate (A);
    \draw[thick] (A) arc[start angle={asin(3/5)},end angle={asin(4/5)},radius=0.5];
    \draw[thick] (0.7,0) arc[start angle={0},end angle={asin(3/5)},radius=0.7];
    
    \node at (0.5,0.5) {$\phi$};
    \node at (0.8,0.3) {$\omega t$};

\end{tikzpicture}

\end{document}

```



