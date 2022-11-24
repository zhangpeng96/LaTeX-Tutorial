




![[tikz/figures/1-1.png]]

```latex
\begin{tikzpicture}
    \tkzInit[xmin=-5,xmax=5,ymin=-5,ymax=5]
    \tkzDrawXY[noticks]
    \tkzGrid[color=gray]
    \tkzDefPoints{-4/4/A, -3/1/B, -1/2/C}
    \tkzDrawPolygon[line width=1pt](A,B,C)
    \tkzLabelPoints[left](B)
    \tkzLabelPoints[above](A)
    \tkzLabelPoints[right](C)
\end{tikzpicture}
```

![[1-2.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 2.2/0/C, 1.5/2/A, 1.2/0/D}
    \tkzDrawPolygon(A,B,C)
    \tkzDefPointsBy[projection=onto A--B](C){E}
    \tkzInterLL(A,D)(C,E) \tkzGetPoint{F}
    \tkzMarkRightAngle[size=0.15](B,E,C)
    \tkzDrawSegments(A,D C,E)
    \tkzLabelPoints[left](B,E)
    \tkzLabelPoints[above](A)
    \tkzLabelPoints[right](F,C)
    \tkzLabelPoints[below](D)
\end{tikzpicture}
```

![[1-3.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0.8/1.7/A, 0/0/B, 1.5/0/C, 2.5/1.7/D, 2/0/E, 1/2.2/G}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDrawSegments(A,C B,D C,E)
    \tkzDrawLines[add=0.3 and 0](A,B)
    \tkzInterLL(A,C)(B,D) \tkzGetPoint{F}
    \tkzLabelPoints[left](A,B,G)
    \tkzLabelPoints[right](D,E,F)
    \tkzLabelPoints[below](C)
\end{tikzpicture}
```

![[1-4.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 2.4/0/C, 1.4/1.8/A}
    \tkzDrawPolygon(A,B,C)
    \tkzDefPointsBy[projection=onto A--B](C){D}
    \tkzDefPointsBy[projection=onto A--C](B){E}
    \tkzDrawSegments(C,D B,E)
    \tkzMarkRightAngle[size=0.15](B,D,C)
    \tkzMarkRightAngle[size=0.15](A,E,B)
    \tkzLabelPoints[left](B,D)
    \tkzLabelPoints[above](A)
    \tkzLabelPoints[right](E,C)
\end{tikzpicture}
```


![[1-5.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 2/0/C, 1/3/A, 1/0/D}
    \tkzDrawPolygon(A,B,C)
    \tkzDefLine[mediator](A,C) \tkzGetPoints{E0}{F0}
    \tkzDefPointsBy[projection=onto B--C](A){D}
    \tkzInterLL(A,C)(E0,F0) \tkzGetPoint{E}
    \tkzInterLL(A,B)(E0,F0) \tkzGetPoint{F}
    \tkzInterLL(A,D)(E,F) \tkzGetPoint{M}
    \tkzDrawSegments(D,M B,M C,M)
    \tkzDrawLines[add=0.4 and 0.4](E,F)
    \tkzLabelPoints[left](B)
    \tkzLabelPoints[above](A,M)
    \tkzLabelPoints[right](C)
    \tkzLabelPoints[below](D)
    \tkzLabelPoints[above left](F)
    \tkzLabelPoints[below right](E)
\end{tikzpicture}
```


![[2-1.png]]

```latex

\begin{tikzpicture}
\begin{scope}
	\node at (1,-.5){(1)};
	\tkzDefPoints{.8/0/A, 1.2/1.5/B}
	\tkzDrawSegments(A,B)
	\tkzDrawPoints(A,B)
\end{scope}
\begin{scope}[xshift=2cm]
	\node at (.5,-.5){(2)};
	\tkzDefPoints{0/0/A, .6/1.5/B, 1.2/0/C}
	\tkzDrawPolygon(A,B,C)
	\tkzDrawPoints(A,B,C)
\end{scope}
\begin{scope}[xshift=4cm]
	\node at (.5,-.5){(3)};
	\tkzDefPoints{0/0/A, 1.2/0/B, 1/1.5/C, .2/1.5/D}
	\tkzDrawPolygon(A,B,C,D)
	\tkzDrawPoints(A,B,C,D)
	\tkzDrawSegments(A,C B,D)
\end{scope}
\begin{scope}[xshift=6cm]
	\node at (.5,-.5){(4)};
	\tkzDefPoints{0.2/0/A, 1.2/0/B, 1.6/.8/C,.7/1.2/D, -.2/.7/E}
	\tkzDrawPolygon(A,B,C,D,E)
	\tkzDrawSegments(A,C A,D B,D B,E C,E)
	\tkzDrawPoints(A,B,C,D,E)
\end{scope}
\end{tikzpicture}
```


![[2-2.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 3/.2/C, 3.1/1.5/D, .5/2.2/A}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDefMidPoint(A,B) \tkzGetPoint{E}
    \tkzDefMidPoint(B,C) \tkzGetPoint{F}
    \tkzDefMidPoint(C,D) \tkzGetPoint{G}
    \tkzDefMidPoint(D,A) \tkzGetPoint{H}
    \tkzDrawPoints[size=2](E,F,G,H)
    \tkzLabelPoints[below](C,B,F)
    \tkzLabelPoints[above](A,D,H)
    \tkzLabelPoints[left](E)
    \tkzLabelPoints[right](G)
    \tkzDrawSegments(E,F F,G G,H H,E)
\end{tikzpicture}
```



![[2-3.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoint(150:4){B}
    \tkzDefPoints{0/0/A, -3.464/0/C}
    \tkzDrawPolygon(A,B,C)
    \tkzDefMidPoint(A,B) \tkzGetPoint{E}
    \tkzDefPointsBy[projection=onto A--B](C){D}
    \tkzDrawSegments(C,E C,D)
    \tkzLabelPoints[left](B) 
    \tkzLabelPoints[above](D,E)
    \tkzLabelPoints[below](C,A)
    \tkzMarkRightAngle[size=0.15](A,C,B)
    \tkzMarkRightAngle[size=0.15](C,D,B)
\end{tikzpicture}
```



![[2-4.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoint(0,0){C}
    \tkzDefPoint(1.2,0){A}
    \tkzDefPoint(0,.8){B}
    \tkzDefSquare(B,A)\tkzGetPoints{E}{F}
    \tkzGetPointCoord(E){e}
    \tkzDefPoint(\ex,0){D}
    \tkzDefSquare(C,B)\tkzGetPoints{I}{J}
    \tkzDefSquare(E,D)\tkzGetPoints{H}{G}
    \tkzDrawPolygon[](C,B,I,J)
    \tkzDrawPolygon[](B,A,E,F)
    \tkzDrawPolygon[](D,E,G,H)
    \tkzDrawLine[add = .1 and .1](J,H)
    \node at (barycentric cs:C=1,B=1,I=1,J=1){$a$};
    \node at (barycentric cs:B=1,A=1,E=1,F=1){$c$};
    \node at (barycentric cs:D=1,E=1,G=1,H=1){$b$};
    \tkzLabelLine[below right](J,H){$l$}
\end{tikzpicture}
```



![[2-5.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{1.4/2.4/A, 0/0/B, 2.8/0/C}
    \tkzDrawPolygon(A,B,C)
    \tkzDefMidPoint(A,B) \tkzGetPoint{D}
    \tkzDefMidPoint(A,C) \tkzGetPoint{E}
    \tkzDefPointsBy[projection=onto B--C](D){G}
    \tkzDefPointsBy[projection=onto B--C](E){F}
    \tkzDrawPolygon[](D,G,F,E)
    \tkzLabelPoints[above](A,D,E)
    \tkzLabelPoints[below](B,C,F,G)
\end{tikzpicture}
```



![[2-6.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{2/1.5/A, 0/0/B, 2/-1.5/C, 4/0/D}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDefPointsBy[projection=onto B--C](A){E}
    \tkzDrawSegments(B,D A,C A,E)
    \tkzLabelPoints[above](A)
    \tkzLabelPoints[below](C,E)
    \tkzLabelPoints[left](B)
    \tkzLabelPoints[right](D)
    \tkzMarkRightAngle[size=0.15](A,E,C)
\end{tikzpicture}
```



![[2-7.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 0/2/A}
    \tkzDefSquare(A,B)\tkzGetPoints{C}{D}
    \tkzDrawPolygon[](A,B,C,D)
    \tkzDrawSegment(A,C)
    \tkzDefBarycentricPoint(A=1,B=4) \tkzGetPoint{E}
    \tkzDefBarycentricPoint(A=1,C=3) \tkzGetPoint{P}
    \tkzDrawSegments(P,B P,E)
    \tkzLabelPoints[left](A,B,E)
    \tkzLabelPoints[right](C,D,P)
    \tkzDrawPoints[size=2](P)
\end{tikzpicture}
```



![[2-8.png]]

```latex
\begin{tikzpicture}
	\tkzDefPoints{0/0/B,2/0/C,3/1.5/D}
	\tkzDefParallelogram(B,C,D) \tkzGetPoint{A}
	\tkzDrawPolygon(A,B,C,D)
	\tkzDrawSegments(A,C B,D)
	\tkzInterLL(A,C)(B,D) \tkzGetPoint{O}
	\tkzDefMidPoint(A,O) \tkzGetPoint{E}
	\tkzDefMidPoint(B,O) \tkzGetPoint{F}
	\tkzDrawSegments(E,F)
	\tkzDrawPoints[size=2](E,F)
	\tkzLabelPoints[above](A,D)
	\tkzLabelPoints[below](B,C,F,O)
	\tkzLabelPoints[right](E)
\end{tikzpicture}
```



![[2-9.png]]

```latex
\begin{tikzpicture}
	\tkzDefPoints{0/0/B, 1.4/2.7/A, 1.8/0/C}
	\tkzDrawPolygon(B,C,A)
	\tkzDefMidPoint(A,C) \tkzGetPoint{D}
	\tkzDefMidPoint(A,B) \tkzGetPoint{E}
	\tkzDrawSegments(C,E B,D)
	\tkzInterLL(C,E)(B,D) \tkzGetPoint{O}
	\tkzDrawPoints[size=2](O)
	\tkzDefMidPoint(O,B) \tkzGetPoint{M}
	\tkzDefMidPoint(O,C) \tkzGetPoint{N}
	\tkzDrawPolygon(E,M,N,D)
	\tkzLabelPoints[above](A,O)
	\tkzLabelPoints[below](B,C,M,N)
	\tkzLabelPoints[left](E)
	\tkzLabelPoints[right](D)
	\tkzMarkRightAngle[size=0.15](B,O,C)
\end{tikzpicture}
```



![[2-10.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/1.5/A, 0/0/B, 2/0/C}
    \tkzDefParallelogram(A,B,C) \tkzGetPoint{D}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDrawSegment(B,D)
    \tkzDefPointBy[reflection = over B--D](C) \tkzGetPoint{C'}
    \tkzDrawSegments[dashed](B,C' D,C')
    \tkzInterLL(B,C')(A,D) \tkzGetPoint{E}
    \tkzDrawPoints(E)
    \tkzLabelPoints[left](A,B,C')
    \tkzLabelPoints[right](C,D)
    \tkzLabelPoints[below right](E)
\end{tikzpicture}
```



![[2-11.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 0/2/A}
    \tkzDefSquare(A,B)\tkzGetPoints{C}{D}
    \tkzDrawPolygon[](A,B,C,D)
    \tkzDrawSegment(B,D)
    \tkzDefMidPoint(B,D) \tkzGetPoint{O}
    \tkzDrawLine[bisector](D,B,C) \tkzGetPoint{E}
    \tkzDefPointsBy[rotation=center C angle -90](E){F}
    \tkzDrawSegments(D,F C,F)
    \tkzInterLL(B,E)(D,F) \tkzGetPoint{H}
    \tkzDrawSegments(H,C E,H O,H)
    \tkzInterLL(O,H)(D,C) \tkzGetPoint{G}
    \tkzDrawPoints[size=2](O,G,E)
    \tkzLabelPoints[left](A,B,O)
    \tkzLabelPoints[right](D,F,H)
    \tkzLabelPoints[below](C)
    \tkzLabelPoints[above left](G)
    \tkzLabelPoints[below left](E)
\end{tikzpicture}
```



![[2-12.png]]

```latex
\begin{tikzpicture}
    \begin{scope}[xshift=0cm]
        \tkzDefPoints{0/0/B0, 0/1.2/A0}
        \tkzDefSquare(A0,B0)\tkzGetPoints{C0}{D0}
        \tkzDrawPolygon(A0,B0,C0,D0)
        \tkzDefMidPoint(C0,D0) \tkzGetPoint{C1}
        \tkzLabelPoint[right](C1){$\Rightarrow $}
    \end{scope}
    \begin{scope}[xshift=1.8cm]
        \tkzDefPoints{0/0/B0, 0/1.2/A0}
        \tkzDefSquare(A0,B0)\tkzGetPoints{C0}{D0}
        \tkzDrawPolygon(A0,B0,C0,D0)
        \tkzDefMidPoint(A0,B0) \tkzGetPoint{A1}
        \tkzDefMidPoint(B0,C0) \tkzGetPoint{B1}
        \tkzDefSquare(A1,B1) \tkzGetPoints{C1}{D1}
        \tkzDrawPolygon(A1,B1,C1,D1)
        \tkzLabelPoint[right](C1){$\Rightarrow $}
    \end{scope}
    \begin{scope}[xshift=3.6cm]
        \tkzDefPoints{0/0/B0, 0/1.2/A0}
        \tkzDefSquare(A0,B0)\tkzGetPoints{C0}{D0}
        \tkzDrawPolygon(A0,B0,C0,D0)
        \tkzDefMidPoint(A0,B0) \tkzGetPoint{A1}
        \tkzDefMidPoint(B0,C0) \tkzGetPoint{B1}
        \tkzDefSquare(A1,B1) \tkzGetPoints{C1}{D1}
        \tkzDrawPolygon(A1,B1,C1,D1)
        \tkzDefMidPoint(A1,B1) \tkzGetPoint{A2}
        \tkzDefMidPoint(B1,C1) \tkzGetPoint{B2}
        \tkzDefSquare(A2,B2) \tkzGetPoints{C2}{D2}
        \tkzDrawPolygon(A2,B2,C2,D2)
        \tkzLabelPoint[right](C1){$\Rightarrow $}
    \end{scope}
    \begin{scope}[xshift=5.4cm]
        \tkzDefPoints{0/0/B0, 0/1.2/A0}
        \tkzDefSquare(A0,B0)\tkzGetPoints{C0}{D0}
        \tkzDrawPolygon(A0,B0,C0,D0)
        \tkzDefMidPoint(A0,B0) \tkzGetPoint{A1}
        \tkzDefMidPoint(B0,C0) \tkzGetPoint{B1}
        \tkzDefSquare(A1,B1) \tkzGetPoints{C1}{D1}
        \tkzDrawPolygon(A1,B1,C1,D1)
        \tkzDefMidPoint(A1,B1) \tkzGetPoint{A2}
        \tkzDefMidPoint(B1,C1) \tkzGetPoint{B2}
        \tkzDefSquare(A2,B2) \tkzGetPoints{C2}{D2}
        \tkzDrawPolygon(A2,B2,C2,D2)
        \tkzDefMidPoint(A2,B2) \tkzGetPoint{A3}
        \tkzDefMidPoint(B2,C2) \tkzGetPoint{B3}
        \tkzDefSquare(A3,B3) \tkzGetPoints{C3}{D3}
        \tkzDrawPolygon(A3,B3,C3,D3)
        \tkzLabelPoint[right](C1){$\cdots $}
    \end{scope}
\end{tikzpicture}
```



![[2-13.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/A, 2/0/B, 2.5/1.5/C}
    \tkzDefParallelogram(A,B,C) \tkzGetPoint{D}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDefBarycentricPoint(A=3,C=1) \tkzGetPoint{E}
    \tkzDefBarycentricPoint(A=1,C=3) \tkzGetPoint{F}
    \tkzDrawSegments(A,C)
    \tkzDrawPolygon(D,E,B,F)
    \tkzLabelPoints[left](A,D,E)
    \tkzLabelPoints[right](B,C,F)
\end{tikzpicture}
```



![[2-14.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/B, 4/0/D, 0/-0.5/A, 4/-1/C}
    \tkzDrawSegments(A,B C,D)
    \tkzDrawLine[add = .1 and .1](B,D)
    \tkzLabelLine[below right](B,D){$l$}
    \tkzMarkRightAngle[size=0.15](A,B,D)
    \tkzMarkRightAngle[size=0.15](C,D,B)
    \tkzLabelPoints[above](B,D)
    \tkzLabelPoints[below](A,C)
\end{tikzpicture}
```


![[2-15.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/1.5/A, 0/0/B, 2/0/C}
    \tkzDefParallelogram(A,B,C) \tkzGetPoint{D}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDefMidPoint(A,D) \tkzGetPoint{M}
    \tkzDefMidPoint(B,C) \tkzGetPoint{N}
    \tkzDefMidPoint(B,M) \tkzGetPoint{E}
    \tkzDefMidPoint(C,M) \tkzGetPoint{F}
    \tkzDrawSegments(B,M C,M E,N F,N E,F M,N)
    \tkzLabelPoints[left](A,B,E)
    \tkzLabelPoints[right](C,D,F)
    \tkzLabelPoints[above](M)
    \tkzLabelPoints[below](N)
\end{tikzpicture}
```



![[2-16.png]]

```latex
\begin{tikzpicture}
    \tkzDefPoints{0/0/A, 3/0/B, 3/1.5/C}
    \tkzDefParallelogram(A,B,C) \tkzGetPoint{D}
    \tkzDrawPolygon(A,B,C,D)
    \tkzDefBarycentricPoint(A=2,D=3) \tkzGetPoint{Q}
    \tkzDefBarycentricPoint(A=4,B=3) \tkzGetPoint{P}
    \tkzDrawSegments(Q,C P,Q P,C)
    \tkzDrawPoints[size=2](Q,P)
    \tkzLabelPoints[left](A,D,Q)
    \tkzLabelPoints[right](B,C)
    \tkzLabelPoints[below](P)
\end{tikzpicture}
```


![[2-17.png]]

```latex
\begin{tikzpicture}
	\tkzInit[xmin=-4.4,xmax=1,ymin=-1,ymax=1]
	\tkzAxeX
	\tkzDefPoints{0/0/A, 0/1/B, -2/1/C}
	\tkzDefParallelogram(A,B,C) \tkzGetPoint{D}
	\tkzDrawPolygon(A,B,C,D)
	\tkzCompass[color=red,delta=25](A,C)
	\tkzCalcLength[cm](A,C)\tkzGetLength{ACl}
	\tkzDefPoint(-\ACl, 0){D}
	\tkzDrawPoints[size=2](A,C,D)
	\tkzDrawSegments(A,C)
	\tkzLabelPoints[above](C)
	\tkzLabelPoints[above left](D)
	\tkzLabelPoints[above right](A)
\end{tikzpicture}
```


