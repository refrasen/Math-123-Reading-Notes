# Math 123 General Notes Chapter 10

## Closed Orbits and Limit Sets

undamped harmonic oscillator equation: all nonzero solutions are periodic 

### 10.1 Limit Sets

Recall: $Y \in \R^n$ is an $\omega$-limit point for the solution through $X$ if there is a sequence $t_n \rightarrow \infin$ such that $\lim_{n\rightarrow \infin}\phi_{t_n}(X) = Y$ $\equiv$ the solution curve through $X$ accumulates on the point $Y$ as time moves forward

The set of all $\omega$-limit points of the solution through $X$ is the $\omega$-limit set of $X$ and is denoted by $\omega(X)$ 

The $\alpha$-limit potins and the $\alpha$-limit set with $\alpha(X)$ are defined by replacing $t_n \rightarrow \infin$ with $t_n \rightarrow -\infin$ 

by a *limit set* what is meant is a set of form $\omega(X)$ or $\alpha(X)$ 

Examples:

* If $X^*$ is an asymptotically stable equilibrium, it is the $\omega$-limit set of every point in its basin of attraction.
* Any equilibrium is its own $\alpha$- and $\omega$-set
* A periodic solution is the $\alpha$-limit and $\omega$-limit set of every point on it
  * such a solution may also be the $\omega$-limit set of many other points

Examples: **example of limit set that is not equilibria** 

the system $r' = \frac{1}{2}(r-r^3)\\\theta' = 1$

all nonzero solutions tend to the periodic solution that resides on the unit circle in the plane, so the $\omega$-limit set of any nonzero point is this closed orbit

---

the system **example of limit set that is not equilibria** 

$x' = \sin x(-0.1\cos x - \cos y)\\ y' = \sin y(\cos x - 0.1 \cos y)$ 

* equilibria that are saddles at the corners of the square:
  * (0, 0), (0, $\pi$), ($\pi$, 0), ($\pi$, $\pi$)
  * others would be mod $2\pi$ 
  * I guess other equilibria: $-0.1 \cos x = \cos y$ AND $\cos x = 0.1 \cos y$ 
    * I guess this would occur: $x = \pi/2$, $x = 3\pi/2$ 
* Heteroclinic solutions connecting equilibria from $(0,0)$ to $(0,\pi)$ to $(\pi, \pi)$ to $(\pi, 0)$ to $(0,0$) again
* spiral source: $(\pi/2, \pi, 2)$
* Any solution coming from the spiral source accumulate on the four heteroclinic solutions connecting the equilibria, so the $\omega$-limit set of any point is the square bounded by $x = 0, \pi$ and $y = 0, \pi$  

---

#### Proposition

1. If $X$ and $Z$ lie on the same solution, then $\omega(X) = \omega(Z)$ and $\alpha(X) = \alpha(Z)$ 
2. If $D$ is a closed, positively invariant set and $Z$ $\in D$, then $\omega(Z) \sub D$ and similalry for negatively invariant sets and $\alpha$-limits
3. A closed invariant set and, in particular, a limit set, contains the $\alpha$-limit and $\omega$-limit sets of every point in it

Proof: 

(1): Suppose $Y \in \omega(X)$, $\phi_s(X) = Z$. If $\phi_{t_n}(X) \rightarrow Y$, then: $[\phi_{t_n -s}(Z) = \phi_{t_n}(X)] \rightarrow Y$ 

$\phi_{0}(X) = \phi_{-s}(Z)$, so $\phi_{t_n}(X) = \phi_{t_n -s}(Z)$ 

so $Y \in \omega(Z)$ 

(2): if $\phi_{t_n}(Z) \rightarrow Y \in \omega(Z)$ as $t_n \rightarrow \infin$, then we have $t_n \geq 0$ for sufficiently large $n$ so that $\phi_{t_n}(Z) \in D$ (because $D$ is positively invariant)

Therefore $Y$ $\in D$ since $D$ is closed: i.e, contains the limit points of all sequences made up of terms from $D$ 

(3): follows immediately from (2)

### 10.2 Local Sections and Flow Boxes (lots of terminology)

Local behavior of the flow associated with $X' = F(X)$ near a given point $X_0$ that is NOT an equilibrium point

#### **transverse line** at a non equilibrium point $X_0$, denoted by $l(X_0)$: 

the straight line through $X_0$ that is perpendicular to the vector $F(X_0)$ based at $X_0$ 

Parameterize $l(X_0)$ as follow:

* $V_0$ is the unit vector based at $X_0$ and perpendicular to $F(X_0)$ 
* $h: \R \rightarrow l(X_0)$ is defined by $h(u) = X_0 + uV_0 = l(X_0)$ 

---

#### Local Section

$F(X)$ is continuous, so the vector field is not tangent to $l(X_0)$, at least in some open interval in $l(X_0)$ surrounding $X_0$. This open subinterval containing $X_0$ is called a **local section** at $X_0$ 

At each point of a local section $\mathcal{S}$, the vector field points "away from" $\mathcal{S}$, so solutions must cut across a local section

In particular, $F(X) \neq 0$ for $X \in \mathcal{S}$

---

#### **flow box** in a neighborhood of $X_0$:

* gives a complete description of the behavior of the flow in a neighborhood of a nonequilibrium point by means of a special set of coordinates

intuitive description of the flow in a flow box: Points move in parallel straight lines at constant speed

---

##### map $\Psi$ from a neighborhood $\mathcal{N}$ to a neighborhood of $X_0$ 

Given a local section $\mathcal{S}$ at $X_0$, we may **construct a map $\Psi$ from a neighborhood** $\mathcal{N}$ of the origin in $\R^2$ to a neighborhood of $X_0$ as follows:

**Given $(s,u) \in \R^2$ we define $\Psi(s,u) = \phi_s(h(u))$** 

<u>Just for understanding:</u>

* from $X_0$, we go along $l(X_0)$ until $X_0 + uV_0$ 
* then we move along the flow for the system from that point for $s$ time

<u>What maps to what:</u>

$\Psi$ maps the vertical line $(0,u)$in $\mathcal{N}$ to the local section $\mathcal{S}$ (to some point in $l(X_0)$)

$\Psi$maps horizontal lines to pieces of solution curves of the system

<u>When is it 1-1</u>

if we choose $\mathcal{N}$ sufficiently small, the map $\Psi$ is <u>one to one</u> on $\mathcal{N}$

<u>Usual neighborhood</u>

Usually take $\mathcal{N}$ in the form {$(s,u)| |s| < \sigma$}, where $\sigma > 0$

##### <u>Notation for a flow box</u>

Sometimes we write $\mathcal{V}_\sigma = \Psi(\mathcal{N})$ and call $\mathcal{V}_\sigma$ the **flow box** at (or about) $X_0$ 

---

if $X \in \mathcal{V}_\sigma$, then $\phi_t(X) \in \mathcal{S}$ for a unique $t \in (-\sigma, \sigma)$ 

If $\mathcal{S}$ is a local section, the solution through a point $Z_0$ may reach $X_0 \in \mathcal{S}$ at a certain time $t_0$ 

**This "time of first arrival" at $\mathcal{S}$ is a continuous function of $Z_0$** 

so if $Y_0$ near $Z_0$ then $t_0$ for $Y_0$ is close to $t_0$ for $Z_0$ ?

#### Proposition

Let $\mathcal{S}$ be a local section at $X_0$ and suppose $\phi_{t_0}(Z_0) = X_0$ 

Let $\mathcal{W}$ be a neighborhood of $Z_0$. Then there is an open set $\mathcal{U}\sub \mathcal{W}$ containing $Z_0$ and a continuous function $\tau: \mathcal{U} \rightarrow \R$ such that $\tau(Z_0) = t_0$ and

$\phi_{\tau(X)}(X) \in \mathcal{S}$ 

for each $X$ $\in \mathcal{U}$ 

(Proof on page 218)

* $F(X_0) = (\alpha, \beta) \neq (0,0)$
* Let $Y = (y_1, y_2)$
* $\eta(Y) = Y\cdot F(X_0) = \alpha y_1 + \beta y_2$
* $Y \in l(X_0)$ if and only if $\eta(Y) = Y\cdot F(X_0) = (X_0 + V)\cdot F(X_0) = X_0 \cdot F(X_0)$ 
* Define $G: \R^2 \times \R \rightarrow \R$: $G(X, t) = \eta(\phi_t(X)) = \phi_t(X)\cdot F(X_0)$ 
* $G(Z_0, t_0) = X_0\cdot F(X_0)$ because $\phi_{t_0}(Z_0) = X_0$ 
* and $\frac{\partial G}{\partial t}(Z_0, t_0) = |F(X_0)|^2 \neq 0$ 
* Implicit Function Theorem 
  * $G(X, t) - G(Z_0, t_0) = 0$ when $X = Z_0, t = t_0$ 
  * and $\frac{\partial[ G(X, t) - G(Z_0, t_0)]}{\partial t} = \frac{\partial G}{\partial t}(X, t)$ and at $(Z_0, t_0)$ is nonzero
  * so there's $\tau: \R^2 \rightarrow \R$ s.t. $\tau(Z_0) = t_0$ and is a smooth function defined on a neighborhood $\mathcal{U}_1$ of $(Z_0, t_0)$ and $G(X, \tau(X)) \equiv G(Z_0, t_0) = X_0 \cdot F(X_0)$
* So $\phi_{\tau(X)}(X)$ belongs to the transverse line
* If $\mathcal{U} \sub \mathcal{U}_1$ is sufficiently small neighborhood of $Z_0$, then $\phi_{\tau(X)}(X) \in \mathcal{S}$ 

### 10.3 The Poincare Map

Closed orbits may be stable, asymptotically stable, or unstable

stable: all solutions starting at some neighborhood of the closed orbit will stay in some bigger(ish) neighborhood of the orbit

AS: all solutions starting at some neighborhood will stay in some bigger(ish) neighborhood but also tend towards the closed orbit 

**honestly, see chapter 8 for the definitions and replace equilibrium with closed orbit**

---

#### Tool Used To Determine the Stability of Closed Orbits

Given a closed orbit $\gamma$, there is an associated *Poincare map* for $\gamma$ 

Near a closed orbit, this map is defined as follows:

Choose $X_0 \in \gamma$ and let $\mathcal{S}$ be a local section at $X_0$ 

We consider the **first return map on $\mathcal{S}$** 

​	This is the function $P$ that associates to $X \in \mathcal{S}$ the point $P(X) = \phi_t(X) \in \mathcal{S}$, where $t$ is the smallest positive time for which $\phi_t(X) \in \mathcal{S}$ 

$P$ may not be defined on all points on $\mathcal{S}$ because the solutions through certain points in $\mathcal{S}$ may never return to $\mathcal{S}$ 

But for sure: $P(X_0) = X_0$ (because $\gamma$ is a closed orbit and $X_0 \in \gamma$

<u>The Poincare map is defined and continuously differentiable in a neighborhood of $X_0$</u>

**proof:**

Define $f(X,s) = P(X) - \phi_s(X)$ so that $f(X_0) = 0$ 

and $\frac{\partial f}{\partial s}(X,s) =  -F(\phi_s(X))$ and at $(X_0, t_0)$, where $t_0$ is the smallest time such that $\phi_{t_0}(X_0) = X_0$ , because $X_0$ is a nonequilibrium point, $F(X_0) \neq 0$ 

so IFT: there exists a smooth function $\tau: \mathcal{U} \rightarrow \R$ $\mathcal{U}$ is a neighborhood of $X_0$ 

with $\tau(X_0) = t_0$ and

$f(X, \tau(X)) = 0$ for all $X \in \mathcal{U}$ 

so for all $X \in \mathcal{U}$ $P(X) = \phi_{\tau(X)}(X)$ $\blacksquare$

In the case of planar systems: 

a local section is a subset of a straight line through $X_0$ so we may regard this local section as a subset of $\R$ and take $X_0 = 0 \in \R$ 

Thus the Poincare map is a real function taking 0 to 0

<u>Proves if $|P'(X_0)| < 1$ $\gamma$ is AS</u>

If $|P'(0)| < 1$, it follows that $P(x) = ax + \text{higher-order terms}$, where $|a| < 1$

Thus, for $x$ near $0$, $P(x)$ is closer to $0$ than $x$ 

or $P(X)$ is closer to $X_0$ than $X$ if $P'(X_0) < 1$? 

This means: the solution through the corresponding point in $\mathcal{S}$ moves closer to $\gamma$ after one passage through the local section

Continuing, we see that each passage through $\mathcal{S}$ brings the solution closer to $\gamma$, and so we see that $\gamma$ is **asymptotically stable.**

We obtain the following:

##### Proposition (important part)

Let $X' = F(X)$ be a planar system and suppose that $X_0$ lies on a closed orbit $\gamma$. Let $P$ be the Poincare map defined on a neighborhood of $X_0$ in some local section. If $|P'(X_0)| < 1$, then $\gamma$ is asymptotically stable 

* for $X \in S$ $P(X)$ return $\phi_s(X)$, where $s > 0$ and $\phi_s(X) \in S$ 

##### Example: $r' = r(1-r) \\ \theta' = 1$ 

* closed orbit lying on the unit circle $r = 1$ 
  * the solution is given by $(\cos t, \sin t)$ when the initial condition is $(1, 0)$ $\in \R^2$
* local section lying along the positive real axis because $\theta' = 1$ 
* given any $x \in (0, \infin)$ we have $\phi_{2\pi}(x, 0)$, which also lies on the positive real axis
  * $\theta(t) = t$
  * We have the poincare map $P: \R^+ \rightarrow \R^+$ from the above
  * where $P(x) = \phi_{2\pi}(x,0)$ 
  * and $P(1) = \phi_{2\pi}(1,0) = (\cos 2\pi, \sin 2\pi) = (1, 0)$ 
* Need to calculate $P'(x)$ 
  * already know $\theta(t) = t$ 
  * need $r(2\pi)$ 
  * $\frac{dr}{dt} = r(1-r)$ 
  * $\int \frac{1}{r(1-r)}dt = t + \text{constant }$
  * end up with $r(t) = \frac{xe^t}{1-x+xe^t}$ 
* $P(x) = r(2\pi) = \frac{xe^{2\pi}}{1 - x + xe^{2\pi}}$
* $P'(1) = \frac{e^{2\pi}(e^{2\pi}) - e^{2\pi}(-1 + e^{2\pi})}{e^{4\pi}} = \frac{1}{e^{2\pi}} < 1$ and $> 0$ 
* so $|P'(1)| < 1$ meaning the periodic solution is AS

### 10.4 Monotone Sequences in Planar Dynamical Systems

Let $X_0, X_1, . . . \in \R^2$ be a finite or infinte sequence of distinct points on the solution curve through $X_0$ 

We say that the sequence is **monotone along the solution** if $\phi_{t_n}(X_0) = X_n$ with $0 \leq t_1 < t_2 \cdots .$ 

Let $Y_0, Y_1, . . .$ be a finite or infinite sequence of points on a line segment $I$ in $\R^2$ 

We say that this sequence is **monotone along** $I$ if $Y_n$ is between $Y_{n-1}$ and $Y_{n+1}$ in the natural order for all $n \geq 1 $ 

A sequence of points may be on the intersection of a solution curve and a segment $I$; they may be monotone along the solution curve but not along the segment or vice versa

However, this is impossible if the segment is a local section in the plane

#### Proposition:

Let $S$ be a local section for a planar system of differential equations and let $Y_0, Y_1, Y_2$ . . . be a sequence of distinct points in $S$ that lie on the same solution curve. If **this sequence is monotone along the solution**, <u>then</u> it is also **monotone along** $S$ 

**Proof:**

* Uses the fact that a local section... the flow moves parallel to each other and in the same direction?
* uniqueness of solutions so solutions do not cross
* if you can connect two points with an arc and that arc doesn't cross a certain path? it means that 
  * connectedness?

#### Proposition

For a planar system, suppose that $Y \in \omega(X)$. Then the solution through $Y$ crosses any local section at no more than one point. The same is true if $Y \in \alpha(X)$ 

**Proof**: 

I don't understand why if $Y_1, Y_2$ are distinct points on the solution going through $Y$ and $Y_1, Y_2 \in S$ and $Y \in \omega(X)$ , then $Y_1, Y_2 \in \omega(X)$ 

### 10.5 The Poincare-Bendixson Theorem

#### Theorem (Poincare-Bendixson)

Suppose that $\Omega$ is a <u>nonempty</u>, <u>closed</u>, and <u>bounded</u> <u>limit set</u> of a planar system of differential equations that <u>contains no equilibrium point</u>. Then $\Omega$ is a closed orbit