
```tikz
\begin{document}

\begin{tikzpicture}[scale=1.5]
    
    % Medium separation
    \fill[cyan!40, opacity=0.15] (-3,-0.1) rectangle (3,0);
    
    % Normal line
    \draw[dashed, thick] (0,0) -- (0,2) node[above] {Normal to surface};
    
    % Incident ray
    \draw[-<, thick, magenta] (0,0) -- (150:3) 
        node[midway, above, sloped, xshift=-15pt] {Incident Ray};
    
    % Refracted ray
    \draw[->, thick, magenta] (0,0) -- ++(30:3) 
        node[midway, above, sloped, xshift=15pt] {Reflected Ray};
    

    % Angles
    \draw[thick] (0,0.4) arc (90:30:0.4) 
        node[right, yshift=10pt]{$\theta_2$}; 
    
    \draw[thick] (0,0.5) arc (90:150:0.5) 
        node[left, yshift=10pt]{$\theta_1$}; 
    


\end{tikzpicture}

\end{document}

```

