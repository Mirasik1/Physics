
```tikz
\begin{document}

\begin{tikzpicture}[scale=0.8]
    
    % Medium separation
    \draw[thick] (-7,0) -- (29,0);
    \draw[dashed] (0,-3) -- (0,3);
    \draw[dashed] (20,-3) -- (20,3);
    
    \draw[->, thick, red] (-6,0) -- (-6,1) node[midway, left] {Object};
    \draw[->, thick, dashed, red] (12,0) -- (12,-2);
    \draw[->, thick, dashed, red] (28,0) -- (28,2) node[midway, right] {Image};
    
    % Rays
    \draw[->, magenta] (-6,1) -- (0,1);
    \draw[->, magenta] (-6,1) -- (0,-2);
    \draw[->, magenta] plot[domain=-6:13, samples=100] (\x, {-\x/6});
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-\x/4+1});
    \draw[->, magenta] plot[domain=0:13, samples=100] (\x, {-2});


    \draw[->, magenta] plot[domain=12:29, samples=100] (\x, {\x/4-5});
    \draw[->, magenta] plot[domain=20:29, samples=100] (\x, {\x/2-12});
    \draw[->, magenta] plot[domain=12:20, samples=100] (\x, {\x/2-8});
    \draw[->, magenta] plot[domain=12:20, samples=100] (\x, {-2});
    \draw[->, magenta] plot[domain=20:29, samples=100] (\x, {2});
    
	\pgfmathsetmacro{\lensRadius}{8}
	\pgfmathsetmacro{\lensHeight}{3}
	\pgfmathsetmacro{\startAngle}{asin(\lensHeight/\lensRadius)}


	\draw [fill = cyan!40, opacity=0.15]  (0,\lensHeight)
  arc[start angle=180-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
  arc[start angle=-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
   -- cycle;

	\draw [fill = cyan!40, opacity=0.15]  (20,\lensHeight)
  arc[start angle=180-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
  arc[start angle=-\startAngle,delta angle=2*\startAngle,radius=\lensRadius]
   -- cycle;
	
    
    % Medium labels
    \node[above] at (-4, 0) {F`}; 
    \node[above] at (4, 0) {F};     
    \node[above] at (16, 0) {F`}; 
    \node[above] at (24, 0) {F}; 
    \draw[fill=black] (-4,0) circle (2pt);
	\draw[fill=black] (4,0) circle (2pt);
	\draw[fill=black] (16,0) circle (2pt);
	\draw[fill=black] (24,0) circle (2pt);



    \draw[-] (-6,-0.2) -- (-6,-4.2);
    \draw[-] ( 0,-3) -- ( 0,-4.2);
    \draw[-] (12,-2.2) -- (12,-4.2);
    \draw[-] (20,-3) -- (20,-4.2);
    \draw[-] (28,-0.2) -- (28,-4.2);

    \draw[<->] (-6+0.2,-4) -- ( 0-0.2,-4) node[midway, above] {$d_{oA}$};
    \draw[<->] ( 0+0.2,-4) -- (12-0.2,-4) node[midway, above] {$d_{iA}$};
    \draw[<->] (12+0.2,-4) -- (20-0.2,-4) node[midway, above] {$d_{iB}$};
    \draw[<->] (20+0.2,-4) -- (28-0.2,-4) node[midway, above] {$d_{oB}$};

	


\end{tikzpicture}

\end{document}


```

