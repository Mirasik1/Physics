
```tikz
\usepackage{tikz}

\begin{document}

\begin{tikzpicture}[scale=0.5]

	\pgfmathsetmacro{\lensRadius}{13}
	\pgfmathsetmacro{\lensHeight}{6}
	\pgfmathsetmacro{\startAngle}{asin(\lensHeight/\lensRadius)}
	\pgfmathsetmacro{\lensWidth}{\lensRadius * (1 - cos(\startAngle))}

	\draw[->] (-5, 5) -- (1,5) -- ++({3.141-2*0.394 r}:-3);
	\draw[->] (-5, -5) -- (1,-5) -- ++({2*0.394 r}:-3);


	\draw[dashed] plot[domain=-3:1, samples=100] (\x, {-5/12*(\x-13)});
	\draw[dashed] plot[domain=-3:1, samples=100] (\x, {5/12*(\x-13)});

    \node[align=center, font = {\Large\bfseries\sffamily}] at (-3,0){Rays\\from\\distant\\source};


    \draw [fill = cyan!40, opacity=0.15]  (1.46744,\lensHeight)
    arc[start angle=180-\startAngle,delta angle=2*\startAngle,radius=\lensRadius] -- ++(0.5,0) arc[start angle=180-\startAngle + 2*\startAngle,delta angle=-2*\startAngle,radius=\lensRadius];
    
\begin{scope}[xshift=500]
	\draw[->] (-7, 5) -- (-1,5) -- ++({2*0.394 r}:-3);
	\draw[->] (-7, -5) -- (-1,-5) -- ++({3.141-2*0.394 r}:-3);


	\draw[dashed] plot[domain=-5:-1, samples=100] (\x, {-5/12*(\x+13)});
	\draw[dashed] plot[domain=-5:-1, samples=100] (\x, {5/12*(\x+13)});

	\node[align=center, font = {\Large\bfseries\sffamily}, xshift=-50] at (-3,0){Rays\\from\\distant\\source};

    \draw [fill = cyan!40, opacity=0.15]  (-1.46744,\lensHeight)
    arc[start angle=\startAngle,delta angle=-2*\startAngle,radius=\lensRadius] -- ++(0.5,0) arc[start angle=-\startAngle,delta angle=2*\startAngle,radius=\lensRadius];
\end{scope}

\end{tikzpicture}

\end{document}

```



