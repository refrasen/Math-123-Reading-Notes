# Math 123 Reading Notes (8)

## Chapter 8. Equilibria in Nonlinear Systems

### 8.1 Some Illustrative Examples

#### Stable Curve

Not very clear, the methodology of finding a stable curve for any nonlinaer system

It was a very specific example

It was more staged as, once we found the general solution to the system

Prove that on this curve are solutions that tend towards (0,0) as time increases

#### Change of variables as a way to convert to linear systems?

introduce

$u = f(x,y)$

$v = g(x,y)$ for example and have

$\frac{\partial u}{\partial t} = \frac{\partial f}{\partial x}\frac{\partial x}{\partial t} + \frac{\partial f}{\partial y}\frac{\partial y}{\partial t}$

$\frac{\partial v}{\partial t} = \frac{\partial g}{\partial x}\frac{\partial x}{\partial t} + \frac{\partial g}{\partial y}\frac{\partial y}{\partial t}$

#### in general, impossible to convert a nonlinear system to a linear one 

##### Tip: Sometimes changing to polar coordinates helps

$x = r\cos\theta$

$x'(t) = \frac{\partial x}{\partial r}\frac{\partial r}{\partial t} + \frac{\partial x}{\partial \theta}\frac{\partial \theta}{\partial t}$ $= r'(t)\cos\theta + (-r\sin\theta)\theta'(t)$ 

and similarly for $y'$   

then we can get a system for

$r' = ... \\\theta' = ...$  

#### Understand geometrically...

if we're looking at a two dimensional system, 

when is $x', y' \begin{cases} > 0 \\ = 0 \\<  0 \end{cases}$  

#### Possible to linearize a system locally, sometimes

##### Get a linearized system (locally), find a conjugacy between the flow of the linearized system and the nonlinearized system?

#### Example of system that cannot be linearized (page 164)

#### Linear planar system with zero eigenvalue or center

addition of nonlinear terms often changes the phase portrait

### 8.2 Nonlinear Sinks and Sources

#### Solutions of planar nonlinear systems near eq. points. resemble those of their linear parts only in the case where the linearized system is hyperbolic

##### hyperbolic meaning real part of eigenvalues is nonzero

#### Linearized System near $X_0$

Let: $X' = F(X)$

Suppose: $F(X_0) = 0$ 

Let $DF_{X_0}$ *denote* the Jacobian matrix of $F$ evaluated at $X_0$ 

Then, the linear system of diff. eqn.'s

$Y' = DF_{X_0}Y$ is the linearized system near $X_0$ 

If $X_0 = 0$, the linearized system is obtained by simply dropping all of the nonlinear terms in $F$ 

e.g., $F_1(x,y) = x^2 + y$ 

$F_2(x,y) = xy^2 + 3x$ 

$\frac{\partial F_1}{\partial x} = 2x, \frac{\partial F_1}{\partial y} = 1$  , and similalry for $F_2$

we get

$Y' = \begin{pmatrix} 0 & 1 \\ 3 & 0 \end{pmatrix}\begin{pmatrix} x \\ y \end{pmatrix}$ 

so $x' = x \\ y' = 3x $ 

#### Specialize discussion: Planar system, linearized system has a sink at $0$ 

$x' = f(x,y) \\ y' = g(x,y)$ is the system

$f(x_0,y_0) = 0 = g(x_0, y_0)$ 

Change of coordinates:

$u = x - x_0, v = y - y_0$ 

we have a new system that has an equilibrium point at (0,0)

So we assume that $x_0 = y_0 = 0$ at the outset. 

Further, another linear change of coordinates to put the linearized system in canonical form

Assume linearized system has dist. eigenvalues: $-\lambda < -\mu < 0$  

our system becomes

$x' = -\lambda x + h_1(x,y) \\ y' = -\mu y + h_2(x,y)$ 

$h_j = h_j(x,y)$ contains all the higher order terms 

$h_j$ contnains terms that are quadratic or higher order in $x$ and/or $y$ 

equiv: $\lim_{(x,y) \rightarrow (0,0)} \frac{h_j(x,y)}{r} = 0$  

where $r = \sqrt{x^2 + y^2}$ 

The linearized system:

$x' = -\lambda x\\ y' = - \mu y$ (this indeed matches up with the whole $Y' = DF_{X_0}Y$, as we are assuming $X_0 = (0,0)$ 

The vector field for this system always points inside the circle of radius $r = \sqrt{x^2 + y^2}$ 

So for the linearized system, all solutions tend towards origin with strictly decreasing radial components

The same thing happens for the nonlinear system, at least close to (0,0)

$q(x,y)$ denotes the dot product of the vector field with $(x,y)$ 

and after simplifying and combining certains terms etc, we end up having

$q(x,y) < 0$ at least near the origin

##### For the $\alpha + i\beta$ eigenvalue case: (spiral sink), $\alpha < 0$ 

we do the same thing (?) but with the system:

$x' = \alpha x - \beta y + h_1(x,y) \\ y' = \beta x + \alpha y + h_2(x,y)$ 

##### For repeated Eigenvalues

Want to obtain a linearized system:

$x' = -\lambda x + \epsilon y \\ y' = -\lambda y$ , where $\epsilon$ is suff. small (see chapter 4)

#### The Linearization Theorem

Suppose: the $n-dim$ system $X' = F(X)$ has an equilibrium point at $X_0$ that is hyperbolic

Then: the nonlinear flow is conjugate to the flow of the linearized system in a neighborhood of $X_0$ 

Note: book didn't prove this.

This theorem lets us know what types of linear systems can be linearized(?) near equilibrium points

### 8.3 Saddles

Case of an equilibrium for which the linearized system has a saddle at the origin in $\R^2$. 

We may assume that this system is in the form

$x' = \lambda x + f_1(x,y)$ 

$y' = -\mu y + f_2(x,y)$ 

where $-\mu < 0 < \lambda$ 

and $f_j(x,y)/r$ tends to $0$ as $r \rightarrow 0$ 

We call this type of equilibrium point a saddle 

For the linearized system, the $y-$axis serves as the stable line, with all solutions on this line tending to $0$ as $t \rightarrow \infin$ 

the $x$-axis is the unstable line.

We cannot expect these stable and unstable straight lines to persist in the nonlinear case

However, there do exist a pair of curves through the origin that have similar properties

Let $W^s(0)$ denote the set of initial conditions whose solutions tend to the origin as $t\rightarrow \infin$ 

Let $W^u(0)$ denote the set of points whose solutions tend to origin as $t\rightarrow\infin$ 

$W^s(0)$ and $W^u(0)$ are called the stable curve and unstable curve respectively

#### The Stable Curve Theorem

Suppose the system

$x' = \lambda x + f_1(x,y) \\ y' = -\mu y + f_2(x,y)$ 

satisfies $-\mu < 0 < \lambda$ and $f_j(x,y)/r \rightarrow 0$ as $r \rightarrow 0$ 

Then:

there is an $\epsilon > 0$ and a curve $x = h^s(y)$ that is defined for $|y| < \epsilon$ and satisfies $h^s(0) = 0$ 

Furthermore:

1. All solutions whose initial condition lie on this curve remain on this curve for all $t \geq 0$ and tend to the origin as $t \rightarrow \infin$ 
2. The curve $x = h^s(y)$ passes through the origin tangent to the $y-axis$ 
3. All other solutions whose initial conditions lie in the disk of radius $\epsilon$ centered at the origin leave this disk as time increases

##### Remarks

1. The curve $x = h^s(y)$ is called the local stable curve at $0$ 
2. We can find the complete stable curve $W^s(0)$ by following solutions that lie on the local stable curve backward in time
3. The function $h_s(y)$ is actually $C^\infin$ at all points, but we won't prove it here

A similar unstable curve theorem provides us with a local unstable curve of the form $y = h^u(x)$ 

* This curve is tangent to the $x-$axis at the origin
* all solutions on this curve tend to the origin as $t \rightarrow -\infin$ 

##### Brief sketch of the proof 

1. Consider the square bounded by the lines $|x| = \epsilon$ and $|y| = \epsilon$ for $\epsilon >0$ sufficiently small
   1. The nonlinear vector field points into the square along the interior of the top and the bottom boundaries, $y = \pm \epsilon$ , since the system is close to the linear system $x' = \lambda x$, $y' = -\mu y$ 
   2. The nonlinear vector field points outside the square along the left and right boundaries, $x = \pm \epsilon$ 
2. Consider the initial conditions that lie along the top boundary $y = \epsilon$ 
   1. Some of these solutions will exist the square to the left, while others exist to the right
   2. Solutions cannot do both, so these sets are disjoint
      1. Moreover, these sets are open
      2. the boundary contains points that get arbitrarily close to these sets that aren't in these sets (?)
      3. if the union of these open sets, which is an open set, made up the entire boundary, we would get a contradiction since the boundary contains points that no disk centered on them is in the boundary.
   3. So there must be some initial conditions whose solutions do not exit at all
3. We will 
   1. show that each of these nonexiting solutions tend to the origin
   2. show that there is only one intial condition on the top and bottom boundary whose solution behaves this way
   3. show that this solution lies along some graph of the form $x = h^s(y)$, which has the required properties

##### Filling in the details of the proof

1. Let $B_\epsilon$ denote the square bounded by $x = \pm \epsilon$ and $y = \pm \epsilon$ 
2. Let $S_\epsilon^\pm$ denote the top and bottom boundaries of $B\epsilon$ 
3. Let $C_M$ denote the conical region given by $|y| \geq M|x|$ inside $B_\epsilon$ 

##### Lemma.

Given $M > 0$, there exists $\epsilon > 0$ such that the vector field points outside $C_M$ for the points on the boundary of $C_M \cap B_\epsilon$ (except at the origin)

Proof

1. Given $M$, choose $\epsilon > 0$ so that $|f_1(x,y)| \leq \frac{\lambda}{2\sqrt{M^2+1}}r$ for all $(x,y) \in B_\epsilon$ 

   1. allowed to do this since $\frac{f_1(x,y)}{r}\rightarrow 0$ as $ (x,y) \text{ or }r \rightarrow 0$ ?, as in, $f_1(x,y)$ is $o(r)$?
   2. so for $\delta = \frac{\lambda}{2\sqrt{M^2+1}}$, there exists $\epsilon' > 0$ s.t. for all $|(x,y)|\leq \epsilon'$ , $|\frac{f_1}{r}| \leq \delta$ etc.  
   3. and $\epsilon$ will represent the largest side length of a square that can fit in the disk with radius $\epsilon'$

2. Now suppose $x > 0$. Then along the right boundary of $C_M$ we have

   1. $x' = \lambda x + f_1(x, Mx)$

      $\geq \lambda x - |f_1(x, Mx)|$

      $\geq \lambda x - \frac{\lambda}{2\sqrt{M^2+1}}r$

      $= \lambda x - \frac{\lambda}{2\sqrt{M^2+1}}(x\sqrt{M^2+1})$

      ​	$r = x\sqrt{M^2+1}$?

      ​	$\sqrt{x^2 + M^2x^2} = x\sqrt{M^2+1}$ checks out

      $= \frac{\lambda}{2}x > 0$

   2. So $x' > 0$ on this side of the boundary cone

3. Similarly, if $y > 0$, we may choose $\epsilon > 0$ smaller if necessary so that we have $y' < 0$ on the edges of $C_M$ where $y > 0$

   1. Choosing $\epsilon$ so that $|f_2(x,y)| \leq \frac{\mu}{2\sqrt{M^2+1}}r$ 

4. On the edge of $C_M$ that lies in the first quadrant, the vector field points down and to the right and hence out of $C_M$ 

5. Similar calculations show that the vector field points outside $C_M$ on all other edges of $C_M$ 

It follows from this lemma that there is a set of initial conditions in $S_{\epsilon}^{\pm}\cap C_M$ whose solutions eventually exit from $C_M$ to the right and another set in $S_\epsilon^\pm \cap C_M$ whose solutions exist left

These sets are open because of continuity of solutions with respect to initial conditions

​	a continuous function brings open sets to open sets?

​	Let $X_0$ be an initial condition such that $\phi(t,X_0)$ eventually leave $C_M$ 

​	then we have for any $\epsilon > 0$, there exists $\delta > 0$ s.t. for any $X$ satisfying $|X - X_0| < \delta$, $|\phi(t,X) - \phi(t,X_0)| < \epsilon$  (not for all of $t$ perhaps)

​	so for any $X_0$ s.t. the $\phi(t,X_0)$ eventually leaves $C_M$, there's a disk centered around it s.t. all initial conditions in this disk have solution that eventually exit

---

**We next show that each of these sets is actually a single open interval**

$C_M^+$ denotes the portion of $C_M$ lying above the $x-$axis

$C_M^-$ denotes the portion lying below this axis

##### Lemma. 

Suppose $M > 1$. Then there is an $\epsilon > 0$ such that $y' < 0$ in $C_M^+$ and $y' > 0$ in $C^-_M$  

Proof:

$|Mx| \leq y$ in $C_M^+$ so that

$r^2 = x^2 + y^2$, and $x^2 \leq y^2/M^2$ inside the cone

$r^2 \leq y^2/M^2 + y^2$ or $r \leq \frac{y}{M}\sqrt{1+M^2}$ 

1. As in the previous lemma, we choose $\epsilon$ so that
   1. $|f_2(x,y)| \leq \frac{\mu}{2\sqrt{M^2+1}}r$  for all $(x,y) \in B_\epsilon$. 
2. We then have in $C_M^+$
   1. $y' \leq -uy + |f_2(x,y)|$ 
      1. just from the system and facts about inequalities and absolute values
   2. $\leq -\mu y + \frac{\mu}{2\sqrt{M^2+1}}r$
      1. 
   3. $\leq -\mu y + \frac{\mu}{2M}y$
   4. $\leq -\frac{\mu}{2}y$ 

This proves the result for $C_M^+$, the proof for $C_M^-$ is similar

1. $y \leq -|Mx|$ $\equiv$ $y^2 \geq M^2x^2$
2. $r < y/M \times \sqrt{1+M^2}$
3. $y' \geq -\mu y - |f_2(x,y)|$ 
   1. $\geq$ $\mu|y| - \frac{\mu}{2\sqrt{M^2+1}}r$
   2. $\geq \mu|y| - \frac{\mu}{2M}y$
      1. if $a > b$, then $ac < bc$, if $c < 0$ 
      2. so $r < y/M(\sqrt{1+M^2})$,
      3. $-r \frac{\mu}{2 \sqrt{M^2+1}} > -\frac{\mu}{2M}y$ 

What this tells us is that solutions that begin on $S_\epsilon^+\cap C_M$ decrease in the $y-$direction while they remain in $C_M^+$. 

No solution can remain in $C_M^+$ for all time unless that solution tends to the origin

By the **existence and uniqueness theorem**, the set of points in $S_\epsilon^+$ that exit to the right or left must then be two open intervals (one interval for solutions exiting right, one for left)

* As in, paths cannot cross each other
* Imagine having two separate intervals with solutions exiting to the right (or left)
  * then in between we have solutions that will eventually cross these solutions as they 
    * tend towards origin 
    * exit left ( or right)

We see similar behavior in $C_M^-$ 

---

**We now claim that the interval of initial conditions in $S_\epsilon^\pm$ whose solutions tend to 0 is actually a single point**

1. Recall the variational equation for this system (Section 7.4)
   1. $U' = DF_{X(t)}U$, 
   2. where 
      1. $X(t)$ is a given solution of the nonlinear system 
      2. ![1539162671923](C:\Users\Renee\AppData\Roaming\Typora\typora-user-images\1539162671923.png)
   3. Shown in Chapter 7, given $\tau > 0$, if $|U_0|$ is sufficiently small, then the solution of the variational equation, $U(t)$ that satisfies $U(0) = U_0$ and the solution $Y(t)$ of the nonlinear system satisfying $Y(0) = X_0 + U_0$ remain close to each other for $0 \leq t \leq \tau$ 
   4. Now let $X(t) = (x(t), y(t))$ be one of the solutions of the system that never leaves $C_M$. Suppose $x(0) = x_0$, $y(0) = \epsilon$ 

##### Lemma. 

Let $U(t) = (u_1(t), u_2(t))$ be any solution of the variational equation $U' = DF_{X(t)}U$

that satisfies $|u_2(0)/u_1(0)| \leq 1$. Then we may choose $\epsilon > 0$ sufficiently small so that $|u_2(t)| \leq |u_1(t)|$ for all $t \geq 0$ 

Proof:

1. The variational equation may be written
   1. $u_1' = \lambda u_1 + f_{11}u_1 + f_{12}u_2 \\ u_2' = -\mu u_2 + f_{21}u_1 + f_{22}u_2$
      1. $|f_{ij}|$ may be made as small as we like by choosing $\epsilon$ smaller
      2. Because $|x_0| \leq \epsilon$, since $X_0$ is one of the initial conditions on the upper boundary of a square with side lengths $2\epsilon$ 
2. Given any solution $(u_1(t), u_2(t))$ of this equation, let $\eta = \eta(t)$ be the slope $u_2(t)/u_1(t)$ of the solution
3. Using the variational equation and the quotient rule, we find that $\eta$ satisfies
   1. $\eta' = \alpha(t) - (\mu + \lambda + \beta(t))\eta + \gamma(t)\eta^2$ 
      1. $\alpha(t) = f_{21}(t)$ 
      2. $\beta(t) = f_{11})t -f_{22}(t)$ 
      3. $\gamma(t) = -f_{21}(t)$ 
   2. $\alpha, \beta, \gamma$ are small
4. Recall that $\mu + \lambda > 0$ $\implies$ $-(\mu + \lambda + \beta(t)) < 0$ 
   1. since $|\beta(t)|$ is sufficiently small enough
5. It follows that, if $\eta(t) > 0$, there are constants $a_1, a_2$ with $0 < a_1 < a_2$ such that
   1. $-a_2 \eta + \alpha(t) \leq \eta ' \leq -a_1 \eta + \alpha (t)$
6. Now, if we choose $\epsilon$ small enough and set $u_1(0) = u_2(0)$ so that $\eta(0) = 1$, then we have $\eta'(0) < 0$, so that $\eta(t)$ initially decreases
   1. Similarly if $\eta(0) = -1$, then $\eta'(0) > 0$ so $\eta(t)$ increases
7. In particular, any solution that begins with $|\eta(0)| <1$ can never satisfy $\eta(t) = \pm 1$
8. Since our solution satisfies $|\eta(0)| \leq 1$, it follows that this solution is trapped in the region where $|\eta(t)| < 1$ $\implies$ $|u_2(t)| \leq |u_1(t)|$ for all $t > 0$. This proves the lemma

Completing the proof of the theorem,

1. suppose that we have a second solution $Y(t)$ that lies in $C_M$ for all time.

2. So we must have $Y(t) \rightarrow 0$ as $t \rightarrow \infin$ 

3. Suppose $Y(0) = (x_0', \epsilon)$, where $x_0' \neq x_0$ 

4. Any solution with initial value $(x,\epsilon)$, with $x_0 < x<x_0'$ must tend to the origin (continuous dependence and no crossing of solutions may occur)
   1. So, we may assume that $x_0'$ is as close as we like to $x_0$ 

5. We will approximate $Y(t) - X(t)$ by a solution of the variational equation.

6. Let $U(t)$ denote the solution of the variational equation $U' = DF_{X(t)}U$, satisfying $u_1(0) = x_0' - x_0, u_2(0) = 0$ 
7. The above lemma applies to $U(t)$, so that $|u_2(t)| \leq |u_1(t)|$ for all $t$
8. We have $|u_1'| = |\lambda u_1 + f_{11}(t)u_1 + f_{12}(t)u_2| \geq \lambda|u_1| - (|f_{11}(t)|+ |f_{12}(t)| )|u_1|$ 
   1. But $|f_{11} + f_{12}| \rightarrow 0$ as $\epsilon \rightarrow 0$, so we have $|u_1'| \geq K|u_1|$ , for some $K > 0$
   2. Hence $|u_1(t) |\geq C e^{Kt}$ for $t \geq 0$ 
      1. $|u'_1(t)| \geq KCe^{Kt}$, so if $u_1(t) < Ce^{Kt}$, we'd have a contradiction
9. $Y(t) \rightarrow 0 $ by assumption
10. But then the distance between $Y(t)$ and $U(t)$ must become large if $u_1(0) \neq 0$ 
    1. I think they mean $Y(t)$ and $X(t)$ which should both tend towards origin as t increases
    2. but if the distance between gets large, we arrive at a contradiction, since they must actually get closer to each other since they converge to the same point
11. So $U(t) = 0 \implies Y(t) = X(t)$ 
12. Also, we claim that $X(t)$ tends to the origin tangentially to the $y-$axis
    1. this follows immediately from the fact that we may choose $\epsilon$ small enough so that $X(t)$ lies in $C_M$ no matter how large $M$ is. 
    2. The slope of $X(t)$ tends to $\pm \infin$ as $X(t)$ $\rightarrow (0,0)$ 

#### Higher Dimensional Saddles

Suppose $X' = F(X)$ where $X \in \R^n$ 

Suppose that $X_0$ is an equilibrium solution for which the linearized system has $k$ eigenvalues with negative real parts and $n-k$ eigenvalues with positive real parts

Then the local stable, unstable sets are not generally curves, Rather, they are "submanifolds" of dimension $k$ and $n-k$ respectively

This means there is a linear change of coordinates in which the local stable set is given near the origin by the graph of a $C^\infin$ function $g: B_r \rightarrow \R^{n-k}$ 

that satisfies $g(0) - 0$, and all partial derive of $g$ vanish at the origin

$B_r$ is the disk of radius $r$ centered at the origin in $\R^k$ 

The local unstable set is a similar graph over an $n-k$ dimensional disk

Each of these graphs is tangent at the equilibrium point to the stable and unstable subspaces at $X_0$ 

Hence, they only meet at $X_0$ 

Im wondering if they meant that dimensions are swapped since in the example, we have 2 negative eigenvalues, and the dimension of the space of stable solutions is 2.

the example on page 174 really illustrates this well

$u' = -u \\ 'v = -v \\ w' = w$ is a linear system

we have 2 negative eigenvalues, 1 positive value

### 8.4 Stability

#### a stable equilibrium definition

An equilibrium is said to be stable if nearby solutions stay nearby for all future time

Precise Definition:

Suppose $X^* \in \R^n$ is an equilibrium point for the diff. eqn. $X' = F(X)$ 

Then $X^*$ is a stable equilibrium point *if* 

$\forall$ neighborhood $\mathcal{O}$ of $X^*$ in $\R^n$, there is a neighborhood $\mathcal{O_1}$ of $X^*$ in $\mathcal{O}$ such that every solution $X(t)$ with $X(0) = X_0 \in \mathcal{O_1}$ is defined and remains in $\mathcal{O}$ for all $t > 0$ 

#### asymptotic stability

If $\mathcal{O_1}$ can be chosen above so that we have $\lim_{t\rightarrow \infin} X(t) = X^*$, then we say that $X^*$ is asymptotically stable

#### unstable

$X^*$ is an equilibrium that isn't stable $\equiv$ $X^*$ is an unstable equilibrium

This means that there is a neighborhood of $\mathcal{O}$ of $X^*$ such that

for every neighborhood $\mathcal{O_1}$ of $X^*$ in $\mathcal{O}$, 

there is at least one solution $X(t)$ starting at $X(0) \in \mathcal{O_1}$ that does not lie entirely in $\mathcal{O}$ for all $t > 0$ 

#### sinks are asymptotically stable and therefore stable

#### sources and saddles are examples of unstable equilibria 

#### Example of a stable, but not asymptotically stable equilibrium

the origin in $\R^2$ for a linear equation $X' = AX$ where $A$ has pure imaginary eigenvalues

This is not that important since the slightest nonlinear perturbation will destroy its character.

even a small linear perturbation can make a center into a sink or source

Thus when the linearization of the system at an equilibrium point is hyperbolic, we can immediately determine the stability of that point.

Unfortunately, many important equilibrium points that arise in applications are nonhyperbolic, making it hard to figure out the stability of an equilibrium...?

### 8.5 Bifurcations

We will go over some simple examples of bifurcations that occur for nonlinear systems

Consider the family of systems

$X' = F_a(X)$ 

where $a$ is a real parameter

We assume that $F_a$ depends on $a$ in a $C^\infin$ fashion

A bifurcation occurs when there is a "significant" change in the structure of the solutions of the system as $a$ varies

The simplest types of bifurcations occur when the number of equilibrium solutions changes as $a$ varies

#### Recall the elementary bifurcations we encountered in Chapter 1 for first order equations $x' = f_a(x)$ 

if $x_0$ is an equilibrium point, and if $f_a'(x) \neq 0$ small changes in $a$ do not change the local structure near $x_0$ 

that is, $x' = f_{a+\epsilon}(x)$ has an equilibrium point $x_0(\epsilon)$ that varies continuously with $\epsilon$ for $\epsilon$ small

This is an immediate consequence of the implicit function theorem

##### Example, saddle-node bifurcation: $x' = x^2 + a$ 

single equilibrium point at $x = 0$, when $a = 0$ 

$f_0'(0) = 0$, but $f_0 '' (0) \neq 0$ 

for $a > 0$, no equilibrium points

for $a < 0$, pair of equilibrium points

A bifurcation occurs as the parameter passes through $a = 0$ 

This type of bifurcation is called a **saddle-node bifurcation**

#### Saddle-node bifurcation

In such a bifurcation, there is an interval about the bifurcation value $a_0$ and another interval $I$ on the $x-$axis in which the diff. eq. has

1. 2 equilibrium points in $I$, if $a < a_0$
2. 1 equilibrium point in $I$, if $a = a_0$ 
3. 0 equilibrium points in $I$ if $a > a_0$ 

Of course, we could switch the signs, and the bifurcation could take place the other way

#### Theorem. Saddle-Node Bifurcation

Suppose $x' = f_a(x)$ is a first-order differential equation for which

1. $f_{a_0}(x_0) = 0$ 
2. $f_{a_0}'(x_0) = 0$
3. $f_{a_0}'' \neq 0$ 
4. $\frac{\partial f_{a_0}}{\partial a}(x_0) \neq 0$ 

Then this differential equation undergoes a saddle-node bifurcation at $a = a_0$ 

Proof in book.

This is my restatement 

let $x_0$ be an equilibrium point

$f_{a_0}(x_0) = 0$ 

If $\frac{\partial f_{a_0}}{\partial a}$ is invertible $\equiv$ its determinant is nonzero $\equiv$ it is nonzero

THEN there exists an open set $U$ of $\R$ containing $x_0$ such that there exists a unique continuously differentiable function $a: U \rightarrow \R$ 

$a(x_0) = a$ and $f_{a(x_0)}(x_0) = 0$ for all $x_0$ in $U$

so if $x_0$ is in $U$, it is an equilibrium point for the equation $x' = f_{a(x_0)}(x_0)$ 

$\frac{\partial a}{\partial x}(x) = -\frac{\frac{\partial f}{\partial x}}{\frac{\partial f}{\partial a}}$ 

using the assumptions, we have $a'(x_0) = 0$

Differentiating again and using assumptions:

$a''(x_0) \neq 0$ 

the graph of $a = a(x)$ is concave up or concave down, so for certain values of $a$, if we drew a horizontal line through $a$ in the $xa$-plane, this horizontal line could intersect 0, 1, or 2 points on the $a = a(x)$ curve

##### Why are these typical bifurcations for first order equations?

We must have both

1. $f_{a_0}(x_0) = 0$ 
2. $f'_{a_0}(x_0) = 0$ 

if $x' = f_a(x)$ is to undergo a bifurcation when $a = a_0$ 

Just by looking at the graph, we get that there are at least two points $x_1, x_2$ s.t. $f_{a_0}(x_1) = f_{a_0}(x_2)$, so at some point $a$, these two points will be on the $x-$axis? 

Generically (in the sense of section 5.6), the next higher order derivatives at $(x_0, a_0)$ will be nonzero

these are the conditions for a saddle-node bifurcation

#### Example (Pitchfork Bifurcation)

$x' = x^3 - ax$ 

three equilibria: $x = 0, x = \pm \sqrt{a}$ 

when $a > 0$, when $a \leq 0$, $x = 0$ is the only equilibrium point

####  Bifurcations in Higher Dimensions

##### Example

$x' = x^2 + a \\ y' = -y$

when $a = 0$, this is one of the systems considered in section 8.1

unique equilibrium point at origin, and the linearized system has a $0$ eigenvalue

when $a > 0$, $x' > 0$, so all solutions move to the right, the equilibrium point disappears

When $a < 0$, we have a pair of equilibria, $(\pm \sqrt{-a}, 0)$ 

Linearized equation is $X' = \begin{pmatrix} 2x & 0 \\ 0 & -1 \end{pmatrix}X$

at $(\sqrt{a}, 0)$: $A = \begin{pmatrix} 2\sqrt{a} & 0 \\ 0 &-1 \end{pmatrix}$ 

so we have a saddle since we have a negative and a positive eigenvalue

at $(-\sqrt{a}, 0)$ , we have two negative eigenvalues, so we have a sink

Note: solutions on the liens $x = \pm \sqrt{-a}$ remain for all time on these lines since $x' = 0$ on these lines

Solutions tend directly to the equilibria since $y' = -y$ 

​	so if $y > 0$, $y $ decreases and vice versa

##### Example (polar coordinates)

$r' = r-r^3 \\ \theta' = \sin^2(\theta) + a$ 

the origin is always an equilibrium point since $r' = 0$ when $r = 0$ 

no other equilibria when $a > 0$ since, $\theta' > 0$ 

​	so at $(1, \theta)$, even though we get $r' = 0$, the solution moves counterclockwise

​	at any nonzero starting radius, we have that it moves away from the starting point since the change in angle is always nonzero

When $a =0$, we can have more equilibria:

$\sin^2(\theta) = 0$ at $\theta = 0, \theta = \pi$ and $r = 1$ 

1. When $-1 <a < 0$

we get four equilibria on the circle $r = 1$

​	as $\sin^2(\theta) = -a$ is solvable when $-a \in (0, 1)$ 

​	$\sin(\theta) = \pm\sqrt{-a}$

​	$\sin(\theta + \pi) = -\sin(\theta )$

​	and since $\sin(\theta)$ takes on any value from $(-1, 1)$ twice in a $2\pi$ length interval

​	we have $\theta_\pm$, and $\theta_\pm +\pi$ 

​	where $0 < \theta_+ < \pi/2$ and $-\pi/2 < \theta_{-} < 0$ 

The flow of this system takes straight rays through the origin $\theta = $ constant to other straight rays

​	this is due to $\theta'$ only depending on $\theta$ and not on $r$ 

​	is this when the rays take on $\theta = \theta_\pm, \theta \_\pm + \pi$ ? I think so yes

The unit circle is invariant in the sense that any solution that starts on the circle remains there for all time, because $r' = 0$ on the circle,

 and all solutions tend towards the unit circle $r' > 0$ if $0 < r < 1$ 

we have sinks at two of the equilibria

and saddles at the other two

 $r' < 0$, if $ r > 1$ 

also observe when $\theta'$ is negative or positive 

2. When $a = 0$, the $x-$axis, i.e, $\theta = 0, \pi$ is invariant, and all nonzero solutions on this line tend to the equilibrium at points at $x = \pm 1$ 

​	$r > 1 \implies r' < 0$, $0 <r < 1 \implies r' > 0$  

In the upper half plane, $\theta' > 0$ so all other solutions in this region wind counterclockwise about origin, and tend to $x = -1$, since $0 < \theta < \pi$ and once $\theta \rightarrow \pi$, $\theta' \rightarrow 0$ 

since solutions are al throughout the $x-$axis, it acts as a barrier so no other solutions can wind more than $\pi$ around the plane about origin

the lower half plane has all solutions tending towards $x = 1$, with $\theta \rightarrow 2\pi$ 

3. When $a > 0$

$\theta' > 0$ everywhere

and we have a periodic solution on the circle $r = 1$, since $r' = 0$ when $r = 1$ 

and all nonzero solutions are attracted to it

The dramatic change is caused by a pair of saddle-node bifurcations at $a = 0$

---

The previous examples all featured bifurcations that occur when the linearized system has a zero eigenvalue (at a = 0)

##### Example: (Hopf Bifurcation)