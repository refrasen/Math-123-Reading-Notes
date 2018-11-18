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

##### Notation: Conservative Systems, Potential Energy, Conservative Force Field

There is a **smooth** function $U: \R^n \rightarrow \R$ such that

$F(X) = - (\frac{\partial U}{\partial x_1}(X), \frac{\partial U}{\partial x_2}(X), . . ., \frac{\partial U}{\partial x_n}(X)) = - \text{grad }U(X)$ 

* the negative sign is traditional
* such a force field is called *conservative* 

**definition:** if we have a force field $F(X)$ and there is a function $U(X)$ such that $F(X) = - \text{grad }U(X)$, then $F(X)$ is a conservative force field 

**Associated system of differential equations** is the **conservative system**

$X' = V \\ V' = -\frac{1}{m}\text{grad }U(X)$, lowkey, $V' = \frac{1}{m}F(X)$  

is called a *conservative system*

**potential energy** of a **conservative system**

The function $U$ is called the *potential energy* of the system

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

Proof: $X(t)$ is the path of a particle moving under the influence of a central force field.

