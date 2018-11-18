# Math 123 Chapter 9

# Global Nonlinear Techniques

### Warning: None of these techniques works for ALL nonlinear systems

## 9.1 Nullclines

For a system in the form 

$x_1' = f_1(x_1, . . ., x_n) \\ \vdots \\ x_n' = f_n(x_1, . . ., x_n)$

##### the $x_j$-nullcline is the set of points were $x_j'$ vanishes

$\equiv$ the set {$P$ point: $f_j(P) =0$} 

$x_j$-nullclines *usually* separate $\R^n$ into a collection of regions in which the $x_j$-components of the vector field point in either the positive or negative direction

$\implies$

##### If we determine all of the nullclines, then this allows us to decompose $\R^n$ into a collection of open sets, in each of which the vector field points in a "certain direction"

in $x,y$, $x$-nullclines divide $\R^2$ into regions where vector field points either to the left or to the right, $y-$nullclines divide $\R^2$ into regions where vector field points either up or down

intersection of these nullclines are equilibrium points 

##### basic regions: regions between the nullclines

in $\R^2$: not vertical, nor horizontal: must point NE, NW, SE, SW

#### example: $x' = y - x^2 \\ y' = x-2$ 

$x' = 0 \iff y = x^2$ parabola

 $y' = 0 \iff x = 2$ vertical line

Where do these two curves meet: $(2,4)$

**By first choosing one point in each of these regions, and then determining the direction of the vector field at that point, we can decide the direction of the vector field at all points in the basic region**

$(2,4)$ is a saddle: can tell from the direction field and the linearized system at $(2,4)$ 

**we can also fill in approximate behavior of solutions everywhere in the plane** **using nullclines and direction fields**

* where do all solutions eventually end up?
* are some regions invariant?
* cross one of the nullclines into an invariant region(?) 
* tend to equilibrium?
* (in next example) when are solutions tangent to nullclines?
  * I believe it's when the $x_j$ nullcline has all $x_i$ components set to $0$ except for $x_j$ itself
    * in planar: for $x' = 0$, it happens on vertical lines, i.e., $x = a$ 

#### example: Heteroclinic Bifurcation

 $x' = x^2 -1 \\ y' = -xy + a(x^2 -1)$ 

$x$-nullclines: $x = \pm 1$

$y$-nullclines $xy = a(x^2-1)$ 

equilibrium points $(\pm1, 0)$ 

$x' = 0$ on $x = \pm1$, so the vector field is tangent to these nullclines

$x = \pm 1$ is a vertical line

x-nullclines tell us when the solutions are going up or down i.e., are vertical

Also: $ y' = \begin{cases} -y & x = 1 \\ y & x = -1 \end{cases}$ 

Solutions tend to $(1,0)$ on $x = 1$ 

Solutions tend away from $(-1, 0)$ along $x = -1$ 

The above discussion is valid for all $a \in \R$ 

**<u>a = 0</u>** 

​	$x' = x^2 -1 \\ y' = -xy$

​	so $y' = 0$ along the axes

​	**vector field tangent to the $x$-axis**

​	vector field given by $x' = x^2 -1 $ on $x$-axis

​	when $-1 < x < 1$, solutions on $x$-axis go to the left towards $(-1, 0)$ and away from $(1,0)$ 

​	when $x < -1$, solutions on $x$-axis go to the right towards $(-1, 0)$ 

​	when $x > 1$, solutions on $x$-axis go to the right away from $(1,0)$ 

​	Combining this with the vertical lines: on $x = 1$, solutions tend towards, on $x = -1$, solutions tend away: both equilibria are saddles

​	**vector field is not tangent to the $y$-axis** 

​	$x' = -1, y' = 0$, so solutions on $y$-axis travel to the left

##### **notice: one branch (the left branch) of the unstable curve through (1,0) coincides with the right branch of the stable curve through (-1,0)**

* solutions travel from one saddle to the other on this curve
* therefore, these solutions are called heteroclinic solutions or saddle connections

###### **This rarely happens, but when it does, you can expect a bifurcation**

<u>**a is not equal to 0**</u>  

​	$x$-nullclines remain the same, but $y$-nullclines change: $y = a(x^2-1)/x$ 

​	<u>**a > 0**</u>

​		in particular: when $-1 < x < 1, y = 0$

​		$x' < 0$, points to the left

​		$y' = a(x^2-1) < 0$ points south 

​		no longer have heteroclinic connection

​		the right side of the stable curve for $(-1,0)$ must come from $y = \infin$ in the upper half plane

​		the left portion of the unstable curve for $(1,0)$ must descend to $y = -\infin$ in the lower half plane

​		when $a = 0$, all solutions stayed in either the upper or lower plane

​		but with $a > 0$ solutions can now travel from upper half to lower half between $x = \pm 1$ 

​		so the bifurcation at $a = 0$ opens the door for certain solutions to make this transit 

## 9.2 Stability of Equilibria

### Liapunov Method

##### basin of attraction

the set of all initial conditions with solutions that tend to the equilibrium point

Let $L: \mathcal{O} \rightarrow \R$ be

1. differentiable
2. defined on open set $\mathcal{O}$ in $\R^n$ 
   1. $\mathcal{O}$ contains an equilibrium point $X^*$ of the system $X' = F(X)$ 

Consider the function $\dot{L}(X) = DL_X(F(X))$

if $\phi_t(X)$ is the solution of the system passing through $X$ when $t = 0$:

$\dot{L}(X) = \frac{d}{dt}|_{t=0} L\circ \phi_t(X)$ by the Chain Rule

explanation:

​	as $ \frac{\partial L(X)}{\partial X} = DL_X$, and $X = \phi_0(X)$

​	and $F(X) = \frac{\partial \phi_0(X)}{\partial t}$

If $\dot{L} < 0 \implies$ $L$ decreases along the solution curve through $X$ 

### Liapunov Stability Theorem

Let $X^*$ be an equilibrium point for $X'= F(X)$. Let $L: \mathcal{O} \rightarrow \R$ be a differentiable function defined on an open set $\mathcal{O}$ containing $X^*$. Suppose further that

(a) $L(X^*) = 0 $ and $L(X) > 0$ if $X \neq X^*$

(b) $\dot{L} \leq 0$ in $\mathcal{O} - X^*$

Then $X^*$ is stable. Furthermore, if $L$ also satisfies

(c) $\dot{L} < 0$ in $\mathcal{O} - X^*$ 

then $X^*$ is asymptotically stable

Proof: https://d1b10bmlvqabco.cloudfront.net/attach/jl6rzi97ruv48w/gw9jba2wp696ys/jnns33jqe297/lyapunov.pdf

---

* A function satisfying (a) and (b) is called a **Liapunov function** for $X^*$ 
* if (c) holds as well, $L$ is a *strict* Liapunov function.

When finding Liapunov functions:

From class: easy to try $ax^2 + by^2$ 

#### If there's one eigenvalue with real part > 0, we have unstable equilibrium

### Example. (The Nonlinear Pendulum)

A pendulum consists of a light rod of length $l$ to which is attached a ball of mass $m$ 

The other end of the rod is attached to a wall at a point so that the ball of the pendulum moves on a circle centered at this point

position of the mass at time $t$: $(l \sin \theta(t), -l\cos \theta(t))$ 

speed of mass is the length of the velocity vector: $l d\theta/dt$ 

acceleration: $ld^2\theta/dt^2$ 

Forces acting on pendulum: gravity, friction

gravitational force = $mg$ acting in the downward direction

component of this force tangent to the circle of motion: $-mg\sin\theta$ 

force due to friction is proportional to velocity and is given by $-bld\theta/dt$ , $b > 0$ 

when $b = 0$, we have an ideal pendulum

**Newton's law gives second order differential equation:**

$ml\frac{d^2\theta}{dt^2} = -bl \frac{d\theta}{dt}-mg\sin \theta$ 

let $m = l = g = 1$, 

$\frac{d^2\theta}{dt^2} = -b \frac{d\theta}{dt} - \sin\theta$ 

let $v = \frac{d\theta}{dt}$ , and we get the system: 

$\theta' = v$ 

$v' = -bv - \sin \theta$ 

Two equilibrium points (mod $2\pi$):

$\theta = 0$, $v = 0$ (downward rest)

$\theta = \pi, v = 0$ (upward rest): unstable

$\begin{pmatrix} 0 & 1 \\ 1 & -b\end{pmatrix}$ eigenvalues: $\lambda_{1,2} = \frac{-b \pm \sqrt{b^2 + 4}}{2} > 0$

For downward equilibrium:  $\begin{pmatrix} 0 & 1 \\ -1 & -b\end{pmatrix}$,

if $b = 0$, pure imaginary

if $b > 0$, have negative real parts, so asymptotically stable 

Consider the energy function: $E(\theta, v) = \frac{1}{2}v^2 + 1 - \cos \theta$ 

$\dot{E} = vv' + \sin \theta \theta' = -bv^2$ 

so $\dot{E} \leq 0$ so the origin is a stable equilibrium

if $b = 0$, $\dot{E} \equiv 0$ $\implies$ $E$ is constant along all solutions, plot level curves of $E$ to see where the solution curves reside

see book for more on this example...

### Invariant set $\mathcal{P}$

for each $X \in \mathcal{P}$, $\phi_t(X)$ is defined and in $\mathcal{P}$ for all $t \in \R$ 

#### Positively Invariant

for each $X \in \mathcal{P}$, $\phi_t(X)$ is defined and in $\mathcal{P}$ for all $ t\geq 0$  

### Entire Solution of a system

A set of the form {$\phi_t(X)| t \in \R$}

### Lasalle's Invariance Principle

Let <u>$X^*$ be an equilibrium point for $X' = F(X)$ and</u> let <u>$L: \mathcal{U} \rightarrow \R$ be a Liapunov function for $X^*$, where $\mathcal{U}$ is an open set containing $X^*$</u>. Let <u>$\mathcal{P} \sub \mathcal{U}$ be a neighborhood of $X^*$ that is closed. Suppose that $\mathcal{P}$ is positively invariant and that there is no entire solution in $P - X^*$ on which $L$ is constant</u>. Then $X^*$ is asymptotically stable, and $\mathcal{P}$ is contained in the basin of attraction of $X^*$ 

#### Example: Damped Pendulum, $X^* = (0,0)$ 

$\theta' = v \\ v' = -bv - \sin \theta$ 

* Note: There are other initial positions in the basin of $(0,0)$ not in $\mathcal{P}$ 

### $\omega$-limit points or $\omega$-limit set of the solution $X(t)$ 

set of all points that are limit points of a given solution

### $\alpha$-limit points or $\alpha$-limit set of a solution $X(t)$ 

set of all points $Z$ such that $\lim_{n \rightarrow \infin}X(t_n) = Z$ for some sequence $t_n \rightarrow -\infin$ 

### The $\alpha$-limit set and the $\omega$-limit set of a solution that is defined for all $t \in \R$ are closed, invariant sets

## 9.3 Gradient Systems

A gradient system on $\R^n$ is a system of differential equations of the form

### $X' = - \text{grad }V(X)$

#### where $V: \R^n \rightarrow \R$ is a $C^\infin$ function, and $\text{grad }V = (\frac{\partial V}{\partial x_1}, . . ., \frac{\partial V}{\partial x_n})$ 

the vector field $\text{grad }V$ is called the **gradient** of $V$ 

Notice: $- \text{grad }V(X) = \text{grad}(-V(X))$ 

### $DV_X(Y) = \text{grad }V(X)\cdot Y$  

The derivative of $V$ at $X$ evaluated at $Y = (y_1, . . ., y_n) \in \R^n$ is given by the dot product of the vectors $\text{grad }V(X)$ and $Y$. This follows immediately from 

$DV_X(Y) = \sum_{j=1}^n \frac{\partial V}{\partial x_j}(X)y_j$ 

Let $X(t)$ be a solution of the gradient system with $X(0) = X_0$, and let $ \dot V: \R^n \rightarrow \R$ be the derivative of $V$ along this solution

$\dot V(X) = \frac{d}{dt}|_{t=0}V(X(t))$ 

### $V$ is strictly decreasing along nonconstant solutions of the system $X' = -\text{grad }V(X)$ 

Moreover: $\dot V(X) = 0$ **if and only if** $X$ is an equilibrium point

Proof by chain rule: $DV_{X}(X') = \text{grad }V(X)\cdot X' = \text{grad }V(X) \cdot(-\text{grad }V(X)) = -|\text{grad }V(X)|^2 \leq 0$ 

#### If $X^*$ is an isolated critical point that is a minimum of $V$, then $X^*$ is an asymptotically stable equilibrium point of the gradient system

### Level Surfaces of $V: \R^n \rightarrow \R$ 

These are subsets $V^{-1}(c)$ with $c \in \R$ 

so the points $X$ in $\R^n$ such that $V(X) = c$ 

if $X \in V^{-1}(c)$ is a **regular point**, that is, $\text{grad }V(X) \neq 0 \iff \dot V \neq 0$, then $V^{-1}(c)$ looks like a surface of dimension $n-1$ near $X$ 

---

Proof:

This means (by renumbering) $\partial V/\partial x_n(X) \neq 0$ 

We may use Implicit Function Theorem:

$V: \R^{n-1 + 1} \rightarrow \R$ is continuously differentiable 

$\R^{n-1 + 1}$ has coordinates $(x_1, . . . , x_{n-1}, x_n)$ 

??? $V(x_1, . . ., x_{n-1}, x_n) = 0$??? no, it equals $c$, but I suppose we could easily go

$V(x_1, . . . , x_n{-1}, x_n) - c = 0$ 

and because $\partial V/\partial x_n(X) \neq 0$ :

There is a $C^\infin$ function $g: \R^{n-1} \rightarrow \R$ such that, near $X$, the level set $V^{-1}(c)$ is given by

$V(x_1, . . ., x_{n-1}, g(x_1, . . ., x_{n-1})) = c$ 

$\equiv V(x_1, . . . , x_{n-1}, g(x_1, . . ., x_{n-1})) - c = 0$, for all $X \in U$, where $U$ is a neighborhood of $(x_1, . . ., x_{n-1})$

Near $X$, $V^{-1}(c)$ looks like the graph of $g$ 

---

$n=2$: $V^{-1}(c)$ is a simple curve through $X$ when $X$ is a regular point 

if all point in $V^{-1}(c)$ are regular points, then $c$ is a **regular value** for $V$ 

$n =2 $: if $c$ is a regular value, then the level set $V^{-1}(c)$ is a union of simple (nonintersecting) curves

If $X$ is nonregular point for $V$ $\implies $ $\text{grad }V(X) = 0$, so $X$ is a **critical point** for $V$ since all partial derivatives of $V$ vanish at $X$ 

If $Y$ is a vector tangent to the level surface $V^{-1}(c)$ at $X$, then we can find a curve $\gamma(t)$ in this level set for which $\gamma'(0) = Y$. Since $V$ is constant along $\gamma, $ it follows that $DV_X(Y) = \frac{d}{dt}|_{t=0} V\circ \gamma(t) = 0 $ 

**grad $V(X)$ is perpendicular to every tangent vector to the level set $V^{-1}(c)$ at $X$** 

$\equiv$ **The vector field grad $V(X)$ is perpendicular to the level surfaces $V^{-1}(c)$ at all regular points of $V$** 

---

Summarized in the following:

### Properties of Gradient Systems

For the system $X' = -\text{grad }V(X)$: 

1. If $c$ is a regular value of $V$, then the vector field is perpendicular to the level set $V^{-1}(c)$ 
2. The critical point of $V$ are the equilibrium points of the system
3. If a critical point is an isolated minimum of $V$, then this point is an asymptotically stable equilibrium point

#### Example: $V(x,y) = x^2(x-1)^2 + y^2$ 

* $X' = F(X) = -\text{grad }V(X)$ 
  * $x' = -2x(x-1)(2x-1) \\ y' = -2y$ 
* Equilibrium points: $(0,0), (1/2, 0), (1,0)$
* Linearized systems at the EP give
  * $(0,0), (1,0)$ are sinks, $(1/2, 0)$ is a saddle
* Invariant sets:
  * $x, y$-axes
  * $x = \frac{1}{2}$, $x = 1$ 
* stable curve at $(1/2, 0)$ is $x = 1/2$, unstable curve at $(1/2, 0)$ is the interval (0,1) on the $x$-axis
  * if $x < 1/2$, $x' < 0$, if $x > 1/2$ $x' > 0$ 
* All solutions tend to one of three equilibria     

### If $Z$ is an $\alpha$-limit point or an $\omega$-limit point of a solution of a gradient flow, then $Z$ is an equilibrium point 

---

Proof:

if $Z$ is an $\omega$-limit point, using the proof of Lasalle's Invariance Principle from $9.2$, 

$V$ is constant along the solution through $Z$ 

so $\dot V(Z) = 0$ , and so $Z$ must be an equilibrium point 

For the case of $\alpha$-limit point $Z$ of $X' = -\text{grad }V(X)$: $Z$ is an $\omega$ limit point of $X' = \text{grad }V(X)$ so $\text{grad }V(Z) = 0$ 

---

**If a gradient system has only isolated equilibrium points, this result implies that every solution of the system must tend either to infinity or to an equilibrium point.**

In the example: $V(x,y) = x^2(x-1)^2 + y^2$ 

$V^{-1}([0,c])$ are closed, bounded, and **positively invariant** under the gradient 

so each solution entering such a set is defined for all $t\geq 0$, and tends to one of the three equilibria 

the solution through every point does enter such a set , since the solution through $(x,y)$ enter the set $V^{-1}([0, c_0])$, where $V(x,y) = c_0$ 

---

for the linearization of a gradient system at an equilibrium point $X^*$ is the matrix $[a_{ij}]$, where

$a_{ij} = -(\frac{\partial ^2 V}{\partial x_i \partial x_j})(X^*) = -(\frac{\partial ^2 V}{\partial x_j \partial x_i})(X^*) = a_{ji}$

so this matrix is symmetric, and symmetric matrices have only real eigenvalues

### For a gradient system $X' = -\text{grad }V(X)$, the linearized system at any equilibrium point has only real eigenvalues.

## 9.4 Hamiltonian Systems

A Hamiltonian system in $\R^2$ is a system of the form 

$x' = \frac{\partial H}{\partial y}(x,y) \\ y' = -\frac{\partial H}{\partial x}(x,y)$ 

where $H: \R^2 \rightarrow \R$ is a $C^\infin$ function called the **Hamiltonian function**

### Example: Undamped Harmonic Oscillator

$x' = y \\ y' = -kx$ , $k > 0$ 

$H(x,y) = \frac{1}{2}y^2 + \frac{k}{2}x^2$ 

$H(x,y) = \frac{1}{2}y^2 + C(x)$

$\frac{\partial H}{\partial x} = C'(x) = kx$ 

$C(x) = \frac{k}{2}x^2$ 

### Example: Ideal Pendulum

$\theta'' = v \\ v' = -\sin \theta$ 

$E(\theta, v) = \frac{1}{2}v^2 + 1 - \cos \theta$ serves as a Hamiltonian function (Hamiltonian function unique up to adding a constant)

Hamiltonian function is a **first integral** or **constant of the motion**: $H$ is a constant along every solution of the system , or $\dot H \equiv 0$ 

because: $\dot H = \frac{\partial H}{\partial x}x' + \frac{\partial H}{\partial y}y' = \frac{\partial H}{\partial x}\frac{\partial H}{\partial y} + \frac{\partial H}{\partial y}(-\frac{\partial H}{\partial x}) = 0$

this $\implies$

---

### For a Hamiltonian system in $\R^2$, $H$ is constant along every solution curve

We can draw the phase portrait without solving the system.

We simply plot the level curves $H(x,y) = \text{constant}$ 

Equilibrium points are critical point of $H$, that is where both partial derivatives of $H$ vanish

#### Example: $x' = y \\ y' = -x^3 + x$ 

$H(x,y) = \frac{x^4}{4}- \frac{x^2}{2} + \frac{y^2}{2} + \frac{1}{4}$ 

has minimum of $0$ at $(\pm 1, 0)$ 

other equilibrium point: $(0,0)$ 

Linearized system:

$X' = \begin{pmatrix} 0 & 1 \\ 1 - 3x^2 & 0 \end{pmatrix}X$ 

at $(0,0)$, we have a saddle with eigenvalues $\lambda = \frac{0 \pm \sqrt{0 - 4(-1)}}2 = \pm 1$

at $(\pm 1, 0)$, the eigenvalues are $\pm \sqrt{2}i$ so a center for the linearized system

The equilibrium points remain centers in the nonlinear system and 

stable and unstable curves at origin match up exactly: we have solutions that tend to origin in both forwards and backward time: **homoclinic solutions/orbits**

---

### Eigenvalues of the linearized system for a planar Hamiltonian system at equilibrium points are either $\pm \lambda$ or $\pm i\lambda$, $\lambda \in \R$ 

## 9.5 Exploration