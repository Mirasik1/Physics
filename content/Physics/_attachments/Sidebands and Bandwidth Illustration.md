```tikz
\usepackage{tikz}

\begin{document}

\begin{tikzpicture}[scale=2]

    % Axes
    \draw[->] (0,0) -- (5,0) node[right] {Frequency};
    \draw[->] (0,0) -- (0,3) node[above] {Signal power};

    % Frequency components
    \draw[red, thick] (1.5,0) -- ++(0,2);
    \draw[red, thick] (3.5,0) -- ++(0,2);
    \draw[red, thick] (2.5,0) -- ++(0,2.5);
    
    % Labels
    \node[below] at (1.5,0) {$(f_c - f_m)$};
    \node[below] at (3.5,0) {$(f_c + f_m)$};
    \node[below] at (2.5,0) {$f_c$};

    % Bandwidth arrow
    \draw[<->] (1.5,-0.5) -- (3.5,-0.5);
    \node[below] at (2.5,-0.5) {bandwidth $2f_m$};

\end{tikzpicture}

\end{document}

```



