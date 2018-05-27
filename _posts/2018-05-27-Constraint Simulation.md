# Constraint Simulation

> 會寫這篇是因為最近實作的論文，需要處理Constraint Simulation。
>
> Background: Multivariable Calculus, Linear Algebra, Particle System

## Impulse-Based Dynamics
>**There is, however, another technique that is very popular among game physics engines, which takes an impulse-based approach, operating on the velocity of the bodies and not on the force or acceleration**.

[Tutorial1](https://github.com/tommyvsfu1/Computer-Animation/tree/master/constraint%20dynamic/constraint_pendulum)

![pendulum](https://i.imgur.com/pF6XaPm.gif)

這個tutorial  是非常簡單的Constraint 範例

由於還不熟悉java library , 因此我是直接寫出explicit form 

比較優雅的方式當然是matrix form

Constraint function
$$
\begin{split}
C &= \frac{1}{2}*(p \cdot{p} - l^2)
  \newline
   &= \frac{1}{2}*(x^2+y^2-l^2)
   \newline
J &= [\frac{\partial C}{\partial x},\frac{\partial C}{\partial y}]
   \newline
   &= [x,y]
    \newline
JM^{-1}J^{T}\lambda&=-J(\frac{\dot{q}}{\Delta{t}}+M^{-1}F_{ext})
    \newline
    \Bigg( )
\end{split}
$$




















註記：

[非常推薦文章](https://www.toptal.com/game/video-game-physics-part-iii-constrained-rigid-body-simulation)





