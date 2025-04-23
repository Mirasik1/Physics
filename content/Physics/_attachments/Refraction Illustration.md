
```tikz
\begin{document}

\begin{tikzpicture}[scale=1.5]
    
    % Medium separation
    \fill[cyan!40, opacity=0.15] (-5,-3) rectangle (3,0);
    \draw[thick, gray] (-5,0) -- (3,0);
    
    % Normal line
    \draw[dashed, thick] (0,-3) -- (0,3);
    
    % Incident ray
    \draw[<-, thick, magenta] (0,0) -- ++(120:3) 
        node[midway, above, sloped, xshift=-15pt] {Ray};
    
    % Refracted ray
    \draw[->, thick, magenta] (0,0) -- ++(-75:3) 
        node[midway, above, sloped] {Ray};
    
    % Wavefronts
    \foreach \x in {3, 2, 1, 0} { 
        \draw[thick, cyan] (-\x, 0) -- ++(30:{\x+2});
        \draw[thick, cyan] (-\x, 0) -- ++(-165:{-\x+5});
    }
    
    % Wavefront label
    \draw[thick, cyan] (-2, 0) -- ++(30:4) 
        node[midway, sloped, above, xshift=-11pt] {Wave fronts};
    
    % Angles
    \draw[thick] (-2.6,0) arc (0:30:0.4) 
        node[right, xshift=5pt]{$\theta_1$}; 
    
    \draw[thick] (-3.4,0) arc (-180:-165:0.4) 
        node[left, yshift=-5pt]{$\theta_2$}; 
    
    \draw[thick] (0,0.4) arc (90:120:0.4) 
        node[right, xshift=5pt]{$\theta_1$}; 
    
    \draw[thick] (0,-0.4) arc (-90:-75:0.4) 
        node[left]{$\theta_2$};
    
    % Medium labels
    \node[right] at (2, 1) {1}; 
    \node[right] at (2, -1) {2}; 

\end{tikzpicture}

\end{document}

```

