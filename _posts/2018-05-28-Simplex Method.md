# Simplex Method

1. Assume we have a feasilble solution

      [y0,y1,.....ym,0,0,0,0,0]^T

      則如何change basis

2.two more issues

- how to choose which column q enter and p exits
- stopping criterion, change to a BFS let the objective function be "smaller"

this will include the term "rcc", relative cost coefficient

### Background

$$
\begin{align*}

&
\begin{bmatrix}
   A  ,b
\end{bmatrix}
\\
&
E\begin{bmatrix}
   A  ,b
\end{bmatrix}
=
\begin{bmatrix}
  I_m ,Y_{m,n-m},\widetilde{b}
\end{bmatrix}
\\
&
x=[x_{B} ^T, x_D ^T]^T is \ \ a \ \ solution \ \ to \ \ Ax=b
, \    \
x_B=\widetilde{b}-Dx_D
\ \ , \   \widetilde{b} \ \ is \ \ a \ \ solution\ \ to \ \ A_{m} x=b_{m} 
\\
&
x=\begin{bmatrix}
  \widetilde{b}
  \\
  0
\end{bmatrix}+
\begin{bmatrix}
  -Dx_D
  \\
  x_D
\end{bmatrix},x_D \in R^{n-m}
\\
&
\ \ particular\& homogenous  
\\
&
好好思考行列數跟\widetilde{b}的關係
\end{align*}
$$



### Canonical Augmented Matrix

$$
\begin{align*}
&
Define 
\begin{bmatrix}
  I_m ,Y_{m,n-m},\widetilde{b}
\end{bmatrix}x=y_0 \ \ called \ \ Canonical\ \  Augmented \ \ Matrix
\\
&
\begin{bmatrix}
  I_m ,Y_{m,n-m},\widetilde{b}
\end{bmatrix}x=y_0, note \ \ that \ \ Ay_0=b
\\
&
that\ \ is
\\
&
b=y_{10}a_1+y_{20}a_2+y_{30}a_3+...+y_{m0}a_m
\\
&
重點來了
\\
&
Let \ \ a_{i} ', i=1,...,n+1 \ \ be \ \ the \ \ column \ \ in \ \ the \ \ augmented \ \ matrix
\\
&
for \ \ m< j  \leq n
\\
&
a_j ' =y_{1j}a_1 '+y_{2j}a_2 ' +...+y_{mj}a_m ' , because \ \ [a_1 '...a_m '] =[e_1,...,e_m]
\\
&
left \ \ multiply \ \ E^{-1}
\\
&
a_j= y_{1j}a_1 +y_{2j}a_2  +...+y_{mj}a_m ,m<j \leq n
\end{align*}
$$



### Change Basis

