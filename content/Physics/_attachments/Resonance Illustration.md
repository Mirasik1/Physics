```tikz
\begin{document}

\begin{tikzpicture}[scale=1.5]
    % Axes
    \draw[->] (0,0) -- (3,0) node[below, midway, sloped, yshift=-17pt] {Frequency};
    \draw[->] (0,0) -- (0,3.5) node[above, midway, sloped] {Amplitude};
    
    % Labels
    \node at (0.0,3.7){$A$};
    \node at (3.2,0){$f$};
    \node at (1.5,-0.2) [below] {$f_0$};
    
    % Upper resonance curve (A)
    \draw[red, thick] plot[domain=0.25:0.887, samples=100] (\x, {exp(-2*(\x-1.5)^2)+0.3});   
	\draw[red, thick] plot[domain=2.75:2.113, samples=100] (\x, {exp(-2*(\x-1.5)^2)+0.3});
	
	\draw[red, thick] plot[domain=0.887:2.113, samples=100] (\x, {3*exp(-3*(\x-1.5)^2)-0.2});
	
    \draw[red, thick] plot[domain=0.25:2.75, samples=100] (\x, {exp(-3*(\x-1.5)^2)});
    % Points A and B
    \node[below] at (1.5,3.3) {A};
    \node[below] at (1.5,1.5) {B};
    
    % Tick mark for f0
    \draw[thick] (1.5,0) -- (1.5,-0.2);
\end{tikzpicture}


\end{document}

```
