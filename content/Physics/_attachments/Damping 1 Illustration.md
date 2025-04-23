```tikz
\begin{document}

\begin{tikzpicture}[scale=1.5]
    % Axes
    \draw[thick, ->] (0,0) -- (5,0) node[right] {$t$};
    \draw[thick, ->] (0,-2) -- (0,2) node[above] {$x$};
    
    % Damped oscillation
    \draw[thick, red] plot[domain=0:4, samples=200] (\x, {1.5*cos(0.3*\x r)}) node[right, black] at (2.7, 1.2) {C};
    \draw[thick, red] plot[domain=0:2.1, samples=200] (\x, {.8*cos(1*\x r)+0.7}) node[right, black] at (1.7, 0.8) {B};
    \draw[thick, red] plot[domain=0:4.5, samples=200] (\x, {exp(-0.5*\x^1.4))*1.5*cos(\x*\x r)}) node[left, black] at (1, 0.5) {A};
    
\end{tikzpicture}

\end{document}

```
