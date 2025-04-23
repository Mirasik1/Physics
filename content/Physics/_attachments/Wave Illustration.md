```tikz
\begin{document}
\begin{tikzpicture}
    % Draw the wave
    \draw[red, thick, domain=0:4.5*pi, samples=100] plot (
        {\x}, {1.5*sin(deg(\x))});
    
    % Draw the horizontal axis
    \draw[thick, ->] (-0.125,0) -- (4.5*pi,0);
    
    % Labels for crest and trough
    \node[above] at ({pi/2},1.5) {Crest};
    \node[below] at ({3*pi/2},-1.5) {Trough};
    
    % Amplitude markers
    \draw[|-|, thick] ({pi/2},0) -- ({pi/2},1.5) node[yshift=-50pt] {Amplitude};
    \draw[|-|, thick] ({3*pi/2},0) -- ({3*pi/2},-1.5) node[yshift=50pt] {Amplitude};
    
    % Wavelength markers
    \draw[<->, thick] ({1.75*pi},-1.05) -- ({3.75*pi},-1.05) node[midway,below] {$\lambda$};
    \draw[<->, thick] ({2.5*pi},1.55) -- ({4.5*pi},1.55) node[midway,above] {$\lambda$};
\end{tikzpicture}
\end{document}
```

