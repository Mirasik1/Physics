```tikz
\begin{document}

\begin{tikzpicture}
    % Labels
    \draw[->] (1.75*pi,4.5) -- (1.75*pi,1.5) node[yshift=-15pt] {Time};
    \node[left] at (-0.5, 4.3) {Pulses far apart,};
    \node[left] at (-0.5, 4) {approaching};
    \node[left] at (-0.5, 2.3) {Pulses overlap};
    \node[left] at (-0.5, 2) {precisely};
    \node[left] at (-0.5, 0.3) {Pulses far apart,};
    \node[left] at (-0.5, 0) {receding};
    
    % First row: Approaching pulses
    \draw[thick] (0,4) -- (0.25*pi,4);
    \draw[thick, domain=0.25*pi:0.5*pi, samples=100] plot (\x, {sin(deg(-4*\x))/2+4});
    \draw[->, thick] (0.5*pi,4.6) -- (0.625*pi,4.6);
    \draw[thick] (0.5*pi,4) -- (pi,4);
    \draw[thick, domain=pi:1.25*pi, samples=100] plot (\x, {sin(deg(-4*\x))/2+4});
    \draw[<-, thick] (0.875*pi,3.4) -- (1*pi,3.4);
    \draw[thick] (1.25*pi,4) -- (1.5*pi,4);
    
	\draw[thick] (2*pi,4) -- (2.25*pi,4);
    \draw[thick, domain=2.25*pi:2.5*pi, samples=100] plot (\x, {sin(deg(-4*\x))/2+4});
    \draw[->, thick] (2.5*pi,4.6) -- (2.625*pi,4.6);
    \draw[thick] (2.5*pi,4) -- (3*pi,4);
    \draw[thick, domain=3*pi:3.25*pi, samples=100] plot (\x, {sin(deg(4*\x))/2+4});
    \draw[<-, thick] (2.875*pi,4.6) -- (3*pi,4.6);
    \draw[thick] (3.25*pi,4) -- (3.5*pi,4);
    
    % Second row: Overlapping pulses
    \draw[thick] (0,2) -- (1.5*pi,2);
	
	
    \draw[thick] (2*pi,2) -- (2.625*pi,2);
    \draw[thick, domain=2.625*pi:2.875*pi, samples=100] plot (\x, {-cos(deg(4*\x))+2});
    \draw[thick] (2.875*pi,2) -- (3.5*pi,2);
	
    
    % Third row: Receding pulses
    \draw[thick] (0,0) -- (0.25*pi,0);
    \draw[thick, domain=0.25*pi:0.5*pi, samples=100] plot (\x, {sin(deg(4*\x))/2});
    \draw[<-, thick] (0.125*pi,-0.6) -- (0.25*pi,-0.6);
    \draw[thick] (0.5*pi,0) -- (pi,0);
    \draw[thick, domain=pi:1.25*pi, samples=100] plot (\x, {sin(deg(4*\x))/2});
    \draw[->, thick] (1.25*pi,0.6) -- (1.375*pi,0.6);
    \draw[thick] (1.25*pi,0) -- (1.5*pi,0);
    
	\draw[thick] (2*pi,0) -- (2.25*pi,0);
    \draw[thick, domain=2.25*pi:2.5*pi, samples=100] plot (\x, {sin(deg(-4*\x))/2});
    \draw[<-, thick] (2.125*pi,0.6) -- (2.25*pi,0.6);
    \draw[thick] (2.5*pi,0) -- (3*pi,0);
    \draw[thick, domain=3*pi:3.25*pi, samples=100] plot (\x, {sin(deg(4*\x))/2});
    \draw[->, thick] (3.25*pi,0.6) -- (3.375*pi,0.6);
    \draw[thick] (3.25*pi,0) -- (3.5*pi,0);
\end{tikzpicture}

\end{document}
```
