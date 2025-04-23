
```tikz
\usepackage{tikz}

\begin{document}

\begin{tikzpicture}[scale=2]

    % Source (Hot Reservoir)
    \draw[fill=red!70, draw=black, opacity = 0.5] (-0.8,3) rectangle (0.8,3.5);
    \node at (0,3.25) {\textbf{HEAT SOURCE}};
    \node at (1.2,3.25) {\small at $T_H$};

    % Heat Input Q_H
    \draw[thick, ->, cyan] (0,3) -- (0,2) node[midway,right] {\textbf{$Q_H$}};

    % Heat Engine Circle
    \draw[thick] (0,1.5) circle (0.5);
    \node at (0,1.5) {\textbf{ENGINE}};
    
    % Work Output W
    \draw[thick, ->, cyan] (0.5,1.5) -- (1.5,1.5);
    \draw[fill=green!30, draw=black, opacity = 0.5] (1.5,1.25) rectangle (2,1.75);
    \node at (1.75,1.5) {\textbf{W}};

    % Heat Output Q_C
    \draw[thick, ->, cyan] (0,1) -- (0,0) node[midway,right] {\textbf{$Q_C$}};

    % Sink (Cold Reservoir)
    \draw[fill=blue!70, draw=black, opacity = 0.5] (-0.8,0) rectangle (0.8,-0.5);
    \node at (0,-0.25) {\textbf{COLD SINK}};
    \node at (1.2,-0.25) {\small at $T_C$};


\end{tikzpicture}

\end{document}

```

