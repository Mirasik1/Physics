```tikz
\begin{document}
\begin{tikzpicture}
    % Draw the wave
    \draw[red!70, thick, domain=0:10, samples=500] plot (
        {\x}, {cos(deg(\x*2*pi*2.5))});
    
    % Draw the horizontal axis
    \draw[thick] (0,0) -- (10.5,0);
    \draw[opacity=0] (0,0) -- (13.5,0);
    \draw[thick] (0,-1.125) -- (0,1.125);

    \node[align=center] at (12,0) {the carrier wave\\(no modulation)};


\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}
\begin{tikzpicture}
    % Draw the wave
    \draw[blue!50, thick, domain=0:10, samples=200] plot (
        {\x}, {sin(deg(\x*2*pi/5))});
    
    % Draw the horizontal axis
    \draw[thick] (0,0) -- (10.5,0);
    \draw[opacity=0] (0,0) -- (13.5,0);
    \draw[thick] (0,-1.125) -- (0,1.125);
    
	\node[align=center] at (12,0) {the signal};


\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}
\begin{tikzpicture}
    % Draw the wave
    \draw[red!70, thick, domain=0:10, samples=1000] plot (
        {\x}, {cos(deg(\x*5*pi-5*cos(deg(\x*2*pi/5))))});
    
    % Draw the horizontal axis
    \draw[thick] (0,0) -- (10.5,0);
    \draw[opacity=0] (0,0) -- (13.5,0);
    \draw[thick] (0,-1.125) -- (0,1.125);

	\node[align=center] at (12,0) {the frequency-\\modulated wave};

    

\end{tikzpicture}
\end{document}
```

