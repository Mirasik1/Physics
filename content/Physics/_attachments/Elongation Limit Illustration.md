
```tikz
\usepackage{tikz}
\usepackage{amsmath}

\begin{document}

\begin{tikzpicture}[scale=1.5]

    % Axes
    \draw[thick,->] (0,0) -- (7.5,0) node[below] {Elongation, $\Delta L$};
    \draw[thick,->] (0,0) -- (0,5.5) node[left] {Force, $F$};

    % Elastic Region: Linear F = k * ΔL (Hooke's Law)
    \draw[thick, magenta] (0,0) -- (1.8,3.6) node[sloped, midway, below] {Elastic region};


    % Labels
    \draw[fill=magenta] (2,3.8) circle (1pt) -- ++ (0.5, -0.5) node[below] {Elastic limit};
    \draw[fill=magenta] (7,4.5) circle (1pt) -- ++ (-0.5, -0.5) node[below] {Breaking point};
    \draw[fill=magenta] (1.8,3.6) -- ++ (-0.5, 0.5) node[above] {Elastic region};
    \node[above] at (3.5,4.2) {Plastic region};
    \draw[dashed] (0,5) -- ++ (7,0) node[above] {Ultimate strength};


\end{tikzpicture}

\end{document}

```

