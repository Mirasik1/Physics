
```tikz
\begin{document}

\begin{tikzpicture}[scale=2/3]
    
    % Medium separation
    \draw[thick] (-7,0) -- (13.6,0);
    \draw[dashed] (0,-4) -- (0,4);
    
    \draw[->, thick, red] (-6,0) -- (-6,1) node[midway, left] {Object};
    
    % Rays
    \draw[->, magenta] (-6,1) -- (0,1);
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-\x/4+1});


	\pgfmathsetmacro{\lensRadius}{8}
	\pgfmathsetmacro{\lensHeight}{3}
	\pgfmathsetmacro{\startAngle}{asin(\lensHeight/\lensRadius)}

	\draw [fill = cyan!40, opacity=0.15]  (0,\lensHeight)
  arc[start angle=180-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
  arc[start angle=-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
   -- cycle;
    
    % Medium labels
    \node[above] at (-4, 0) {F`}; 
    \node[above] at (4, 0) {F}; 
    \draw[fill=black] (-4,0) circle (2pt);
	\draw[fill=black] (4,0) circle (2pt);


\end{tikzpicture}

\end{document}


```
```tikz
\begin{document}

\begin{tikzpicture}[scale=2/3]
    
    % Medium separation
    \draw[thick] (-7,0) -- (13.6,0);
    \draw[dashed] (0,-4) -- (0,4);
    
    \draw[->, thick, red] (-6,0) -- (-6,1) node[midway, left] {Object};
    \draw[->, thick, dashed, red] (12,0) -- (12,-2) node[midway, right] {Image};
    
    % Rays
    \draw[->, magenta] (-6,1) -- (0,1);
    \draw[->, magenta] (-6,1) -- (0,-2);
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-\x/4+1});
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-2});
    
	\pgfmathsetmacro{\lensRadius}{8}
	\pgfmathsetmacro{\lensHeight}{3}
	\pgfmathsetmacro{\startAngle}{asin(\lensHeight/\lensRadius)}


	\draw [fill = cyan!40, opacity=0.15]  (0,\lensHeight)
  arc[start angle=180-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
  arc[start angle=-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
   -- cycle;
    
    % Medium labels
    \node[above] at (-4, 0) {F`}; 
    \node[above] at (4, 0) {F}; 
    \draw[fill=black] (-4,0) circle (2pt);
	\draw[fill=black] (4,0) circle (2pt);


\end{tikzpicture}

\end{document}


```
```tikz
\begin{document}

\begin{tikzpicture}[scale=2/3]
    
    % Medium separation
    \draw[thick] (-7,0) -- (13.6,0);
    \draw[dashed] (0,-4) -- (0,4);
    
    \draw[->, thick, red] (-6,0) -- (-6,1) node[midway, left] {Object};
    \draw[->, thick, dashed, red] (12,0) -- (12,-2) node[midway, right] {Image};
    
    % Rays
    \draw[->, magenta] (-6,1) -- (0,1);
    \draw[->, magenta] (-6,1) -- (0,-2);
    \draw[->, magenta] plot[domain=-6:13, samples=100] (\x, {-\x/6});
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-\x/4+1});
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-2});
    
	\pgfmathsetmacro{\lensRadius}{8}
	\pgfmathsetmacro{\lensHeight}{3}
	\pgfmathsetmacro{\startAngle}{asin(\lensHeight/\lensRadius)}


	\draw [fill = cyan!40, opacity=0.15]  (0,\lensHeight)
  arc[start angle=180-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
  arc[start angle=-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
   -- cycle;
    
    % Medium labels
    \node[above] at (-4, 0) {F`}; 
    \node[above] at (4, 0) {F}; 
    \draw[fill=black] (-4,0) circle (2pt);
	\draw[fill=black] (4,0) circle (2pt);


\end{tikzpicture}

\end{document}


```

