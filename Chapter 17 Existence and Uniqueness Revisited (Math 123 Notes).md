# Chapter 17 Existence and Uniqueness Revisited

## 17.1 The Existence and Uniqueness Theorem

$X' = F(X)$

$F: \R^n \rightarrow \R^n$ 

assume $F$ is $C^1$ 

A solution of this system is differentiable $X: J \rightarrow \R^n$ defined on some interval $J \sub \R$ 

such that for all $t \in J$ 

$X'(t) = F(X(t))$ 

### The Existence and Uniqueness Theorem

Consider the IVP:

$X' = F(X)$,    $X(0) = X_0$ 

Suppose $F: \R^n \rightarrow \R^n$   is $C^1$ 

There exists a unique solution of this IVP

More preciesely: There exists $a > 0$ and a unique solution

$X:(-a,a) \rightarrow \R^n$ 

of this diff. eqn. satisfying the initial condition

## 17.2 Proof of Existence and Uniqueness

$F: \R^n \rightarrow \R^n$ 

$F(X) = (f_1(x_1, . . . , x_n), . . . , f_n(x_1, . . ., x_n))$ 

### $DF_X$ denotes the derivative of $F$ at point $X$ 

Two ways to view derivative:

linear map:

for each $U \in \R^n$ 

$DF_X(U) = \lim_{h\rightarrow 0} \frac{F(X+hU) - F(X)}{h}$ 

or matrix point of view:

$DF_X = (\frac{\partial f_i}{\partial x_j})$ 

each derivative is evaluated at $(x_1, . . ., x_n)$ 

$DF: \R^n \rightarrow L(\R^n)$ 

associates linear maps/matrices to each point in $\R^n$ 

---

### norm $|DF_X|$ of the Jacobian matrix $DF_X$ 

$|DF_X| = \text{sup }_{|U|=1}|DF_X(U)|$ 

where $U \in \R^n$ 

$|DF_X(V)| \leq |DF_X||V|$ for any vector $V \in \R^n$ 

Because $F:\R^n \rightarrow \R^n$ is $C^1$ 

the function sending $X \rightarrow DF_X$ is a continuous function

---

Let $\mathcal{O} \sub \R^n$  be an open set.

### a Lipschitz function $F$ on an open set $\mathcal{O}$ 

A function $F: \mathcal{O} \rightarrow \R^n$ is lipschitz on $\mathcal{O}$ 

if $\exists$ a constant $K$ s.t.

$|F(Y) - F(X) \leq K|Y-X|$ 

for all $X, Y \in \mathcal{O}$ 

$K$: Lipschitz constant for $F$ 

#### Locally Lipschitz

$F$ is locally Lipschitz if each point in $\mathcal{O}$ has a neighborhood $\mathcal{O'}$ in $\mathcal{O}$ such that 

the restriction $F$ to $\mathcal{O'}$ is Lipschitz

the Lipschitz constant of $F|\mathcal{O'}$ may vary with each neighborhood $\mathcal{O'}$ 

### Compactness

a set $\mathcal{C} \sub \R^n$ is comapct if $\mathcal{C}$ is closed and bounded

if $f: \mathcal{C} \rightarrow \R$ is continuous and $\mathcal{C}$ is compact, then:

1. $f$ is bounded on $\mathcal{C}$ 
2. $f$ attains its maximum on $\mathcal{C}$ 

### Lemma: a $C^1$ function from an open set in $\R^n$ to $\R^n$ is locally Lipschitz

Suppose that the function $F:\mathcal{O} \rightarrow \R^n$ is $C^1$ Then $F$ is locally Lipschitz

Proof:

*  pick arbitrary point in $\mathcal{O}$ , $X_0$ 
* Let $\epsilon > 0$ be small s.t. the closed ball $\mathcal{O_\epsilon}$ centered on $X_0$ with radius $\epsilon$ is in $\mathcal{O}$ 
* Using Compactness, because $DF_X$ is continuous and $\mathcal{O}_\epsilon$ is closed and bounded, so $\exists K$ upper bound for $|DF_X|$  on the closed ball
* $\mathcal{O}_\epsilon$ is convex, so if $Y, Z$ in the closed ball, $Y+sU$,the straight line, is in the closed ball
  * $U = Z-Y$, $s \in [0,1]$ 
* Let $\psi(s) = F(Y+sU)$
* Chain rule: $\psi'(s) = DF_{Y+sU} (U)$ 
* $F(Z) - F(Y) = \psi(1) - \psi(0) = \int_0^1 DF_{Y+sU}(U)ds$ 
* $|F(Z) -F(Y)| \leq |\int_0^1 DF_{Y+sU}(U)ds| \leq \int_0^1K|U| ds = K|Z-Y|$ 

#### Remark

If $\mathcal{O}$ is convex and if $|DF_X| \leq K$ for all $X \in \mathcal{O}$ then $K$ is a Lipschitz constant for $F|\mathcal{O}$  

---

### The integral and differential forms are equivalent as equations for $X: J \rightarrow \mathcal{O}$ 

We have $X: J \rightarrow \mathcal{O}$ 

* satisfies $X'(t) = F(X(t))$ with $X(0) = X_0$ 

* * then: $X(t) = X_0 + \int_0^t F(X(s)) ds$ 
* satisfies $X(t) = X_0 + \int_0^tF(X(s))ds$ 
  * then $X' = F(X)$, and $X(0) = X_0$ 

#### To prove existence of soln, we use integral form of differential equation

### Proof of Existence 

#### Assumptions

1. $\mathcal{O_\rho}$ is the closed ball of radius $\rho > 0 $ centered at $X_0$ 
2. There is a Lipschitz constant $K$ for $F$ on $\mathcal{O_\rho}$ 
3. $|F(X)| \leq M$ on $\mathcal{O_\rho}$ 
4. Choose $a < \min(\rho/M, 1/K)$ and let $J = [-a, a]$ 

#### We define a sequence of functions $U_0, U_1, . . . $ from $J$ to $\mathcal{O_\rho}$ 

Then, we prove that these functions converge uniformly to a function satisfying the differential equation.

##### Lemma from Analysis (uniform convergence of functions $U_k$)

Suppose $U_k: J \rightarrow \R^n$, $k = 0, 1, 2, . . . $ is a sequence of continuous functions defined on a closed interval $J$ that satisfy:

1. Given $\epsilon > 0$ , there is some $N > 0$ such that for every $p, q > N$ $\max_{t\in J}|U_p(t)-U_q(t)| < \epsilon$ 

Then:

1. There is a continuous function $U: J \rightarrow \R^n$ such that $\max_{t\in J}|U_k(t) - U(t)| \rightarrow 0$ as $k \rightarrow \infin$ 
2. for any $t$ with $|t| \leq a$, $\lim_{k \rightarrow \infin}\int_0^t U_k(s)ds = \int_0^t U(s)ds$ 

##### Defining sequence of function $U_k$: Picard iteration

##### We want to show the image of $U_k:J\rightarrow \R^n$ is contained in $\mathcal{O_\rho}$

$U_0(t) \equiv X_0$ (the initial condition)

$U_1(t) = X_0 + \int_0^t F(U_0(s)) ds = X_0 + tF(X_0)$ 

since $t \in J$, and $J = [-a, a]$, $|t| \leq a$ 

and from assumption 3, $|F(X)| \leq M$ on $\mathcal{O_\rho}$ 

$|U_1(t)-X_0| = |t||F(X_0)| \leq aM$ 

and from assumption 4

$|U_1(t) - X_0| \leq aM \leq \rho$ 

**so $U_1(t)$ is in $\mathcal{O_\rho}$ for all $t \in J$** 

Inductive step: assume $U_k(t)$ has been defined and $|U_k(t) - X_0| \leq \rho$  for all $t \in J$ 

Then let: $U_{k+1}(t) = X_0 + \int_0^t F(U_k(s))ds$ 

$U_k(s) \in \mathcal{O_\rho}$, so the integrand is defined, as $F$ is defined on $\mathcal{O}$ 

**So now we show $U_{k+1}(t) \in \mathcal{O_\rho}$** 

$|U_{k+1}(t)-X_0|$ $\leq \int_0^t |F(U_k(s))ds|$ 

and as we know, $|F(X)| \leq M$ for all $ X \in \mathcal{O_\rho}$ 

and $t \leq a$ 

so $|U_{k+1}(t)-X_0| \leq Ma < \rho$  

**Now show convergence**

First: show $|U_{k+1}(t) - U_k(t)| \leq (aK)^kL$ 

​	$L$ is the maximum of $|U_1(t) - U_0(t)|$ over $t \in [-a, a]$ 

​	$L \leq aM$ 

​	this involves induction, and using Lipschitz condition

and remember $a < 1/K$, so $aK < 1$ meaning $(aK)^k < 1$ 

and since for $\alpha = aK$, the sequence $\alpha^n$ converges to $0$ as $n\rightarrow \infin$

there is indeed a large enough $N$ s.t. for all $r, s > N$

$|U_r(t) - U_s(t)| \leq$ $\sum_{k=N}^\infin |U_{k+1}(t)-U_k(t)|$

since $|U_r(t) - U_{r-1}(t) + U_{r-1}(t)-U_{r-2}(t) + . . . U_{s+1}(t)-U_s(t)|$ = $|U_r(t)-U_s(t)|$

and using triangle inequality... we get that it is less than $\sum_{k =s}^{r-1} |U_{k+1}-U_k|$ 

which is going to be less than the above for sure

and continuing, $\leq \sum_{k=N}^\infin \alpha^kL$ $\leq \epsilon$ 

the "tail" of the geometric series may be made as small as we please 

So using the Lemma from analysis...

we take the limit of

$U_{k+1}(t) = X_0 + \int_0^t F(U_k(s))ds$ 

and arrive at $X(t) = X_0 + \int_0^t F(X(s))ds$ 

### Proof of Uniqueness

Using that a continuous function attains its max on a a compact set

if $X,Y$ are two solutions to the same IVP

$Q = \max|X(t) - Y(t)|, t \in J$

let $t_1$ be the argmax of $|X(t)-Y(t)|$ 

$Q = |X(t_1) - Y(t_1)| = |\int_0^{t_1}(X'(s) - Y'(s))ds| \leq \int_0^{t_1}|F(X(s))- F(Y(s))| ds$

$\leq \int_0^{t_1}K|X(s) - Y(s)|ds$ 

$aKQ$ 

and $aK < 1$ so we have that this is a contradiction unless $Q = 0$ meaning $X(t) = Y(t$ ) 

### Summary

Given any ball $\mathcal{O_{(\rho, X_0)}} \sub \mathcal{O}$

on which

1. $|F(X)| \leq M$
2. $F$ has a Lipschitz constant $K$ 
3. 0 < $a$ < $\min(\rho/M, 1/K)$ 

There is a unique soln $X:[-a, a] \rightarrow \mathcal{O}$ of the diff. eqn. such that $X(0) = X_0$

This result holds if $F$ is $C^1$ 

### Remark: Curves of two solutions cannot cross if $F$ satisfies the hypotheses of the theorem

## 17.3 Continuous Dependence on Initial Conditions

### Theorem: Solutions that start out close together remain close together for $t$ near $t_0$ 

Let $\mathcal{O} \sub \R^n$ be open and suppose $F: \mathcal{O} \rightarrow \R^n$ has Lipschitz constant $K$. 

Let $Y(t), Z(t)$ be solutions of $X' = F(X)$ which remain in $\mathcal{O}$ 

and are defined on the interval $[t_0, t_1]$. 

Then, for all $t \in [t_0, t_1]$ :

$|Y(t)-Z(t)| \leq |Y(t_0)-Z(t_0)|\exp(K(t-t_0))$ 

These solutions do not separate from each other no faster than exponentially

#### Corollary (Continuous Dependence on Initial Conditions)

Let $\phi(t,X)$ be the flow of the system $X' = F(X)$ where $F$ is $C^1$ 

Then $\phi$ is a continuous function of $X$ 

The proof depends on Gronwall's inequality

### Gronwall's Inequality 

Let $u:[0,\alpha] \rightarrow \R$ be continuous and nonnegative

Suppose $C \geq 0$ and $K \geq 0$ are such that

$u(t) \leq C + \int_0^t Ku(s)\, ds$ for all $t \in [0, \alpha]$ 

Then for all $t$ in this interval $u(t) \leq Ce^{Kt}$ 

Proof:

1. Suppose $C > 0$ 
   1. $U(t) = C + \int_0^t Ku(s)ds > 0$ 
      1. from hypothesis, $u(t) \leq U(t)$ 
   2. Differentiate $U'(t) = Ku(t)$ 
   3. $U'(t)/U(t) = Ku(t)/U(t) \leq K$  
   4. $\frac{d}{dt}(\log U(t)) \leq K$
      1. Using $\frac{d}{dt}(\log U(t)) = (1/U(t))*U'(t) = U'(t)/U(t)$ 
   5. $\log(U(t)) \leq \log(U(0)) + Kt$
      1. comes from integrating both sides of inequality in 4. from $0$ to $t$ over change $ds$ 
   6. $U(t) \leq e^{\log U(0)}e^{Kt}$ = $U(0)e^{Kt} = Ce^{Kt}$ 
   7. Therefore: $u(t) \leq Ce^{Kt}$ 
2. $C = 0$ 
   1. apply above argument to a sequence of positive $c_i$ that tend to $0$ as $i  \rightarrow \infin$ 
      1. $U_i(t) = c_i + \int_0^t Ku(s) ds$ 
      2. and $U_i(t) \leq c_ie^{Kt}$ 
      3. and as $i\rightarrow \infin$ , $c_ie^{Kt} \rightarrow 0$ 

### Proof of Theorem

1. let $v(t) = |Y(t)-Z(t)|$ 
2. $Y(t) - Z(t) = Y(t_0) - Z(t_0) + \int_{t_0}^t (F(Y(s))- F(Z(s))) ds$ 
   1. Fundamental Theorem of Calculus
3. $v(t) \leq v(t_0) + \int_{t_0}^t Kv(s) ds$ 
   1. from definition of $v$
   2. from lipschitz hypothesis 
4. Let $u(t) = v(t+t_0)$ 
5. $u(t) = v(t+t_0) \leq v(t_0) + \int_{t_0}^{t+t_0} Kv(s) ds$ 
   1. from 3. 
6. $u(t) \leq v(t_0) + \int_0^t Ku(\tau) d\tau$ 
   1. from 4. and 5. 
   2. change of variables, $\tau = t + t_0$ 
7. $u(t) = v(t+t_0) \leq v(t_0)e^{Kt}$
   1. Gronwall's Theorem
8. $v(t) \leq v(t_0)e^{K(t-t_0)}$ 
9. $\equiv$ $|Y(t) - Z(t)| \leq |Y(t_0) - Z(t_0)|e^{K(t-t_0)}$ 

### Theorem: Continuous Dependence on Parameters

$X' = F_a(X)$ be a system of differential equations for which $F_a$ is continuously diff. in both $X$ and $a$. Then the flow of this system depends continuously on $a$ as well as $X$ 

Proof:

Artificially augment system to obtain

$x_i' = f_i(x_1, . . ., x_n, a)$ for $i = 1, . . ., n$ 

and $a' = 0$ 

so $a$ just remains a constant, and we get the same solutions

Then invoke continuous dependence of solutions on initial conditions to verify that solutions of the original system depend continuously on $a$ as well.

## 17.4 Extending Solutions

### Theorem

Let $\mathcal{O} \sub \R^n$  be open, and let $F: \mathcal{O} \rightarrow \R^n$ be $C^1$ 

Let $Y(t)$ be a solution of $X' = F(X)$ defined on a maximal open interval $J = (\alpha, \beta)$  $\sub \R$ 

with $\beta < \infin$ 

Then given any compact set $\mathcal{C} \sub \mathcal{O}$, there is some $t_0 \in (\alpha, \beta)$ with $Y(t_0) \notin \mathcal{C}$ 

I.e.,:

If a solution $Y(t)$ cannot be extended to a larger time interval, then this solution leaves any compact set in $\mathcal{O}$ 

as $ t\rightarrow \beta$ , $Y(t)$ accumulates on the boundary of $\mathcal{O}$, or else a subsequence $|Y(t_i)|$ tends to $\infin$ (or both)

Proof, page 396 in Hirsch Smale Davey

Proof by contradiction

1. Suppose $\mathcal{C}$ is a compact set that $Y(t)$ is contained in for all $(\alpha, \beta)$ 
2. This means $Y$ is uniformly continuous on $J$ 
3. Since $\mathcal{C}$ is compact, it contains all limits of converging sequences
   1. so: $\lim_{t \rightarrow \beta} Y(t)$ is defined
   2. since in compact (metric) sets$\equiv$ completeness Cauchy sequences always converge
   3. and if we have a sequence $t_i$ s.t. $t_i \rightarrow \beta$ 
   4. ... fill in gaps... so $|t_r - t_s| \rightarrow 0$ since convergent is cauchy
   5. $|Y(t_r) - Y(t_s)|$ $\leq \sum_{k =s}^{r-1} (t_{k+1}-t_k)M$ = $M(t_r - t_s)$ 
   6. so we choose $N$ s.t. for all $r, s > N$, $|t_r - t_s| \leq \epsilon/M$ 
4. $Y(\beta) = \lim_{t\rightarrow \beta} Y(t)$ is defined
5. and using uniform continuity of $F(Y(s))$ we can get $Y(\beta) = Y(\gamma) + \int_\gamma^\beta F(Y(s)) ds$ 
   1. Lipschitz continuity for $F?$ 
6. We get $Y(t) = Y(\gamma) + \int_{\gamma}^t F(Y(s))ds$ for all $t$ between $\gamma$ and $\beta$ so all $t \in [\gamma, \beta]$ 
7. $Y'(\beta)$ $= F(Y(\beta))$ so $Y$ is a solution on $[\gamma, \beta]$ and $Y$ can be extended to $(\alpha, \beta + \delta)$ for $\delta > 0$ 
8. Contradiction since $(\alpha, \beta)$ is maximal interval

#### Corollary

Let 

1. $\mathcal{C}$ be a compact subset of the open set $\mathcal{O} \sub \R^n$
2.  $F: \mathcal{O} \rightarrow \R^n$ be $C^1$ 
3. $Y_0 \in \mathcal {C}$ 

Suppose:

1. Every solution curve of the form $Y:[0, \beta] \rightarrow \mathcal{O}$ with $Y(0) = Y_0$ lies entirely in $\mathcal{C}$ 

Then:

$\exists$ a solution $Y:[0, \infin) \rightarrow \mathcal{O}$ satisfying $Y(0) = Y_0$ and $Y(t) \in \mathcal{C}$ for all $ t \geq 0$ so this solution is defined for all (forward) time

### Theorem

Let 

1. $F: \mathcal{O} \rightarrow \R^n$ be $C^1$ 
2. $Y(t)$ be a solution of $X' = F(X)$ that is defined on the closed interval $[t_0, t_1]$, with $Y(t_0) = Y_0$ 

Then:

1. There is a neighborhood $U \sub \R^n$ of $Y_0$ and a constant $K$ such that if $Z_0 \in U$ , then there is a unique solution $Z(t)$ also defined on $[t_0, t_1]$ with $Z(t_0) = Z_0$ 
2. $Z$ satisfies $|Y(t) - Z(t)| \leq K|Y_0 - Z_0|\exp(K(t-t_0))$ 

Note: We dropped the requirement that both solutions were defined on the same interval

#### Lemma. If $F: \mathcal{O} \rightarrow \R^n$ is locally Lipschitz and $\mathcal{C} \sub \mathcal{O}$ is a compact set, then $F|\mathcal{C}$ is Lipschitz

The restriction of a locally Lipschitz function to a compact set in its (open set) domain is Lipchitz

## 17.5 Nonautonomous Systems

Let

1.  $\mathcal{O} \sub \R \times \R^n$ be an open set
2. $F: \mathcal{O} \rightarrow \R^n$ be a function that is $C^1$ in $X$ but perhaps only continuous in $t$
3. $(t_0, X_0) \in \mathcal{O}$ 

Consider the nonautonomous differential equation

$X'(t) = F(t, X), \; \; \; X(t_0) = X_0$ 

A solution of this system is a differentiable curve $X(t)$ in $\R^n$ defined for $t$ in some interval $J$ having the following properties:

1. $t_0 \in J$ and $X(t_0) = X_0$ 
2. $(t, X(t)) \in \mathcal{O}$ and $X'(t) = F(t, X(t))$ for all $t \in J$ 

### Fundamental Local Theorem for nonautonomous equations

Let $\mathcal{O} \sub \R \times \R^n$ be open and $F: \mathcal{O} \rightarrow \R^n$ a function that is $C^1$ in $X$ and continuous in $t$ 

If $(t_0, X_0) \in \mathcal{O}$, 

there is an open interval $J$ containing $t$ and a unique solution of $X' = F(t,X)$ defined on $J$ and satisfying $X(t_0) = X_0$ 

#### Corollary

Let $A(t)$ be a continuous family of $n\times n$ matrices. Let $(t_0, X_0)$ $\in J\times \R^n$ 

Then:

$X' = A(t)X, X(t_0) = X_0$ 

has a unique solution on all of $J$ 

proof: Exercise 14 

### A function $F(t,X)$ Lipschitz in $X$ 

if there is a constant $K \geq 0$ s.t.

$|F(t, X_1) - F(t, X_2)| \leq K|X_1 - X_2|$ 

for all $(t,X_1), (t, X_2)$  in $\mathcal{O}$ 

### continuity of solutions as functions of the data $F(t,X)$ 

if $F: \mathcal{O} \rightarrow \R^n$ and $G: \mathcal{O} \rightarrow \R^n$ are both $C^1$ in $X$

and $|F-G|$ is uniformly small, 

we expect solutions to $X' = F(t,X)$and $Y' = G(t,Y)$ having the same initial values, to be close

### Theorem.

Let $\mathcal{O} \sub \R \times \R^n$ be an open set containing $(0, X_0)$ and suppose that $F, G: \mathcal{O} \rightarrow \R^n$ are $C^1$ in $X$ and continuous in $t$. Suppose also that for all $(t,X) \in \mathcal{O}$ 

$|F(t,X) - G(t,X)| < \epsilon$

Let $K$ be a Lipschitz constant in $X$ for $F(t,X)$   

If $X(t), Y(t)$ are solutions of the equations $X' = F(t,X)$ and $Y' = G(t,Y)$ respectively

on some interval $J$, and $X(0) = X_0 = Y(0)$ 

THEN:

$|X(t) - Y(t)| \leq \frac{\epsilon}{K}(\exp(K|t|)-1)$

for all $t \in J$ 

## 17.6 Differentiability of the Flow

Now back to autonomous diff. eqn. 

$X' = F(X)$ $F$ is assumed to be $C^1$ 

Our Aim:

show $\phi(t,X) = \phi_t(X)$ is a $C^1$ function of the two variables 

and to identify $\partial \phi/\partial X$ 

Suffices to prove differentiability in $X$, since we already know $\phi$ is cont. diff. in t by definition

So: Let $X(t)$ be a particular solution of the system defined for $t$ in a closed interval $J$ about 0

with $X(0) = X_0$ 

For each $t \in J$ :

Let $A(t) = DF_{X(t)}$ , the Jacobian matrix of $F$ at the point $X(t)$ 

Since $F$ is $C^1$, $A(t)$ is continuous

### Variational equation along the solution $X(t)$ 

We define the nonautonomous linear equation

$U' = A(t)U$ 

where  $A(t) = DF_{X(t)}$ , the Jacobian matrix of $F$ at the point $X(t)$ 

From previous section, we know that it has a solution on all of $J$ for every $U(0) = U_0$ 

Solutions satisfy the linearity principle

#### Significance

If $U_0$ is small, then the function 

$t \rightarrow $$X(t) + U(t)$

is a good approximation to the solution $X(t)$ of the original autonomous equation

where $X(0) = X_0 + U_0$ 

More precisely:

suppose $U(t, \xi)$  is the solution of the variation equation that satisfies $U(0, \xi) = \xi$ where $\xi \in \R^n$ 

If $\xi$ and $X_0 + \xi$ belong to $\mathcal{O}$, let $Y(t, \xi)$ be the solution of the autonomous equation $X' = F(X)$ that satisfies $Y(0) = X_0 + \xi$ 

### Proposition 

Let $J$ be the closed interval containing 0 on which $X(t)$ is defined

Then $\lim_{\xi \rightarrow 0} \frac{|Y(t, \xi)- X(t)-U(t, \xi)|}{|\xi|}$ 

converges to $0$ uniformly for $t \in J$ 

This means that for every $\epsilon > 0$  there exists $\delta > 0$ such that if $|\xi| \leq \delta$ 

then:$ |Y(t, \xi) - (X(t) + U(t, \xi)) |\leq \epsilon|\xi|$ 

for all $t \in J$ 

As $\xi \rightarrow 0$, the curve $t \rightarrow X(t)+ U(t, \xi)$ is a better and better approximation to $Y(t, \xi)$ 

### Theorem: Smoothness of Flows

The flow $\phi(t,X)$ of the autonomous system $X' = F(X)$ is a $C^1$ function

Proof:

uses Proposition directly above

uses continuity in initial conditions and data of solutions for the variational equation

### Space Derivative $D\phi_t(X)$ of the map $\phi_t$ at $X$ 

it is the same as $\partial \phi(t,X)/\partial X$ 

as opposed to the *time derivative* $\frac{\partial \phi(t,X)}{\partial t}$ 

$D\phi_t(X)$ is the solution of an IVP in the space of linear maps on $\R^n$:

For each $X_0 \in \mathcal{O}$ 

the space derivative of the flow satisfies the differential equation

$\frac{d}{dt}(D\phi_t(X_0)) = DF_{\phi_t(X_0)}D\phi_t(X_0)$ 

$D\phi_0(X_0) = I$ as the initial condition

**Important special case**

equilibrium solution $\bar{X}$ 

$\phi_t(\bar{X}) \equiv \bar{X}$  

$DF_{\bar{X}} = A$, we get

the solution to be

$D\phi_t(\bar{X}) = \exp tA$

so the flow is approximately linear in a neighborhood of an equilibrium point 

### Didn't read proof of proposition too closely



