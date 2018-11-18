# Math 123 Reading Notes Chapter 13

## 13 Applications in Mechanics

### 13.1 Newton's Second Law

#### Notation

##### force field F:

$F$: a vector field on the (configuration) space of the particle, which in our case is $\R^n$ 

$F(X)$ is the force exerted on a particle located at position $X$

---

Connection between physical concept of force field and mathematical concept of diff. eq.: Newton's second law: $F = ma$ 

$mX'' = F(X)$ 

---

As a system:

$X' = V \\ V' = \frac{1}{m}F(X)$   derivative of position is velocity, derivative of velocity is acceleration $= F/m$ 

where $V = V(t)$ is the velocity of the particle

This is a system on $\R^n \times \R^n$ 

often called a *mechanical system with n degrees of freedom* 

---

A solution $X(t) \sub \R^n$ of the second-order equation is said to lie in *configuration space*

The solution $(X(t), V(t))$ $\sub \R^n \times \R^n$ lies in the *phase space* or *state space* 

---

#### Examples

##### Example: Undamped Oscillator 

mass moves in one dimension 

$x(t)$: position at time $t$, $x: \R \rightarrow \R$ 

$mx'' = -kx$ is the diff. eqn. governing this motion

$k > 0$

Force field at point $x \in \R$ is thus $-kx$ 

##### Example: two dimensional harmonic oscillator

$X(t) = (x_1(t), x_2(t))$ $\in \R^2$

The force field is $F(X) = -kX$, with $mX'' = -kX$  

with solutions in configuration space

$x_1(t) = c_1\cos(\sqrt{k/m}t) + c_2 \sin(\sqrt{k/m}t)$

$x_2(t) = c_3 \cos(\sqrt{k/m}t) + c_4 \sin (\sqrt{k/m}t)$ 

for some choices of $c_j$, use chapter 6 methods to check this

---

#### Concepts from Multivariable Calculus

##### dot product (or inner product) of two vectors

$X, Y \in \R^n$, denoted: $X\cdot Y$ 

Defined by: $X\cdot Y = \sum_{i =1}^n x_iy_i$ 

where $X = (x_1, . . ., x_n)$ 

thus $X\cdot X = |X|^2$

If $X, Y: I \rightarrow \R^n$ are smooth functions:

$(X\cdot Y)' = X'\cdot Y + X\cdot Y'$

My Personal Check on $\R^2$:

$x_1y_1 + x_2y_2$

$x_1'y_1 + x_1y_1' + x_2'y_2 + x_2y_2'$

$\sum_{i=1}^n x_i'y_i + x_iy_i'$ 

##### Gradient of a function $g: \R^n \rightarrow \R$ 

$\text{grad } g(X) = (\frac{\partial g}{x_1}(X), . . ., \frac{\partial g}{x_2}(X))$

$\text{grad }g$ is a vector field on $\R^n$ (see chapter 9)

##### Composition of two smooth function $g \circ F$ , and their derivative w.r.t. $t$ 

where $F: \R \rightarrow \R^n$ 

$g: \R^n \rightarrow \R$ 

$\frac{d}{dt}g(F(t)) = \text{grad }g(F(t))\cdot F'(t)$ $= \sum_{i = 1}^n \frac{\partial g}{\partial x_i}(F(t))\frac{\partial F_i}{dt}(t)$

Proof from chain rule on $g\circ F$ :

$g(F_1(t), . . ., F_n(t))$

$\frac{\partial g}{\partial F_1}\frac{\partial F_1}{\partial t}(t)$ $+. . . + \frac{\partial g}{\partial F_n}\frac{\partial F_n}{\partial t}(t)$ 

##### Cross product or vector product $U\times V$ of vectors $U, V \in \R^3$ 

$U\times V = (u_2v_3 - u_3v_2, u_3v_1 - u_1v_3, u_1v_2 - u_2v_1) \in \R^3$ 

I believe this is equal to 

$\det \begin{pmatrix} i & j & k \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{pmatrix}$ 

$U \times V = -V \times U = |U||V|N\sin\theta $

where $N$ is a unit vector perpendicular to $U$ and $V$

orientations of the vectors $U, V, $ and $N$ given by the "right-hand rule"

$\theta$ is the angle between $U$ and $V$ 

$U \times V = 0$ if and only if one vector is a scalar multiple of the other

if $U \times V \neq 0$, then $U \times V$ is perpendicular to the plane containing $U$ and $V$ 

if $U$ and $V$ are function of $t$ in $\R$:

$\frac{d}{dt}(U \times V) = U' \times V + U \times V'$ 

Proof:

$(u_2'v_3 + u_2v_3' - u_3'v_2 - u_3v_2', u_3'v_1 + u_3v_1' - u_1'v_3 - u_1v_3', u_1'v_2 + u_1v_2' - u_2'v_1 - u_2v_1' )$

$= (u_2'v_3 -u_3'v_2, u_3'v_1 - u_1'v_3, u_1'v_2 - u_2'v_1) + (u_2v_3' - u_3v_2', u_3v_1' - u_1v_3', u_1v_2' - u_2v_1')$

###  13.2 Conservative Systems

#### Notation: Conservative Systems, Potential Energy, Conservative Force Field

There is a **smooth** function $U: \R^n \rightarrow \R$ such that

$F(X) = - (\frac{\partial U}{\partial x_1}(X), \frac{\partial U}{\partial x_2}(X), . . ., \frac{\partial U}{\partial x_n}(X)) = - \text{grad }U(X)$ 

* the negative sign is traditional
* such a force field is called *conservative* 

##### **definition:** if we have a force field $F(X)$ and there is a function $U(X)$ such that $F(X) = - \text{grad }U(X)$, then $F(X)$ is a conservative force field 

##### **Associated system of differential equations** is the **conservative system**

$X' = V \\ V' = -\frac{1}{m}\text{grad }U(X)$, lowkey, $V' = \frac{1}{m}F(X)$  

is called a *conservative system*

**potential energy** of a **conservative system**

##### The function $U$ is called the *potential energy* of the system

$U$ should be called *a* potential energy since adding a constant to it does not change the force field $- \text{grad }U(X)$ 

---

#### Examples

##### $F(X) = -kX$ , planar harmonic oscillator force field

* is conservative, with $U(X) = \frac{1}{2}k|X|^2$ as a potential energy
* $|X|^2 = x_1^2 + . . . + x_n^2$ 
* $\frac{\partial U}{\partial x_i} = kx_i$
* $-(kx_1, . . ., kx_n) = - \text{grad }U(X)$

For any moving particle $X(t)$ of mass $m$, the *kinetic energy* is defined to be:

$K = \frac{1}{2}m|V(t)|^2$ 

Notes:

* KE depends on velocity
* PE depends on position

Total Energy is defined on the phase space by:

$E = K + U$ 

Notes about total energy:

* constant along any solution curve of the system
* $E$ is a constant of the motion or a first integral for the flow
  * first integral means that it is constant along every solution of the system

---

#### Theorem (Conservation of Energy)

Let $(X(t), V(t))$ be the solution curve of a conservative system. Then the total energy $E$ is constant along this solution cruve

*Proof*:

Compute $\dot E$, with $E = \frac{1}{2}m|V(t)|^2 + U(X(t))$ 

so $\dot E = \frac{d}{dt}(E)$ 

and $V' = - \text{grad }U/m$

$X' = V$ 

and find that it equals $0$ 

---

Remark: this type of system may be written in Hamiltonian Form

$x_i' = \frac{\partial H}{\partial y_i} \\ y_i' = -\frac{\partial H}{\partial x_i}$ , where $H: \R^n \times \R^n \rightarrow \R$ is the *Hamiltonian function*

* $H$ is constant along solutions of such a system

#### Writing a Conservative System in Hamiltonian Form

**change of variables**

*momentum vector $Y = mV$*

set $H = K + U = \frac{1}{2m}\sum y_i^2+ U(x_1, . . ., x_n)$

Remember:

 $X' = V$

$V' = -\frac{1}{m}\text{grad }U(X)$ 

so 

$x_i' = \frac{\partial H}{\partial y_i} = \frac{1}{2m}(2mv_i) = v_i$, which is exactly what we want for $X'$ 

and $\frac{\partial H}{\partial x_i} =  \frac{\partial U}{\partial x_i}$ so:

$y_i' = -\frac{\partial U}{\partial x_i} $

and $V' =\frac{Y'}{m} = -\frac{\text{grad U}}{m}$

So this works.

---

### 13.3 Central Force Fields

##### Definition of central force field $F$ 

A force field $F$ is *central* if $F(X)$ points directly toward or away from the origin for every $X$

In other words: $F(X)$ is always a scalar multiple of $X$

###### $F(X) = \lambda(X)X$, where $\lambda(X)$ depends on $X$ 

**we often tacitly exclude from consideration a particle at the origin**

* many central force fields are not defined (or are "infinite") at the origin

Theoretically: a function $\lambda(X)$ could vary for different values of $X$ on a sphere given by $|X| = \text{constant}$  

* **in a conservative force field, this is not the case**

#### Proposition: What we can say about a central, conservative force field

Let $F$ be a conservative force field. Then the following statements are equivalent

1. $F$ is central
2. $F(X) = f(|X|)X$
3. $F(X) = -\text{grad }U(X)$ *and* $U(X) = g(|X|)$ 

###### In a conservative and central force field, $\lambda(X)$ is the same for all $X$ on a sphere, so we only consider a function $f(|X|)$, so $F(X) = f(|X|)X$

* as opposed to $\lambda(X)$ which depends on any $X$, not the length of $X$

 Proof:

$(3) \implies (2)$:

1. Use chain rule:
   1. $\frac{\partial U}{\partial x_j} = \frac{\partial g}{\partial x_j}(|X|) = \frac{\partial g}{\partial |X|}\frac{\partial |X|}{\partial x_j} = g'(|X|)\frac{\partial }{\partial x_j}(x_1^2 + x_2^2 + x_3^2)^{1/2} = \frac{g'(|X|)}{|X|}x_j$
2. Prove (2) with $f(|X|) = \frac{g'(|X|)}{|X|}$ 

$(2) \implies (1)$ 

from with $f(|X|) = \frac{g'(|X|)}{|X|} = \lambda(X)$

so substituting into (2) we obtain (1): $F(X) = \lambda(X)X$ 

$(1) \implies (3)$ 

Must prove $U$ is constant on each sphere:

$S_{\alpha} = $ {$X \in \R^n| |X| = \alpha > 0$} (standard definition of a sphere)

* any two points in $S_{\alpha}$ can be connected by a curve in $S_{\alpha}$ 
* Suffices to show that $U$ is constant on *any* curve in $S_{\alpha}$  
* therefore: if $J \sub \R$ is an interval and $\gamma: J \rightarrow S_{\alpha}$ is a smooth curve, we must show that the derivative of $U\circ \gamma$ is $\equiv 0$ 

$\frac{d}{dt}U(\gamma(t)) = \text{grad }U(\gamma(t))\cdot \gamma'(t)$ 

$\text{grad }U(X) = -F(X) = -\lambda(X)X$ because (1)

so $\frac{d}{dt}U(\gamma(t)) = -\lambda(\gamma(t))\gamma(t)\cdot \gamma'(t)$

$= -\frac{\lambda(\gamma(t))}{2}\frac{d}{dt}|\gamma(t)|^2 = 0$

since $\frac{d}{dt}|\gamma(t)|^2 = \gamma(t)\cdot \gamma(t) = 2\gamma(t)\cdot \gamma'(t)$

and for each $t$ in the interval $J$, $|\gamma(t)| =\alpha$

so $|\gamma(t)| \equiv \alpha$ 

which means$\frac{d}{dt}|\gamma(t)|^2 = \frac{d}{dt}\text{constant}$ $= 0$ 

---

#### Proposition. A particle moving in a central force field in $\R^3$ always moves in a fixed plane

Proof: 

$X(t)$ is the path of a particle moving under the influence of a central force field.

$\frac{d}{dt}(X\times V) = V\times V + X \times V'$ $= 0 + X \times X'' = 0$

since $X''$ is a scalar multiple of $X$: $X'' = V' = \frac{1}{m}F(X) = \frac{1}{m}\lambda(X)X$

Therefore, $Y = X(t)\times V(t)$ is a constant vector w.r.t. $t$ 

If $Y \neq 0$, this means that $X$ and $V$ **always** lie in the plane orthogonal to $Y$, which proves the proposition. (always because $Y$ is constant for any $X(t), V(t)$)

If $Y = 0$, this means that $X'(t) = g(t)X(t)$ for some real function $g(t)$

$\implies$ the velocity vector of the moving particle is always directed along the line through the origin and the particle, as is the force on the particle

$\equiv$ the particle moves along the same line through the origin

Proof of this fact:

$(x_1(t), x_2(t), x_3(t))$: coordinates of $X(t)$ 

three separable differential equations

$\frac{dx_k}{dt} = g(t)x_k(t)$, for $k = 1, 2, 3$ 

Integrating, $x_k(t) = e^{h(t)}x_k(0)$, where $h(t) = \int_0^t g(s)ds$ 

Therefore: $X(t)$ is a scalar multiple of $X(0)$, and so $X(t)$ moves in a fixed line and thus a fixed plane

---

##### angular momentum of the system: $m(X \times V)$, $m = $ mass of particle

##### Corollary (Conservation of Angular Momentum): Angular momentum is constant along any solution curve in a central force field

This comes straight from the proof of the preceding proposition, where we have $\frac{d}{dt}(X\times V) = 0$ 

---

#### Conservative Central Force Fields and Angular Momentum ($\R^3$) 

the particle remains for all time in a plane, which we can take to be $x_3 = 0$ (for simplicity, and I believe we can use change of variables to make it this way anyway)

##### angular momentum is given by the vector: $(0, 0, m(x_1v_2 - x_2v_1))$

since $x_3 = 0$ and I believe, $v_3 = 0$, since the particle must remain in the plane $x_3 = 0$ 

##### $l = m(x_1v_2 - x_2v_1)$  

* the function $l$ is constant along solutions since the angular momentum is constant along solutions

* In the planar case, $l$ is called the angular momentum

Using polar coordinates: $x_1 = r\cos\theta$, $x_2 = r \sin \theta$ 

$v_1 = x_1' = r'\cos\theta - r\sin\theta\theta'\\ v_2 = x_2' = r'\sin\theta + r\cos\theta \theta'$  

Then:

$x_1v_2 - x_2v_1 = r\cos\theta(r'\sin\theta + r\cos\theta \theta') - r\sin(r'\cos \theta - r\sin\theta \theta ') = r^2(\cos^2\theta + \sin^2\theta)\theta' = r^2\theta'$ 

so in polar coordinates: $l = mr^2\theta'$

---

#### Kepler's Laws (one of them at least)

##### Notation

###### $A(t) = $ area swept out by the vector $X(t)$ in the time from $t_0$ to $t$ 

* $dA = \frac{1}{2}r^2 d\theta$ 

###### areal velocity: $A'(t) = \frac{1}{2}r^2(t)\theta'(t)$ 

* the rate at which the position vector sweeps out the area

##### Kepler observed that the line segment joining a planet to the sun sweeps out **equal areas in equal times**, so $A' = \text{constant}$ 

* We have proved that this is true for any particle moving in a conservative force field
* Question: is the conservative part necessary?

#### Two constants of the motion/ first integrals for a conservative system generated by a central force field:

##### total energy

##### angular momentum

Ending notes:

* generally, first integrals do not exist for diff. eqn.'s because of chaos

### 13.4 The Newtonain Central Force System

#### Setting up the system:

* this system deals with the motion of a single planet orbiting the sun
* Assume the sun is fixed at the origin in $\R^3$ and that the relatively small planet exerts no force on the sun
* sun exerts a force on a planet given by *Newton's law of gravitation* $\equiv$ *inverse square law* 
  * the sun exerts a force on the planet located at $X \in \R^3$ with a magnitude that is $gm_sm_p/r^2$ 
    * $m_s$ is the mass of the sun
    * $m_p$ is the mass of the planet
    * $g$ is the gravitational constant
  * The direction of the force is towards the sun
* Newton's law yields $m_pX'' = -gm_sm_p \frac{X}{|X|^3}$
  * $X'' = -gm_s\frac{X}{|X|^3}$ 
* We change units so that constants are normalized to one and the equation becomes:

$X'' = F(X) = -\frac{X}{|X|^3}$ 

* $F(X)$ is now the force field

As a system:

##### $X' = V \\ V' = -\frac{X}{|X|^3}$ 

This system is called the **Newtonian central force system**

---

#### It is a central force field and it is conservative

since $\frac{X}{|X|^3} = \text{grad }U(X)$ 

With Potential Energy: $U(X) = -\frac{1}{|X|}$

$ = -\frac{1}{\sqrt{x_1^2 +  . . . + x_3^2}}$ 

so deriving w.r.t. to $x_i$ 

we have three basic function: $1/x$, $\sqrt{x}$ and $x^2$ 

$\frac{1}{x_1^2 + . . . + x_3^2}\frac{1}{2\sqrt{x_1^2+. . . + x_3^2}}2x_i$

$= \frac{x_i}{|X|^3}$ , 

##### $F(X)$ is not defined at $0$: the force field becomes infinite as the moving mass approaches collision with the stationary mass at the origin

---

We restrict our attention to particles moving in the plane $\R^2$ (as in the previous section)

So, we look at solutions in the 

##### configuration space $C = \R^2 - ${$0$}

We denote the 

##### phase space by $P = (\R^2 - ${$0$})$\times \R^2$ 

We visualize phase spaces as the collection of all tangent vectors at each point $X \in C$ 

##### Tangent plane to the configuration space at $X$: $T_{X} = ${$(X,V)| V \in \R^2$}

##### $P = \cup_{X \in C} T_X$ is the tangent space to the configuration space, a subset of $\R^4$ 

##### The dimension of the phase space is four

we can cut this dimension in half by making use of the two known first integrals: total energy and angular momentum

Recall:

First, that energy is constant

second, that $E(X,V) = K(V) + U(X) = \frac{1}{2}|V|^2 - \frac{1}{|X|}$ 

Let $\Sigma_h$ denote the subset of $P$ consisting of all points $(X,V)$ with $E(X,V) = h$ 

##### $\Sigma_h$ is called the energy surface with total energy $h$ 

###### If $h \geq 0$

then $\Sigma_h$ meets each $T_X$ in a <u>circle of tangent</u> vectors satisfying

$|V|^2 = 2(h + \frac{1}{|X|})$ 

The radius of these circles in the tangent plane at $X$ tends to $\infin$ as $X \rightarrow 0$ and decreases to $2h$ as $|X| \rightarrow \infin$ 

Note: Is it a circle because of the whole, $V'$ depends on $F(X)$, which in a conservative central force field like this one depends on $|X|$? I honestly don't know. Or is it because $E$, when $X$ is fixed, depends on $|V|^2$?

###### If $h < 0$ 

the structure of the energy surface $\Sigma_h$ is different

If $|X| > -1/h$ $\implies$ there are no vectors in $T_X \cap \Sigma_h$ 

​	$-|h| + 1/|X| < -|h| + |h|  = 0$, so impossible for $|V|^2$ to equal such a number

If $|X| = -1/h$ $\implies$ only the zero vector in $T_X$ 

​	The circle $r = -1/h$ in configuration space is therefore known as the **zero velocity curve**

​	as for any $X$, such that $|X| = r$, we must have $V = 0$ in order for $E(X, V) = h$  

​	if $X$ lies inside the zero velocity curve, then $T_X$ meets the energy surface in a circle of tangent vectors as before

---

#### Polar Coordinates in configuration space, new variables $(v_r, v_\theta)$ 

##### $V = v_r\begin{pmatrix} \cos\theta \\ \sin \theta\end{pmatrix} + v_\theta\begin{pmatrix} - \sin \theta \\ \cos\theta \end{pmatrix}$ 

##### $V = X' = r'\begin{pmatrix} \cos\theta \\ \sin \theta \end{pmatrix} + r\theta'\begin{pmatrix} -\sin \theta \\ \cos\theta \end{pmatrix}$ 

###### $r' = v_r$, $\theta' = v_\theta/r$ 

Differentiating:

$-\frac{1}{r^2}\begin{pmatrix}\cos\theta \\ \sin\theta \end{pmatrix}$ $= $ $-\frac{X}{|X|^3}$ $= $ $V' = $ $(v_r' - v_\theta \theta')\begin{pmatrix} \cos\theta \\ \sin \theta \end{pmatrix} + (\frac{v_rv_\theta}{r}+v_\theta')\begin{pmatrix} -\sin \theta \\ \cos \theta \end{pmatrix}$ 

Proving the differentiating part, the right most side:

$\frac{\partial V}{\partial r} = r''(\cos \theta, \sin \theta) + \theta'(-\sin \theta, \cos \theta)$ 

$\frac{\partial V}{\partial \theta}= r'(-\sin \theta, \cos \theta) + r\theta'(-\cos \theta, -\sin \theta) + r\theta''(-\sin \theta, \cos \theta)$  

$v_r' = r'' \cdot r'$ (w.r.t $t$)

$v_{\theta }' = r'\theta' + r\theta'' \cdot \theta'$ (w.r.t $t$)

so in front of $(\cos \theta, \sin \theta)$ we have:

$r''r' - r\theta' \theta' = v_r' - v_\theta \theta'$

in front of $(-\sin \theta, \cos \theta)$

$r'\theta' + r' \theta'  + r\theta'' \theta' = v_rv_\theta/r + v_\theta'$

Therefore, in the new coordinates $(r, \theta, v_r, v_\theta)$ the system becomes

##### $r' = v_r \\ \theta' = v_\theta/r \\ v_r' = -\frac{1}{r^2}+ \frac{v_\theta^2}{r} \\ v_{\theta}' = -\frac{v_rv_\theta}{r}$

Explanation:

equating the left most side of the equality above with the right most side, we must have

$v_rv_\theta/ r + v_\theta' = 0$ and $v_r' - v_\theta \theta' = -\frac{1}{r^2}$ 

In these coordinates, total energy is given by

##### $ E(v_r, v_\theta) = \frac{1}{2}(v_r^2 + v_\theta^2)- \frac{1}{r} = h$  

Explanation:

From page 286:

$E(X,V) = \frac{1}{2}|V|^2 - \frac{1}{|X|}$ 

we have $|X| = r$, and $|V|^2 = v_r^2\cos^2\theta + v_r^2 \sin^2\theta + v_\theta^2(\sin^2\theta + \cos^2\theta)$

angular momentum, $l = mr^2\theta'$, now equals, with $m =1$

##### $l = rv_\theta$ 

---

Let $\Sigma_{h,l}$ consist of all points in phase space with total energy $h$ and angular momentum $l$

For simplicity, we will restrict attention to the case where $h < 0$ 

**If $l = 0$, we must have $v_\theta = 0$ $\implies \theta' = 0$ ** 

$\implies$ if $X$ lies *inside* the zero velocity curve, the tangent space at $X$ meets $\Sigma_{h, 0}$ in precisely two vectors of the form

$\pm v_r(\cos \theta, \sin \theta)$, both of which lie on the line connecting $0$ and $X$, one point towards $0$, the other pointing away

On the zero velocity curve, with $|X| = -1/h$, only the zero vector (I'm assuming, we are pointing out the obvious $V = 0$) lies in $\Sigma_{h,0}$.

$\implies$ Each solution in $\Sigma_{h,0}$ lies on a straight line through origin (why? cause of the above):

The solution leaves origin and travels along a straight line until reaching the zero velocity curve, after which time it recedes back to the origin(!)

The vectors in $\Sigma_{h, 0}$ have magnitude tending to $\infin$ as $X \rightarrow 0$ (from earlier discussion, before polar coordinates)$\implies$ these solutions reach the singularity in finite time in both directions (t negative, t positive?). These solutions are called:

##### collision-ejection orbits

**If $l \neq 0$**

If $X$ lies in the zero velocity curve, we have $v_\theta = l/r$ $\implies$

Using $E(v_r, v_\theta)$, 

$r^2v_r^2 = 2hr^2 + 2r - l^2$ $(*)$

The quadratic polynomial in $r$ on the right in Equation $(*)$ must therefore be nonegative

$\implies$ we have restrictions on which $r-$values can occur for $X \in \Sigma_{h,l}$

The graph of this quadratic polynomial is concave down since $h < 0$:

* first derivative w.r.t. $r$?: $4hr + 2$, it is equal to $0$ when $r = 2/(4|h|)$
  * when $r < 2/(4|h|)$, $4hr + 2 > 0$
  * and $r > 2/(4|h|)$ $\implies$ $4hr < -2$ $\implies$ $4hr + 2 < 0$ 
  * so we have a maximum at $r = 2/(4|h|)$
* second derivative: $4h < 0$, which means the rate of change decreases as $r \rightarrow \infin+$ 

**It has no real roots if $l^2 > -1/2h$**

$\implies$ there's no point at which the right hand side of $(*)$ $= 0$

and concave down means that the right hand side remains negative the whole time, but we need nonnegative values

Therefore: the space $\Sigma_{h,l}$ is empty in this case

**If $l^2 = -1/2h$, we have a single root that occurs at $r = -1/2h$**

Therefore: only one $r$-value in $\Sigma_{h,l}$ 

In the tangent plane at $(r, \theta)$:

$v_r = 0$, because $r \neq 0$ and $(*) = 0$ when $r = -1/2h$ $\implies$ $r$ doesn't change, so we remain in a circle

$v_\theta = -2hl$ (since earlier we said $v_\theta = l/r$)

So this represents a circular closed orbit, traversed clockwise if $l < 0$, counterclockwise if $l > 0$ 

**If $l^2 < -1/2h$**: two distinct roots, $\alpha, \beta$

$\alpha < -1/2h < \beta$ and $\alpha > 0$ (since $-b/2a$ in this case is positive)

Let $A_{\alpha, \beta}$: be the annular region $\alpha \leq r \leq \beta$ in the configuration space

Motion in configuration space is confined to $A_{\alpha, \beta}$ (as this is the only time when the right hand side of $(*)$ is nonnegative, assuming we still want $E(v_r, v_\theta) = h$)

#### Proposition

Suppose $h < 0$ and $l^2 < -1/2h$. Then $\Sigma_{h,l} \sub P$ is a two dimensional torus

Proof:

Just read in page 289