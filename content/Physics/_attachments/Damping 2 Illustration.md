```tikz
\begin{document}

\begin{tikzpicture}[scale=1.5]
    % Axes
    \draw[thick, ->] (0,0) -- (6.5,0) node[right] {$t$};
    \draw[thick, ->] (0,-2) -- (0,2) node[above] {$x$};
    
    % Damping envelope
    \draw[dashed] plot[domain=0:6, samples=100] (\x, {2*exp(-0.3*\x)});
    \draw[dashed] plot[domain=0:6, samples=100] (\x, {-2*exp(-0.3*\x)});
    
    % Damped oscillation
    \draw[thick, red] plot[domain=0:6, samples=200] (\x, {2*exp(-0.3*\x) * cos(3*\x r)});
    
\end{tikzpicture}

\end{document}

```
