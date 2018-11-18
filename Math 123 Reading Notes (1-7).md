# Math 123 Reading Notes

## Chapter 1

### 1.1 The Simplest Example 

#### Goes over $ \frac{dx}{dt} = ax$ 

* $x'(t) = ax(t)$ and $x(t) = ke^{at}$ is the only solution
  * proof involves having $u(t)$ be another solution and showing the derivative of $u(t)e^{-at}$ is 0, meaning $u(t)e^{-at} = k$ where k is a constant. 

#### General Solution 

* The collection of all solutions of a diff. eq. 

#### initial condition $x(t_0) = u_0$ 

* For simplicity: often take $t_0 = 0 $ and $k = u_0$ 
  * no loss in generality because if $u(t)$ has $u(0) = u_0$ then the function $v(t) = u(t-t_0)$ is a solution with $v(t_0) = u_0$ 
* for the example $\frac{dx}{xt} = ax$ this means $k = u_0e^{-at}$ 

#### initial value problem 

$x' = ax$,              $x(0) = u_0$ This is 

There is a special solution when $k = 0$ 

This is the solution $x(t) \equiv  0$  

#### equilibrium solution or equilibrium point 

a constant solution when $x(t) \equiv 0 $ and $k = 0$ 

[^1]: Page 2

#### The constant $a$ in the equation $x' = ax$ and how its sign affects the solution 

1. If $a > 0$, $lim_{t \rightarrow \infin}ke^{at}$ equals $\infin$ when $k > 0$, and equals $- \infin$ when $k < 0$ 
2. If $a = 0$, $ke^{at} = constant$ 
3. If $a < 0$, $lim_{t\rightarrow \infin}ke^{at} = 0$  

#### Qualitative Behavior of Solutions: graphs

when a > 0, the graphs tend away from the equilibrium point at 0

when a < 0, the graphs tend toward the equilibrium point at 0

##### equilibrium point as source or sink

source: a > 0? since tends away

sink: a < 0? since tends toward

##### phase line

can see $x(t)$ as a particle moving along the real line since x is a function of time.

at the equilibrium point, the particle remains at rest, while any other solution moves up or down the x-axis (see arrows below)

![1534985497884](C:\Users\Renee\AppData\Local\Temp\1534985497884.png)

#### stable equation $x' = ax$ 

happens if $a \neq 0$ 

More precisely, if a is replaced by another constant b hose sign is the same as a, then the qualitative behavior of the solutions does not change.

If a = 0, then the slightest change in a leads to a radical change in the behavior of the solutions.

##### bifurcation 

we have a _bifurcation_ at a = 0 in the one-parameter family of equations x' = ax

I think this happens when  stability works as above?

### 1.2 The Logistic Population Model

#### Assumptions about the population model:

1. If the population is small, growth rate is nearly directly proportional to the size of the population
2. If the population grows too large, the growth rate becomes negative

#### logistic population growth model

$x' = ax( 1 - \frac{x}{N})$ 

##### _a_ and _N_ are positive parameters:

1. a gives the rate of population growth when x is small
2. N represents a sort of "ideal" population or "carrying capacity"

If x is sufficiently small, makes $\frac{x}{N}$ negligible, so we just have $x' = ax$ 

if x > N, then $x' < 0$ 

Note: this is the simplest model...

**without loss of generality, assume N = 1**

This is so:

carrying capacity is 1 unit of population and x(t) represents a fraction of the ideal population present at time t.

We now have:

$x' = f_a(x) = ax(1-x)$ 

This is an example of a first-order, autonomous, nonlinear differential equation.

#### first order diff. eq.

only the first derivative of x appears.

#### autonomous

The right hand side of the equation depends on x alone, not on time t.

#### nonlinear

since $f_a(x)$ is a nonlinear function of x. (it's quadratic?)

#### Solution of the logistic differential equation

Method of separation and integration

partial fractions

in the end we get

$x(t) = \frac{Ke^{at}}{1 + Ke^{at}}$ where K is the arbitrary constant that arises from integration.

with an evaluation of x at t = 0, and solving for K, we get:

$K = \frac{x(0)}{1 - x(0)}$ and

the solution = $\frac{x(0)e^{at}}{1 - x(0) + x(0)e^{at}}$ 

So we take an initial population x(0)

when x(0) = 1, x(t) reduces to $x(t) \equiv 1$ (equilibrium solution)

$x(t) \equiv 0 $ is also an equilibrium solution

#### Qualitative Feeling for the behavior of solutions

##### slope field

![1534986978125](C:\Users\Renee\AppData\Local\Temp\1534986978125.png)

##### Can look at the graph of the function 

(tells us at what value x, what the growth rate will be) 

##### analytically

* Look at the derivative of x'(t)? e.g. $f'_a = a - 2ax$ 
* we have at x = 0, $f'_a(0) = a > 0$
* $f'_a(1) = -a < 0$ 
* so slopes of $f_a$ need to increase as we pass through x = 0 i.e., as we pass through x = 0, $f'_a$ is increasing, which means $f'_a(x) < f'_a(0) = 0, when x < 0$
  * b/c $f'_a$ = 0 at x = 0, so we have that the slopes of $f_a$ are negative below x = 0.

### 1.3 Constant Harvesting and Bifurcations 

#### Population logistic model thing

##### introduction of harvest rate h

let a = 1 and let the population be harvested at a constant rate h

we now have $x' = x(1-x) -h$ 

where $h \geq 0$ is a new parameter

#### Using graphs of the functions to "read off" qualitative behavior of solutions

1. Keeping a constant, and using h as the only parameter...
2. We look at 3 different cases
   1. 0 < h < 1/4
   2. h = 1/4
   3. h > 1/4
3. Check for roots of each $f_h$ 
   1. When h < 1/4, we have 2 roots
   2. When h = 1/4, we have 1 root
   3. When h > 1/4, we have no roots
4. As a consequence, the diff. eq. has two equilibrium points $x_l$ and $x_r$ 
5. You can check $f_h'(x_l)$ and $f_h'(x_r)$ to check if these are sinks or sources
   1. if positive, a source 
   2. if negative, a sink
6. As h passes through 1/4, we encounter another example of a bifurcation:
   1. $x_l$ and $x_r$ coalesce as h increases through 1/4 and then disappear.

bifurcation...

![1535146696143](C:\Users\Renee\AppData\Local\Temp\1535146696143.png)

1. At h < 1/4, unless x(0) $\geq x_l$, the population won't persist
2. at h = 1/4, we must have x(0) $\geq$ the equilibrium point
3. At any h > 1/4, there's no way for the population to persist: at any x(0), the population is declining

#### bifurcation diagram 

plot the parameter h horizontally, and over each h-value, we plot the corresponding phase line

the curve in the picture below represents the equilibrium points for each value of h

![1534988463695](C:\Users\Renee\AppData\Local\Temp\1534988463695.png)

#### Example: $x' = g_a(x)= x(x-a)$ 

1. look for equilibrium points: set x(x-a) = 0

   1. we get roots at x = 0 and x = a (our equilibrium points)

2. Look at $g'_a(0)$ and $g'_a(a$)

   1. $g'_a(0) = -a$
      1. a > 0: sink
      2. a < 0: source 
   2. $g'_a(a) = a$ 
      1.  a > 0: source
      2. a < 0: sink

3. Bifurcation at a = 0:

   1. only 1 equilibrium point when a = 0.

   2. Also equilibrium point at 0 changes from a source to a sink as a increases through 0. 

   3. x = a changes from sink to source as a increases through 0

      ![1535147430126](C:\Users\Renee\AppData\Local\Temp\1535147430126.png)

### 1.4 Periodic Harvesting and Periodic Solutions

#### Harvesting Doesn't always occur at a constant rate

Example Model:

$x' = f(t,x) = ax(1-x)-h(1+sin(2\pi t))$

and a, h > 0.

harvesting reaches max of $-2h$ at time $t = \frac{1}{4} + n$ where $n$ is an integer (representing year) 

Now this diff. eq. depends on time explicitly (not implicitly through x depending on t)

##### nonautonomous

depends on t as well?

We must do a qualitative approach since the diff. eq. is no longer separable.

the example model is periodic with t = 1, because sin is periodic with $\theta$ = $2\pi$ 

so $f(t+1, x) = f(t, x)$  //this simplifies finding the solution

[^2]: page 10

We know the solutions for $0 \leq t \leq 1$, we know them all.

so let $x_1(t)$ be a solution for defined for $0 \leq t \leq 1$ and satisfies $x_1(0) = x_0$

and suppose $x_2(t)$ satisfies $x_2(0) = x_1(1)$ 

we may define $x_1(t+1) = x_2(t)$ (so this gives us $x_1(t)$ defined for $ 1 \leq t \leq 2$)

So now this extended function is a solution too:

$x_1'(t+1) = x_2'(t) = f(t, x_2(t)) = f(t+1, x_1(t+1))$ 

	because we said $x_1(t+1) = x_2(t)$
	
	because we said $x_2(t)$ satisfies the initial value problem as well
	
	 because we said$f(t, x_2(t)) = f(t+1, x_2(t))$ 

Induction would probably proves we can extend the solution for all t, not just $0 \leq t \leq 1$ 

And if we knew all the solutions in the interval $0 \leq t \leq 1$, we can extrapolate to all time intervals and thereby know the behavior of solutions for all time.

	Are these 1-1? as in, the only way we could have $x_1(t)$ for all t is this method???

Suppose we know x(1) of the solution x(t) satisfying x(0) = $x_0$ 

Then to each such initial condition $x_0$, we can associate the value x(1) of the solution x(t) that satisfies x(0) = $x_0$ (I think we're still using the example model)

##### $p(x_0) = x(1)$ 

composing the function with itself...

$p(p(x_0)) = p(x(1)) = x(2)$ ???? This is assuming... p(x(t)) = x(t+1)????

What else do we know? do we know all values of x(t)?

How does the function p(x) work????

##### p is called a _Poincare map_ for this diff. eq. 

It allows us to move from continuous (diff. eq.) to discrete (iterated functions)

###### fixed-point: $p(x_0) = x_0$ , making $x_0$ a fixed point for function p 

From previous observations...

$x(n) = x_0$ for each integer n. 

moreover, for each t with $0 < t < 1$ 

$x(t) = x(t+1) = x(t+2) = . . . = x(t+n)$ // this was shown earlier with the $x_1, x_2$ thing.

and so we have x(t+n)

That is, the solution satisfying the initial condition $x(0) = x_0$ is a periodic function of t with period 1. 

This solutions are called

##### periodic solutions

of the diff eq. 

Are periodic solutions the only solutions for periodic diff. eqs?

### 1.5 Computing the Poincare Map

#### flow associated to the diff. eq. 

$\phi: \R \times \R \rightarrow \R$ (the corresponding solution?)

If we hold the variable $x_0$ fixed, then the function

$t \rightarrow \phi(t,x_0)$ is just an alternative expression for the solution of the diff. eq. ...

sometimes we write this function as $\phi_t(x_0)$

##### Example

with $x' = ax$, the flow is given by $\phi(t,x_0) = x_0e^{at}$ 

with the logistic equation (w/o harvesting)

$\phi(t,x_0) = \frac{x(0)e^{at}}{1 - x(0) +x(0)e^{at}}$

###### with the logistic diff. eq. with periodic harvesting

$\phi(t, x_0) = x_0 + \int_{0}^{t}f(x, \phi(s,x_0))ds$ 

Differentiate the equation wrt to $x_0$ and use the chain rule, $f(g(x))' = f'(g(x))\times g'(x)$ 

...

set a function $z(t)$ to equal the derivative of the equation wrt to $x_0$ 

Note that $z(0) = 1$ 

find $z'(t)$ 

We now know that $z(t)$ is a solution to a diff. eq. with $z(0) = 1$ 

Via separation of variables, we may compute the solution z(t)... so that we can express z(t) in terms of "what we know," which is some basic function stuff (exp and integrals) and the original diff. eq. This leads to us knowing the derivative of the Poincare map, p'($x_0$) as you can see below:

since $p(x_0) = \phi(1, x_0)$ = x(1) since $\phi$ is simply x(t) expressed in terms of t and $x_0$ 

Note: p'($x_0$) > 0, therefore p is an increasing function.

And differentiating further, we can conclude $p''(x_0) < 0$ 

So the graph of the Poincare map is concave down and can only cross the y = x graph at most twice.

so there are at most two values of x for which p(x) = x.

and from 1.4, these solutions for when p(x) = x gives periodic solutions of the original diff. eq. 

since p($x_0$) = x(1), which in this function with period 1, x(1) = x(0) = $x_0$ 

**The flow $\phi(t, x_0)$ is a periodic function in t with period 1 when $x_0$ is an initial value.**

The diff. eq. also depends on the harvesting parameter h. 

For small values of h, there will be two fixed points: Figure 1.11

Differentiating f w.r.t. h, we get that this derivative of f wrt h is < 0 except when $sin2\pi t = -1$, when the slope is 0...

The values of the Poincare map also decreases as h increases...

There is a unique value $h_*$ for which the poincare map has exactly one fixed point.

### 1.6 Exploration: A Two-Parameter Family

Consider the family of diff. eqs:

$x' = f_{a,b}(x) = ax - x^3 - b$ 

which depends on two parameters: a and b.

1. Fix a = 1, use the graph of $f_{1,b}$ to construct the bifurcation diagram for this family of diff. eq. depending on b
2. Repeat the previous step for a = 0, then for a = -1
3. What does the bifurcation diagram look like for the other values of a?
4. Now fix b and use the graph to construct the bifurcation diagram for this family, which depends on a this time
5. in the ab-plane, sketch the regions where the corresponding differential equation has different numbers of equilibrium points, including a sketch of the boundary between these regions
6. Describe, using phase lines and the graph of $f_{a,b}(x)$, the bifurcations that occur as the parameters pass through the boundary
7. Describe in detail the bifurcations that occur at a = b = 0 as a and/or b vary.
8. Consider the diff. eq. $x' = x - x^3 - bsin(2\pi t)$ where |b| is small. What can you say about the solutions of this eq? are there any periodic solutions?
9. Experimentally, what happens as |b| increases? Do you observe any bifurcations? Explain what you observe.

### Notes to Self

1. Looking at the graph of $f(t,x)$, if there's a steep slop, and we are changing a parameter like some $f(t,x) = g(t,x) + a$, as we change a, there's relatively little change in the equilibrium points for x, around where the slope is steep. otherwise, for a change in a, there's a big change in equilibrium points for x around where the slope is shallow.
2. To avoid the problem of trying to go from $\int a(t)dt$ to $\int_0^ta(s)ds$, 
   1. we can take $x = a(t)x'$ for example, 
   2. do the first part of separation of variables $x/x' = a(t)$ 
   3. Then integrate both sides from 0 to t. $\int_0^t x(s)/x'(s)ds = \int_0^ta(s)ds$ 
   4. The equilibrium solutions!!! 

### Exercises

5. More or less did correctly, He just mentioned that there is a sequence of $a_n$ from -1 with a limit of 0, s.t. when $a = a_k$, number of equilibrium point is $4k + 1$ and if $ a \in (a_k, a_{k+1})$ , number of equilibrium points is $4k +3$ 

6. Didn't do

7. didn't do

8. More or less did correctly, could have simplified the whole process by noticing if we set $z(t) = x(t) - y(t)$ we could've gotten $z'(t) = az(t)$ and remember that this means that $z(t) = Ce^{at}$ 

9. Separating Variables, but instead of integrating by dx and dt, we integrate x/x' from 0 to t over a variable $s$ and the same on the other side, $a(t)$ 

10. Didn't do

11. More or less did correctly, but forgot to mention the case when the solution is the equilibrium point, 0, so note to self, find all equilibrium solutions!!!

    1. the example he used for 11(c) was the solution: $\tan(\pi t/2)$ 

12. So

    1. Did this correctly
    2. Forgot to mention if $x_0 \neq 0$ there are no solutions.
    3. Did this wrong: 
       1. Need to mention not defined for t = 0
       2. Again, forgot the equilibrium solution!
       3. no solution for $C \neq 0$ and $x(0) = 0$ 

13. Did this one right more or less

14. DId this one more or less correctly, could've been more clever/cleaner about it.

    1. Could have started with $x(t+t) = x(0)\exp[\int_0^tp(s)ds]$ 
    2. eventually get to $x(t+T) = x(t)\exp[\int_t^{t+T}p(s)ds]$ 
    3. then I was right initially with using a substitution rule: r = s+T
    4. s = r - T
       1. MAYBE: We get $\int_{-T}^{0}p(r-T)dr = -\int_0^{-T}p(r-T)dr$ do $u = r$
       2. when $r-T = 0 \equiv r = T$ when $r - T = -T \equiv r = 0$ 
       3. $- \int_T^0 p(u-T)du = \int_0^Tp(u-T)du = \int_0^Tp(u)du$ last equality comes from $p$ being periodic
    5. $x(t+T) = x(t)\exp[\int_0^Tp(u)du]$ 
    6. so $x(t+T) = x(t) $$\iff \exp[\int_0^Tp(u)du] = 1 \equiv \int_0^Tp(u)du = 0$  

15. 

    1. Needed to use the fact that for ALL $t$ that $f(t,p) > 0$ and $f(t, q) < 1$
       1. this would mean for any solution that has $x(0)$ in $(p,q)$, since $f$ is continuous, if $x$ ever get in some neighborhood of $q$, it will be decrease, and thus never reach $q$, and if $x$ ever get in some neighborhood of $p$, it will increase and never reach $p$. 
    2. The way he proves $\phi$ and therefore $P$ is continuous is a bit awful, it requires you to go to 17.3 somehow... he just says that since solutions depend continuously on the intial condition, it follows that $\phi$ is continuous


## Chapter 2: Planar Linear Systems

#### Systems Of Differential Equations

A collection of *n* interrelated differential equations of the form

$x'_1 = f_1(t, x_1, x_2, . . ., x_n) \\ x_2' = f_2(t, x_1, x_2, . . ., x_n) \\ \vdots \\x_n' = f_n(t, x_1, x_2, . . ., x_n)$ 

Here the functions of $f_j$ are real-valued functions of the n+1 variables 

Unless otherwise specified, we will always assume the $f_j $ are $C^\infin$: meaning, the partial derivatives of all orders of the $f_j$ exist and are continuous. 

#### Notation 

$X = \begin{pmatrix}x_1\\ \vdots \\ x_n \end{pmatrix}$ , or $X = (x_1, . . ., x_n)$ 

System may be written as:

$X'  = F(t, X)$ 

where $F(t, X) = \begin{pmatrix} f_1(t, x_1, . . , x_n) \\ \vdots \\ f_n(t, x_1, . . ., x_n) \end{pmatrix}$ 

A solution of this system is a function of the form $X(t) = (x_1(t), . . ., x_n(t))$ 

so that $X'(t) = F(t, X(t))$ where $X'(t) = (x'_1(t), . . ., x_n'(t))$ 

#### Autonomous

none of the $f_j$ depends on t, so the system becomes $X' = F(X)$ 

#### Equilibrium Point

A vector $X_0$ for which $F(X_0) = 0$ 

An equilibrium point corresponds to a constant solution $X(t) \equiv X_0$ of the system as before.

Lower Case Letters: variables, real-valued functions

Capital Letters: Vectors, vector-valued functions 

### 2.1 Second-Order Differential Equations

#### Form: $x'' = f(t,x,x')$

#### Examples

##### Newton's equation $mx'' = f(x)$

##### Equation for an RLC circuit in electrical engineering: $LCx'' + RCx' +x = v(t)$

##### the forced harmonic oscillator $mx'' + bx' + kx = f(t)$ 

These equations are a special subclass of two-dim. systems of diff. eq.'s that are defined by simply introducing a second variable $y = x'$ 

E.g.: $x'' + ax' + bx = 0$ becomes, if we let $y= x'$ 

$x' = y \\ y' = -bx - ay$ 

### 2.2 Planar Systems

For the remainder of this chapter we will deal with autonomous systems in $\R^2$, which we will write in the form

		 $x' = f(x,y) \\ y' = g(x,y)$ 

#### Notation

$X' = F(X)$ where $X = (x,y)$ and $F(X) = F(x,y) = (f(x,y), g(x,y))$ 

$F$ is a vector-valued function, where it takes in a vector as inputs, which are then inputs to each of its function entries... 

#### vector field

The right-hand side of this equation defines a *vector field* on $\R^2$ 

So $F(x,y)$ is a vector whose $x-$ and $y-$ components are $f(x,y)$ and $g(x,y)$ resp. 

This vector has the initial point: $(x,y)$ 

#### Direction field

Because many of these vectors overlap, the pattern is hard to visualize, so instead we draw a direction field, which consists of scaled versions of the vectors

A solution of this system should now be thought of as a parameterized curve in the plane of the form $(x(t), y(t))$ such that for each $t$, the tangent vector at the point $(x(t), y(t))$ is $F(x(t, y(t)))$ 

##### Example: $\begin{pmatrix}x(t) \\ y(t) \end{pmatrix} = \begin{pmatrix} a\, sin\, t \\ a\, cos\, t \end{pmatrix}$ 

This curve is a solution to $x' = y \\ y' = -x$ 

since $x'(t) = a\, cos\, t = y(t)$ and $y'(t)  = -a\, sin\, t = -x(t)$ 

These curves define circles of radius $|a|$  that are traversed in the clockwise direction as t increases.

This Example is equivalent to the second-order differential equation $x'' = -x$ by simply introducing the second variable $y = x'$ 

#### Linear second-order diff. eq. 

$a(t)x'' + b(t)x' +c(t)x = f(t)$ 

##### constant coefficient

a special case of a linear second-order diff. eq. 

$ax'' + bx' + cx = f(t)$ which can be written as

$x' = y\\\ y' = \large-\frac{c}{a}x - \frac{b}{a}y + \frac{f(t)}{a}$ 

##### homogenous equation

Basically, when $f(t) \equiv 0$  

###### Example of linear, second-order, constant coefficient diff. eq.: harmonic oscillator 

$x$ denotes the displacement of the mass from its natural resting placed with $x>0$ if spring is stretched and $x<0$ if it is compressed

$x'(t)$ denotes the velocity of the moving mass, and $x''(t)$ is acceleration 

The spring exerts a restorative force prop. to $x(t)$ 

There is a frictional force proportional to $x'(t)$ in the direction opposite to that of the motion 

Three parameters: $m$, the mass of the oscillator, $b \geq 0$ the damping constant, and $k >0$ the spring constant

The force acting on the oscillator (frictional force, restorative force) is = $m \times acceleration$ 

$mx'' + bx' + kx = 0$ 

As a system this equation becomes:

$x' = y\\ y' = -\frac{k}{m}x - \frac{b}{m}y$ 

More generally, the motion of the mass-spring system can be subjected to an external force (such as moving the vertical wall back and forth periodically)

Such an external force usually depends only on time, not position... so 

the general forced harmonic oscillator system:

$mx'' + bx' + kx = f(t)$  where $f(t)$ represents the external force.

The introduction of $f(t)$ makes this equation nonautonomous

### 2.3 Preliminaries from Algebra 

Systems come in the form of

$ax + by = \alpha \\ cx + dy = \beta$ 

Matrix form:

$\begin{pmatrix} a &b\\c&d\end{pmatrix} \begin{pmatrix} x\\y\end{pmatrix} = \begin{pmatrix}\alpha \\ \beta \end{pmatrix}$ 

#### Determinants

If determinant is 0, we may or may not have solutions (not invertible)

	if there is a solution: infinitely many
	
	the kernel is not = 0, I believe. 

#### Linear Independence of vectors

To me, it means that a vector is lin. independent to a set of vectors, if those vectors cannot be lin. combined to make the first vector. 

#### Proposition

V and W are lin. independent iff the matrix made up of these vectors has a determinant not equal to 0. 

#### Basis

A basis for any space V is a set of vectors for any vector *v* in V, there exists a unique linear combination of the basis vectors that make up *v* 

### 2.4 Planar Linear Systems

linear systems, autonomous case, the form these systems assume:

$x' = ax + by \\ y' = cx + dy$ 

were $a, b, c,$ and $d$ are constants

we may set $A = \begin{pmatrix} a &b \\ c &d \end{pmatrix}$ 

This system may be written as

$X' = AX$ 

#### $(0,0)$ is always an equilibrium point for a linear system.

#### Finding equilibria

Solve:

$ax + by = 0 \\ cx + dy = 0$ 

The system as a nonzero solution $\iff$ det A = 0. 

##### If det A = 0, then there is a straight line through the origin on which each point is an equilibrium. 

#### Proposition: The planar linear system $X' = AX$ has

##### 1. A unique equilibrium point (0,0) if det A $\neq$ 0

##### 2. A straight line of equilibrium points if det A = 0 (and A is not the 0 matrix)

### 2.5 Eigenvalues and Eigenvectors

Suppose $V_0$ is a nonzero vector for which we have $AV_0 = \lambda V_0$, where $\lambda \in \R$ 

Then $X(t) = e^{\lambda t}V_0$ is a solution of the system. 

To see this:

$X'(t) = \lambda e^{\lambda t}V_0$ 

$X'(t) = e^{\lambda t}\lambda V_0$

$X'(t) = e^{\lambda t}(AV_0)$ 

$X'(t) = A(e^{\lambda t}V_0)$ 

$X'(t) = AX(t)$  

#### Eigenvector

Definition: a nonzero vector $V_0$ is called an eigenvector of $A$ if $AV_0 = \lambda V_0$  for some $\lambda$, which is called an *eigenvalue* of A

#### Theorem

Suppose that $V_0$ is an eigenvector for the matrix of A with associated eigenvalue $\lambda$. Then the function $X(t) = e^{\lambda t}V_0$ is a solution of the system $X' = AX$ 

Also if $V_0$ is an eigenvector for A with eigenvalue $\lambda$, then any scalar multiple of $V_0$ is also an eigenvector for $A$ with eigenvalue $\lambda$. 

#### How to Find Eigenvalues

Solve:

$(A-\lambda I)V = 0$ 

This system with matrix $(A-\lambda I)$ has nonzero solutions iff det $A - \lambda I$= 0. 

This equation will be a polynomial equation in $\lambda$, known as 

##### (as a function of $\lambda$) the characteristic polynomial

##### Otherwise, it is called the characteristic equation

##### Find roots of char. polynomial to get eigenvalues

##### Using each of the eigenvalues, we find the associated eigenvector

### 2.6 Solving Linear Systems

#### Straight line Solution

Each solution of the form

$X_i(t) = e^{\lambda_i t}V_i$ where $V_i$ is the eigenvector associated to $\lambda_i$ 

is a straight-line solution.

We have $X_i(0) = V_i$, which is a nonzero point in the plane.

For each t, $e^{\lambda_i t}V_i$ is a scalar multiple of $V_i$ and so lies on the straight ray emanating from the origin and passing through $V_i$ 

If $\lambda_i > 0$ $\rightarrow$ 

$\lim_{t \rightarrow \infin}|X_i(t)| = \infin$

$\lim_{t \rightarrow 0}X_i(t) = (0,0)​$

The exact opposite occurs if $\lambda_i < 0 $ 

If $\lambda_i = 0$ the solution $X_i(t)$ is the constant solution $X_i(t) = V_i$ for all $t$ 

#### How to find all solutions of the system given we know the solutions from eigenvalues/vectors?

Let $\lambda_1$ and $\lambda_2$ be eigenvalues with eigenvectors $V_1$ and $V_2$ 

These vectors are linearly independent

$V_1, V_2$ make up a basis for $\R^2$ 

so for any point $Z_0 \in \R^2$ $\exist \, \alpha, \beta \in \R $ s.t.

$\alpha V_1 + \beta V_2 = Z_0$ 

Consider the function

$Z(t) = \alpha X_1(t) + \beta X_2(t)$ where the $X_i(t)$ are the straight-line solutions previously. 

Claim $Z(t)$ is a solution of $X' = AX$

To see this, compute $Z'(t)$ and see that it is indeed equal to $AZ(t)$

so $Z(t)$ is a solution satisfying $Z(0) = Z_0$ (just plug in 0 to see this).

Suppose $Y(t)$ is a another solution with $Y(0) = Z_0$ 

Then:

$Y(t) = \zeta(t)V_1 + \mu(t)V_2$ //Since $V_1, V_2$ are linearly independent, any point (x,y) can be written in terms of $c_1V_1 + c_2V_2$ 

with $\zeta(0) = \alpha$ and $\mu(0) = \beta$  // since $Y(0) = Z_0$, which is uniquely expressed as $\alpha V_1 + \beta V_2$ 

So:

$AY(t) = Y'(t) = \zeta'(t)V_1 +\mu'(t)V_2$ 

but

$AY(t) = \zeta(t)AV_1 + \mu(t)AV_2 \\ = \lambda_1\zeta(t)V_1 + \lambda_2\mu(t)V_2$ 

So using linear independence of $V_2, V_2$ and equating the two $AY(t)$ expressions:

$\zeta'(t) = \lambda_1\zeta(t) \\ \mu'(t = \lambda_2\mu(t)$

This are each in the form of a diff. eq. we have seen before, the simplest case, which can be solved by

$\zeta(t) = \zeta(0)e^{\lambda_1 t} = \alpha e^{\lambda_1 t}\\ \mu(t) = \mu(0)e^{\lambda_2 t} = \beta e^{\lambda_2 t}$

which means $Y(t) = Z(t)$ 

So we have found the unique solution to the IVP:

$X' = AX \quad \quad X(0) = Z_0$ 

#### General solution

The collection of all such solutions is called the *general solution* of $X' = AX$, 

that is, the general solution is the collection of solutions of $X' = AX$ that features a unique solution of the IVP $X(0) = Z_0$ for every $Z_0 \in \R^2$ 

#### Theorem

Suppose A has a pair of real eigenvalues $\lambda_1 \neq \lambda_2$ and associated eigenvectors $V_1$ and $V_2$. Then the general solution of the linear system $X' = AX$ is given by 

$X(t) = \alpha e^{\lambda_1 t}V_1 + \beta e^{\lambda_2 t}V_2$ 

### 2.7 The Linearity Principle

#### linearity principle

If $Y_1(t)$ and $Y_2(t)$ are both solutions to $X' = AX$, then a linear combination of the two is also a solution.

If the initial conditions $Y_1(0), Y_2(0)$ are linearly independent vectors, then these vectors form a basis of $\R^2$ 

#### Theorem 

Let $X' = AX$ be a planar system. Suppose that $Y_1(t)$ and $Y_2(t)$ are solutions of this system, and that the vectors $Y_1(0)$ and $Y_2(0)$ are linearly independent. Then

$X(t) = \alpha Y_1(t) + \beta Y_2(t)$ 

is the unique solution of this system that satisfies $X(0) = \alpha Y_1(0) + \beta Y_2(0)$ 

### Exercises

#### Ex 2. Find the general solution of each of the following linear systems

##### (a) $X' = \begin{pmatrix} 1 & 2 \\ 0 & 3 \end{pmatrix}X$

Finding the eigenvalues and eigenvectors:

$(1-\lambda)(3-\lambda) - 2\times0 = (1-\lambda)(3-\lambda)$, meaning roots at $\lambda = 1, 3$ 

When $\lambda = 1$, eigenvector: $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$, One Solution: $ e^{t}\begin{pmatrix}1 \\ 0 \end{pmatrix}$

When $\lambda = 3$, eigenvector: $\begin{pmatrix} 1 \\ 1\end{pmatrix}$ , One solution:  $e^{3t}\begin{pmatrix}1 \\ 1\end{pmatrix}$ 

General solution: $X(t) = \alpha e^{t}\begin{pmatrix}1 \\ 0 \end{pmatrix}+ \beta e^{3t}\begin{pmatrix}1 \\ 1\end{pmatrix}$ 

##### (b) $X' = \begin{pmatrix} 1 & 2 \\ 3 & 6 \end{pmatrix}X$

Finding eigenvalues: $(1- \lambda)(6 - \lambda) - 6 = \lambda^2 -7\lambda$, roots at $\lambda = 0, 7$ 

When $\lambda = 0$, eigenvector: $\begin{pmatrix} -2 \\ 1 \end{pmatrix}$ 

When $\lambda = 7$, eigenvector: $\begin{pmatrix} 1 \\ 3 \end{pmatrix}$ 

General solution: $X(t) = \alpha \begin{pmatrix} -2 \\ 1 \end{pmatrix} + \beta e^{7t} \begin{pmatrix} 1 \\ 3 \end{pmatrix}$ 

##### (c) $X' = \begin{pmatrix} 1 & 2 \\ 1 & 0 \end{pmatrix}X$

Finding eigenvalues: $(1-\lambda)(-\lambda) - 2 = \lambda^2 -\lambda - 2 = (\lambda -2)(\lambda+1)$, roots at $\lambda = -1,2$ 

When $\lambda = -1$, eigenvector: $\begin{pmatrix} 1 \\ -1 \end{pmatrix}$ 

When $\lambda = 2$, eigenvector: $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$ 

General solution: $X(t) = \alpha e^{-t} \begin{pmatrix} 1 \\ -1 \end{pmatrix} + \beta e^{2t} \begin{pmatrix} 2 \\ 1 \end{pmatrix}$  

##### (d) $X' = \begin{pmatrix} 1 & 2 \\ 3 & -3 \end{pmatrix}X$

Finding eigenvalues: $(1 - \lambda)(-3 - \lambda) - 6 = \lambda^2 +2\lambda - 9$, roots at $\lambda = -1\pm\sqrt{10}$, (found using quadratic equation)

When $\lambda = -1 + \sqrt{10}$ , eigenvector: $\begin{pmatrix} 1 \\ -1 + \sqrt{10}/2 \end{pmatrix}$

When $\lambda = -1 - \sqrt{10}$, eigenvector: $\begin{pmatrix} 1 \\ -1 -1 \sqrt{10}/2 \end{pmatrix}$ 

General solution: $X(t) = \alpha e^{(-1 + \sqrt{10})t}\begin{pmatrix} 1 \\ -1 + \sqrt{10}/2 \end{pmatrix}+ \beta e^{(-1 - \sqrt{10})t}\begin{pmatrix} 1 \\ -1 -1 \sqrt{10}/2 \end{pmatrix}$ 

#### Ex 3. In Figure 2.2 you see four direction fields. Match each of these direction fields with one of the systems in the previous exercise.

![1535689770566](C:\Users\Renee\AppData\Local\Temp\1535689770566.png)

For (a) , when we look at $(1, 0)$, we get back the tangent vector $(1, 0)$, and when we look at $(1, 1)$, we get $(3,3)$ as the tangent vector

For (b), on the line $y = (-1/2)x$ , we should have no vectors

For (c) at $(-1, 1)$, we get the tangent vector $(1, -1)$, and at $(1, -1)$, the tangent vector $-1, 1$ 

and at $(2,1)$, the tangent vector $(4,2)$, also along the $y-$axis, when $y>0$, we should get vectors that go towards the right horizontally, and when $y<0$, vectors that go to the left horizontally.

For (d) along the line $y = x$, we should have vectors of the form $(3x, 0)$ 

So:

$(a) \rightarrow 4$ 

$(b) \rightarrow 2$ 

$(c) \rightarrow 1$ 

$(d) \rightarrow 3$ 

#### Ex 4. Find the general solution of the system $X' = \begin{pmatrix} a & b \\ c & a \end{pmatrix}$ , where $bc > 0$.

Finding eigenvalues: $(\lambda -a)^2 - bc = \lambda^2 -2a +(a^2-bc)$

Using quadratic equation: we get roots at $a \pm \sqrt{bc}$, which is real, since $bc >0$ 

For $\lambda = a + \sqrt{bc}$, the eigenvector is $\begin{pmatrix} \sqrt{|b|} \\ \sqrt{|c|} \end{pmatrix}$

For $\lambda = a - \sqrt{bc}$, the eigenvector is $\begin{pmatrix} \sqrt{|b|} \\ -\sqrt{|c|} \end{pmatrix}$ 

General solution: $X(t) = \alpha e^{(a + \sqrt{bc})t}\begin{pmatrix} \sqrt{|b|} \\ \sqrt{|c|} \end{pmatrix} + \beta e^{(a-\sqrt{bc})t}\begin{pmatrix} \sqrt{|b|} \\ -\sqrt{|c|} \end{pmatrix} $   

#### Ex 6. For the harmonic oscillator system $x'' + bx' + kx = 0$, find all values of $b$ and $k$ for which this system has real, distinct eigenvalues. Find the general solution of this system in these cases. Find the solution of the system that satisfies the initial condition $(0, 1)$. Describe the motion of the mass in this particular case.

$x' = y$

$y' = -kx - by$ 

We now have: $X' = \begin{pmatrix} 0 & 1 \\ -k & -b \end{pmatrix}X$ 

Finding the eigenvalues: $(-\lambda)(-b-\lambda) + k = \lambda^2+b\lambda +k$

We get: $\frac{-b \pm \sqrt{b^2-4k}}{2}$ 

setting $\lambda_1 = (-b+\sqrt{b^2-4k})/2, \lambda_2 = (-b - \sqrt{b^2-4k})/2$

General solution: $X(t) = \alpha e^{\lambda_1t} \begin{pmatrix} 1 \\ \lambda_1 \end{pmatrix} +\beta e^{\lambda_2t} \begin{pmatrix}1 \\ \lambda_2 \end{pmatrix}$ 

To find the solution that satisfies the initial condition $(0 ,1)$, we must solve

$\begin{pmatrix} 1 & 1 \\ \lambda_1 & \lambda_2 \end{pmatrix} \begin{pmatrix} \alpha \\ \beta \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ 

When we row reduce the augmented matrix:

$\begin{pmatrix} 1 & 0 & \lambda_2/(\lambda_2-\lambda_1) \\ 0 &1 & -\lambda_1/(\lambda_2-\lambda_1) \end{pmatrix}$

We end up with $\alpha = \lambda_2/(\lambda_2 - \lambda_1)$ , $\beta = -\lambda_1/(\lambda_2-\lambda_1)$ 

$X(t) = \frac{\lambda_2}{\lambda_2-\lambda_1} e^{\lambda_1t} \begin{pmatrix} 1 \\ \lambda_1 \end{pmatrix} -\frac{\lambda_1}{\lambda_2-\lambda_1} e^{\lambda_2t} \begin{pmatrix}1 \\ \lambda_2 \end{pmatrix}$

1. If $k > 0$, we need $b^2 - 4k > 0$ to have real, distinct values, so $b >2\sqrt{k}$ or $b <- 2\sqrt{k}$   

   1. If $b > 0$ 

      $\lambda_2 < 0$, since $(-b - \sqrt{b^2-4k})/2 < 0$  

      $\lambda_1 < 0$, since $b^2 -4k < b^2$, so $\sqrt{b^2 - 4k} < b$ 

      for all $t > 0$, and because $\lambda_2 < \lambda_1$ 

      $e^{\lambda_1t}> e^{\lambda_2}t > 0$

      $\lambda_2/(\lambda_2-\lambda_1) > \lambda_1/(\lambda_2-\lambda_1) > 0$

      so:

      $x(t) =  \frac{\lambda_2}{\lambda_2-\lambda_1} e^{\lambda_1t} -\frac{\lambda_1}{\lambda_2-\lambda_1} e^{\lambda_2t} >0$ for all $t$, and as $t$ increases, both $e^{\lambda_1t}$ and $e^{\lambda_2t}$ go towards 0, so the mass moves towards the origin.

   2. If $b<0$

      $\lambda_1 > 0$, $\lambda_2> 0$ 

      and $\lambda_2 < \lambda_1$, so $\lambda_2 - \lambda_1<0$ 

      And we have $x(t) =  \frac{\lambda_2}{\lambda_2-\lambda_1} e^{\lambda_1t} -\frac{\lambda_1}{\lambda_2-\lambda_1} e^{\lambda_2t}$ 

      and when $e^{(\lambda_1-\lambda_2)t} >\frac{\lambda_1}{\lambda_2}$, which will happen eventually, since $e^{(\lambda_1-\lambda_2)t} \rightarrow\infin$ as $t \rightarrow \infin$ 

      we have that $x(t) < 0$, and in fact, $x(t) \rightarrow -\infin$ as $t \rightarrow \infin$ 

      which means the mass moves back to origin and the spring keeps compressing. 

2. If $k = 0$, we have eigenvalues: $\lambda_1= 0, \lambda_2 = -b$ with eigenvectors: $(1, 0)$ and $(1, -b)$ respectively. For distinct, real, we must have $b \in \R\setminus$ $0$. 

   The solution that satisfies $X(0) = (1, 0)$ is $\alpha = 1, \beta = 0$ , since which means that $X(t) = (1, 0)$ for all $t$, so the mass isn't moving: this makes sense as the velocity is 0, and the spring constant is 0, so there's no restorative force to bring the mass back to its natural resting place, $x = 0$ 

3. If $k < 0$, $b$ must be real, 

   1. regardless of the sign of $b$, since $b^2-4k > b^2$,  $\sqrt{b^2-4k} > |b|$ 

      $\lambda_1 > 0$, $\lambda_2 < 0$ 

      $\lambda_2/(\lambda_2-\lambda_1) > 0$, and $\lambda_1/(\lambda_2-\lambda_1) < 0$

      so as $t \rightarrow +\infin$ : $\frac{\lambda_2}{(\lambda_2-\lambda_1)}e^{\lambda_1t} \rightarrow +\infin$ and $\frac{\lambda_1}{(\lambda_2-\lambda_1)}e^{\lambda t} \rightarrow 0$   

      so $x(t) \rightarrow +\infin$ , meaning the mass keeps moving away from origin



#### Ex 7. Consider the $2 \times 2$ matrix $A = \begin{pmatrix} a & 1 \\ 0 &1\end{pmatrix}$ Find the value of $a_0$ of the parameter of $a$ for which $A$ has repeated real eigenvalues. What happens to the eigenvectors of this matrix as $a$ approaches $a_0$? 

the characteristic polynomial: $(\lambda -a)(\lambda -1)$ 

So when $a = 1$, we have repeated eigenvalues, and the corresponding eigenvector will be:

$(1, 0)$ 

When $a \neq 1$, we have two eigenvectors, so as $a \rightarrow 1$, we go from 2 eigenvectors:

$(1, 0)$ corresponding to the eigenvalue $a$, and

$(1, 1-a)$ corresponding to the eigenvalue 1.  

and we notice as $a \rightarrow 1$ the eigenvector corresponding to 1 approaches the eigenvector corresponding to $a$ 

#### Ex 9. Give an example of a linear system for which $(e^{-t}, \alpha)$ is a solution for every constant $\alpha$. Sketch the direction field for this system. What is the general solution of this system?

$Y(t) = e^{-t} \begin{pmatrix} 1 \\ 0 \end{pmatrix}+\alpha\begin{pmatrix} 0 \\ 1 \end{pmatrix}$ and $Y'(t) = \begin{pmatrix} -e^{-t} \\ 0\end{pmatrix}$ 

$\begin{pmatrix} -1 & 0 \\ 0& 0\end{pmatrix} \begin{pmatrix} e^{-t} \\ \alpha \end{pmatrix} = \begin{pmatrix} -e^{-t} \\ 0 \end{pmatrix}$, for all $\alpha, t$ 

The general solution is $X(t) = \alpha \begin{pmatrix} 0 \\ 1\end{pmatrix} + \beta e^{-t}\begin{pmatrix} 1 \\ 0 \end{pmatrix}$ 

$x' = -x \\ y' = 0$  

![1535977136866](C:\Users\Renee\AppData\Local\Temp\1535977136866.png)

#### Ex 11 Prove that two vectors $V = (v_1, v_2)$ and $W = (w_1, w_2)$ are linearly independent $\iff$ $\det\begin{pmatrix} v_1 & w_1 \\ v_2 & w_2 \end{pmatrix} \neq 0$

We can prove this by proving: $V$ and $W$ are linearly dependent $\iff \det \begin{pmatrix} v_1 & w_1 \\ v_2 & w_2 \end{pmatrix} = 0$ 

Let $V = \lambda W$, which means $V$ and $W$ are linearly dependent $\iff$$v_1 = \lambda w_1$ and $v_2 = \lambda w_2$ $\iff$ $\lambda = v_1/w_1 = v_2/w_2$ $\iff$ $v_1w_2 = v_2w_1$ $\iff v_1w_2 - v_2w_1 = 0 \iff \det\begin{pmatrix} v_1 & w_1 \\ v_2 & w_2 \end{pmatrix} = 0$ 

#### Ex 12 Prove that if $\lambda, \mu$ are real eigenvalues of a $2 \times 2$ matrix, then any  nonzero column of the matrix $A - \lambda I$ is an eigenvector for $\mu$ 

let $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ , since $\lambda, \mu$ are eigenvalues, 

The characteristic polynomial: $x^2 - (a+d)x - (ad -bc)$ 

We let $\lambda = \frac{(a+d)+\sqrt{(a+d)^2-4(ad-bc)}}{2}$

and $\mu =$ $\frac{(a+d)-\sqrt{(a+d)^2-4(ad-bc)}}{2}$  without loss of generality.

Let's take the column vector from $A - \lambda I$, $\begin{pmatrix} a- \lambda \\ c \end{pmatrix}$ and multiply $A - \mu I$ by this vector.

We get $\begin{pmatrix} a-\lambda& b \\ c & d-\lambda \end{pmatrix} \begin{pmatrix} a - \mu \\ c \end{pmatrix}$  = $\begin{pmatrix} (a-\lambda)(a-\mu) +bc \\ c(a+d -(\mu + \lambda)) \end{pmatrix}$ 

If we prove this is equal to the 0 vector, then $\begin{pmatrix} a- \lambda \\ c \end{pmatrix}$is an eigenvector, provided $\mu \neq a$ and $c \neq 0$ 

$(a-\lambda)(a-\mu)=$ $a^2 -a(\lambda +\mu) - \lambda\mu$ 

$(\lambda + \mu) = $$(a+d)$, so the second entry of the vector is $= c(a+d - (a+d)) = 0$ 

and $\lambda\mu=$$((a+d)^2 - (a+d)^2 + 4(ad-bc))/4 = ad-bc$ 

So $(a-\lambda)(a-\mu) = a^2 -a^2 -ad +ad -bc = -bc$, 

so: $\begin{pmatrix} (a-\lambda)(a-\mu) +bc \\ c(a-\mu + d - \lambda) \end{pmatrix}$ = $\begin{pmatrix} 0 \\ 0 \end{pmatrix}$ 

So now we prove the other column vector is an eigenvector in the same way:

$\begin{pmatrix} a-\lambda& b \\ c & d-\lambda \end{pmatrix} \begin{pmatrix} b \\ d-\mu \end{pmatrix}$ = $\begin{pmatrix} b(a+d - (\lambda + \mu)) \\ bc + (d-\lambda)(d-\mu) \end{pmatrix}$ 

From earlier, we know $b(a+d - \lambda - \mu) = 0$ 

and replacing $(d-\lambda)(d-\mu) = d^2 -ad - d^2 + ad - bc = -bc$, 

so: $\begin{pmatrix} (a-\lambda)(a-\mu) +bc \\ c(a-\mu + d - \lambda) \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$

As long as $\mu \neq d$ and $b\neq 0$, the vector $\begin{pmatrix} b \\ d - \mu \end{pmatrix}$ is an eigenvector

#### Ex 14 Prove that the eigenvectors of a $2 \times 2$ matrix corresponding to distinct real eigenvalues are always linearly independent. 

Let $A$ be a $2 \times 2$ matrix with $2$ eigenvalues: $\lambda, \mu$ where $\lambda \neq \mu$ let $v_\lambda$ and $v_\mu$ be the (nonzero) eigenvectors corresponding to $\lambda$ and $\mu$ respectively. 

Suppose $v_\lambda$ and $v_\mu$ are linearly dependent $\implies v_\lambda = cv_\mu$ for some constant $c \in \R\setminus {0}$, since both vectors must be nonzero. 

$Av_\lambda = \lambda v_\lambda = \lambda(cv_\mu)$

$A(cv_\mu) = \mu(cv_\mu)$

equating the two: $\lambda(cv_\mu) = \mu(cv_\mu)$ 

$\lambda(cv_\mu) - \mu(cv_\mu) = 0 \equiv (\lambda - \mu)(cv_\mu) = 0$

which means, since $cv_\mu$ is nonzero, $\lambda - \mu = 0 \equiv \lambda = \mu$, a contradiction. So these two eigenvectors must be linearly independent. 

## Chapter 3 Phase Portraits for Planar Systems

### 3.1 Real Distinct Eigenvalues 

#### 3 cases for two distinct real eigenvalues

1. $\lambda_1 < 0 < \lambda_2$
2. $ \lambda_1<\lambda_2 < 0$ 

3. $0 < \lambda_1 <\lambda_2$ 

#### Examples

1. $\lambda_1 < 0 < \lambda_2$ , Saddle

   $\lambda_1 < 0 < \lambda_2$ , Saddle

   1. $A = \begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ 

      $X(t) = \alpha e^{\lambda_1t} \begin{pmatrix} 1 \\ 0 \end{pmatrix} + \beta e^{\lambda_2t} \begin{pmatrix} 0 \\ 1 \end{pmatrix}$ 

      ##### Stable and Unstable lines

      Since $\lambda_1 < 0$, solutions of the form $\alpha e^{\lambda_1 t} (1,0)$ lie on the $x$-axis and tend to $(0,0)$ as $t \rightarrow \infin$ , this is the *stable line*  

      Since $\lambda_2 > 0$, the solutions of the form $\beta e^{\lambda_2t}(0,1)$ lie on the $y$-axis tend away from $(0,0)$, this is the *unstable line*

      ##### Phase Portrait in the Phase Plane

      a picture of a collection of representative solution curves of the system in $\R^2$, which we call the *phase plane*  

      ![1536027809350](C:\Users\Renee\AppData\Local\Temp\1536027809350.png)

      In general, "straight line solutions" are when $\alpha \neq 0, \beta = 0$ or vice versa. 

![1536028038546](C:\Users\Renee\AppData\Local\Temp\1536028038546.png)

		All solutions approach the unstable line as $t\rightarrow \infin$ and 
	
		tend toward the stable line as $t \rightarrow -\infin$ 
	
		We always find a stable and unstable line. 

2. $\lambda_1 <\lambda_2 < 0$, Sink

   $A = \begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ 

   Find two straight line solutions:

   $X_1(t) = \alpha e^{\lambda_1 t}(1, 0)$, $X_2(t) = \beta e^{\lambda_2}t(0,1)$

   Now all solutions tend towards $(0,0)$ as $t \rightarrow \infin$ 

   How do they approach the origin? 

   To answer this, we compute the slope $dy/dx$ of a solution with $\beta \neq 0$ 

   We have

   $x(t) = \alpha e^\lambda_1 t \\ y(t) = \beta e^{\lambda_2t}$ 

   $\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{\beta\lambda_2 e^{\lambda_2t}}{\alpha\lambda_1 e^{\lambda_1t}} = \frac{\beta\lambda_2}{\alpha \lambda_1} e^{(\lambda_2 - \lambda_1)t}$ , since $\lambda_2 - \lambda_1 > 0$ 

   the slopes approach $\pm \infin$, provided $\beta \neq 0$ 

   So these solutions not only tend towards origin, but they do so tangentially to the $y$-axis 

   ![1536028631593](C:\Users\Renee\AppData\Local\Temp\1536028631593.png)

   We can call $\lambda_1$ the stronger eigenvalue. Since $\lambda_1 < \lambda_2 < 0$ the $x-coordinates$ of solutions tend to 0 much more quickly than the $y$-coordinates

   This accounts for why solutions, except those on the line corresponding to the $\lambda_1$ eigenvector, tend to "hug" the straight line solution corresponding to the weaker eigenvalue as they approach the origin.

   More generally, for a system with $\lambda_1 < \lambda_2 < 0$ with eigenvectors $(u_1, u_2)$ and $(v_1, v_2)$ respectively:

   General solution: $\alpha e^{\lambda_1t} \begin{pmatrix} u_1 \\ u_2 \end{pmatrix} + \beta e^{\lambda_2t}\begin{pmatrix} v_1 \\ v_2 \end{pmatrix}$ 

   the slope: $  \frac{dy}{dx} = \frac{\lambda_1\alpha e^{\lambda_1 - \lambda_2}t u_2 + \lambda_2\beta v_2}{\lambda_1\alpha e^{\lambda_1 - \lambda_2}t u_1 + \lambda_2\beta v_1} $ 

   Which tends towards the slope $v_2/v_1$ of the $\lambda_2$ eigenvector (weak), unless we have $\beta = 0$ 

   If $\beta = 0$, our solution is the straight line solution corresponding to the eigenvalue $\lambda_1$ (strong)

   This is why all solutions tend to the origin tangentially to the straight line solution corresponding to the weaker eigenvalue. (except for those on the strong straight line) 

3. $0 < \lambda_2 < \lambda_1$, Source

   Regarded as the negative of the previous excample. 

   The phase portrait looks the same, except all solutions tend away from (0,0) on the same path:

   ![1536029580129](C:\Users\Renee\AppData\Local\Temp\1536029580129.png)

so looking at  $  \frac{dy}{dx} = \frac{\lambda_1\alpha  u_2 + \lambda_2\beta e^{(\lambda_2 - \lambda_1)t} v_2 }{\lambda_1\alpha t u_1 + \lambda_2\beta e^{(\lambda_2 - \lambda_1)t} v_1}  $ , we have $\lambda_2 - \lambda_1 < 0$, so the slope as t increases tends towards $u_2/u_1$  and when $\alpha = 0$, we have the straight line solution $\beta e^{\lambda_2t}V$  

Any system of diff. eq.'s whose matrix has real distinct eigenvalues can be manipulated into the above by changing coordinates (change of bases)

If $B$ is the change of coordinates matrix that changes $U, V$ eigenvectors into $E_1, E_2$ respectively,

We have $B(\alpha e^{\lambda_1 t} U + \beta e^{\lambda_2 t} V) = \alpha e^{\lambda_1t} E_1 + \beta e^{\lambda_2 t} E_2$ 

Finally, a special case occurs if one of the eigenvalues is equal to 0. We have a straight line of equilibrium points this case. 

The sign of the other eigenvalue determines whether the other solutions tend toward or away from these equilibria

### 3.2 Complex Eigenvalues

When the roots of the char. polynomial are complex, we call them complex eigenvalues.

When the matrix A has complex eigenvalues, we no longer have straight line solutions.

#### Example. (Center) $A = \begin{pmatrix} 0 & \beta \\ -\beta & 0 \end{pmatrix}$ 

$\beta \neq 0$ , the char poly: $\lambda^2 + \beta^2$ the eigenvalues: $\pm i\beta$ 

We find the eigenvector corresponding to $i\beta$ in the usual way and get

$X(t) = e^{i\beta t} (1, i)$  as a complex solution to $X' = AX$ 

Euler's formula: $e^{i\beta t} = \cos \beta t + i \sin \beta t$

Rewrite the solution: $X(t) = \begin{pmatrix} \cos \beta t _ +i\sin \beta t \\ -\sin\beta t + i\cos \beta t \end{pmatrix}$ = $X_{Re}({t) + iX_{Im}(t)}$ 

Where $X_{Re}(t) = (\cos \beta t, -\sin \beta t)$, $X_{Im}(t) = (\sin\beta t, \cos\beta t)$, which are now real solutions to the original system:

$X'_{Re} + iX'_{Im} = X'(t) = AX = A(X_{Re} + iX_{Im}) = AX_{Re} + iAX_{Im}$

And equating the real and imaginary parts yields: $X'_{Re} = AX_{Re}$ and $X'_{Im} = AX_{Im}$ 

Then we claim this is the general solution of the equation and prove it by showing that these are the only solutions of the equation. We let $Y(t) = (u(t), v(t))$ be another solution, consider the complex function $f(t) = (u(t) +iv(t))e^{i\beta t}$ , differentiating it, we get $f'(t) = 0$ 

so $u(t) +iv(t) = Ce^{-i\beta t}$, where $C \in \C$ 

From this we have that $Y(t)$ is a linear combination of $X_{Re}(t)$ and $X_{Im}(t)$ 

The coefficients are going to be of the form $|C|\cos Arg C$, $|C| \sin Arg C$ 

Each of these solutions is a periodic function with period $2\pi/\beta$ 

Because: $\beta t = \beta t + \beta T$ and we have $\beta T = 2\pi$ 

if $\beta > 0$, circles traverse counterclockwise, if $\beta < 0$, circles traverse clockwise

![1536032501218](C:\Users\Renee\AppData\Local\Temp\1536032501218.png)

#### Example: (Spiral Sink, Spiral Source) $A = \begin{pmatrix} \alpha & \beta \\ -\beta & \alpha \end{pmatrix}$ 

$\alpha, \beta \neq 0$ The characteristic equation is now $\lambda^2 -2\alpha\lambda + \alpha^2 + \beta^2$ 

Eigenvalues are $\lambda = \alpha \pm i\beta$ 

$(1,i)$ is again an eigenvector corresponding to $\alpha + i\beta$ 

So $X_{Re} = e^{\alpha t} (\cos{\beta t}, -\sin{\beta t})$, $X_{Im} = e^{\alpha t}(\sin\beta t , \cos \beta t)$ , which are real solutions of the system whose initial conditions are linearly independent

w/o $e^{\alpha t}$ these solutions would wind periodically around circles centered at the origin

Spiral sink: When $\alpha < 0$, these solutions spiral towards origin since the radius is decreasing as t increases

Spiral source: When $\alpha > 0$, these solutions spiral away from origin since the radius is increasing as t increases

![1536213795047](C:\Users\Renee\AppData\Local\Temp\1536213795047.png)

### 3.3 Repeated Eigenvalues

#### Simple case: $A = \begin{pmatrix} \lambda & 0 \\ 0 & \lambda \end{pmatrix}$ 

In this case, every single nonzero vector is an eigenvector

$X(t) = \alpha e^{\lambda t}V$

each solution lies on a straight line through origin and either 

1. tends to origin if $\lambda < 0$
2. tend away from origin if $\lambda > 0$ 

#### Case when $A = \begin{pmatrix}  \lambda & 1 \\ 0 & \lambda \end{pmatrix}$ 

We only have one linearly independent eigenvector, $(1,0)$ 

We have only one straight line solution: $X_1(t) = \alpha e^{\lambda t}(1, 0)$  

Other solutions:

$x' = \lambda x + y \\ y' = \lambda y$ 

If $y \neq 0$, we must have $y(t) = \beta e^{\lambda t}$ 

and therefore the diff. eq. for $x(t)$ reads:

$x' = \lambda x + \beta e^{\lambda t}$, a nonautonomous, first-order diff. eq. 

Best option:

$x(t) = \alpha e^{\lambda t} + \mu te^{\lambda t}$ 

This technique is called the method of undetermined coefficients.

Note: since $\lambda$ is repeated , there is a $t$ in front of $\mu e^\lambda t$ 

the solution of the system is now:

$\alpha e^{\lambda t }(1,0) + \beta e^\lambda (t ,1)$

If $\lambda <0$, each term tends to 0 as t increases.

If $\lambda > 0​$, each term tends away from origin

![1536038564708](C:\Users\Renee\AppData\Local\Temp\1536038564708.png)

### 3.4 Changing Coordinates

Have dealt with only three types of matrices:

![1536034387669](C:\Users\Renee\AppData\Local\Temp\1536034387669.png)

Where $\lambda$ may equal $\mu$ in the first case. 

#### Canonical form

Any 2$\times$2 matrix that is in one of these three forms is said to be in canonical form.

Given any linear system $X' = AX$ , we can always "change coordinates" so that new system's coefficient matrix is in canonical form and hence easily solved. 

#### linear map or linear transformation 

on $\R^2$ is a function $T: \R^2 \rightarrow \R^2$ of the form

$T\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} ax +by \\ cx + dy \end{pmatrix}$ 

That is, $T$ simply multiplies any vector by the 2 $\times$ 2 matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ 

We will thus think of the linear map and its matrix as being interchangeable so that we also write:

$T = \begin{pmatrix} a& b \\ c& d\end{pmatrix}$ We hope no confusion will result from this slight imprecision

Suppose $T$ is invertible. This means that an *inverse matrix* $S$ that satisfies $TS = ST = I$ 

where $I$ is the 2$\times$2 identity matrix

$S = \frac{1}{\det T} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$

#### Proposition. The 2$\times$2 matrix $T$ is invertible if and only if $\det T \neq 0$ 

Consider a linear system 

$Y' = (T^{-1}AT)Y$ for some invertible linear map T.

Note that if $Y(t)$ is a solution of this new system, then $X(t) = TY(t)$ solves

$X' = AX$ 

The linear map $T$ converts solutions of $Y' = (T^{-1}AT)Y$ to solutions of $X' = AX$ 

$T^{-1}$ takes solutions of $X' = AX$ to solutions of $Y' = (T^{-1}AT)Y$  

#### Example. (Real Eigenvalues)

$TE_j = V_j$ , so $T = (V_1 \, \;V_2)$ 

$T^{-1}AT$ $= \begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ , if we have two distinct real eigenvalues

#### Example. (Complex Eigenvalues)

Now suppose that the matrix has eigenvalues, $\alpha \pm i\beta$ with $\beta\neq 0$ 

The complex vector $V_1 + iV_2$ is the eigenvector corresponding to $\alpha + i\beta$ 

We claim $V_1, V_2$ are linearly independent. (proof in book)

Equating real and imaginary components of $A(V_1 + iV_2) = (\alpha + i\beta)(V_1 +iV_2 )$ 

$AV_1 = \alpha V_1 - \beta V_2$

$AV_2 = \beta V_1 + \alpha V_2$ 

let $T$ be the matrix whose columns are $V_1$ and $V_2$ so $TE_j = V_j$ 

The canonical form $(T^{-1}AT)$ equals $\begin{pmatrix} \alpha & \beta \\ -\beta & \alpha \end{pmatrix}$ 

$\alpha > 0$ , spiral source

$\alpha = 0$, center

$\alpha < 0$, spiral sink

#### Example. (Repeated Eigenvalues)

If there exists a pair of linearly independent eigenvectors, then in fact $A$ must be in the form

$A = \begin{pmatrix} \lambda & 0 \\ 0 & \lambda \end{pmatrix}$  (exercise 15 proves this)

If there is only one linearly independent eigenvector:

Let $V$ be the eigenvector, and $W$ is a vector lin. ind. of $V$

Then $AW = \mu V + \nu W$, since any vector is a lin. comb of two lin. ind. vectors in $\R^2$ 

We claim that $\nu = \lambda$  (proof in book)

Finally, let $U = (1/\mu)W$ 

$AU = V + (\lambda/\mu)W$ = $V + \lambda U$ 

So letting $TE_1 = V, TE_2 = U$ 

We have $T^{-1}AT = \begin{pmatrix} \lambda & 1 \\ 0 & \lambda \end{pmatrix}$ 

## Chapter 4 Classification of Planar Systems

### 4.1 The Trace-Determinant Plane

$A = \begin{pmatrix} a& b \\ c&d \end{pmatrix}$ 

#### Characteristic Equation: $\lambda^2 - (a+d)\lambda + (ad-bc) = 0$ 

##### $\equiv \lambda^2 - (tr\,A)\lambda + \det A = 0$ 

##### $\lambda\pm = \frac{1}{2}(tr\,A \pm \sqrt{(tr\,A)^2-4\det A})$

##### $\lambda_+ + \lambda_- = tr\,A$

trace is the sum of the eigenvalues

##### $\lambda_+\lambda_- = \det A$ 

determinant is the product of the eigenvalues

##### T = tr A and D = det A

#### Trace-Determinant plane, (T,D)

Location of this point determines the geometry of the phase portrait

##### $T^2 - 4D$ says:

###### 1. Complex with nonzero imaginary part if $T^2 - 4D<0$

###### 2. Real and distinct if $T^2 - 4D > 0$

###### 3. Real and repeated if $T^2 - 4D = 0$ 

##### If $T^2 - 4D < 0$ 

$\alpha = T$ in $\alpha \pm i\beta$ 

###### 1. Spiral Sink if $T < 0$

###### 2. Spiral Source if $T > 0$ 

###### 3. Center if $T = 0$ 

##### If $T^2 -4D > 0$ 

since $D$ is the product of eigenvalues

###### 1. Saddle if D < 0

and using $T^2 < T^2 - 4D$ since $4D <  T^2 - T^2 = 0$

$T + \sqrt{T^2-4D} > 0$

$T - \sqrt{T^2 -4D} < 0$

###### 2. If $D > 0$ and $T<0$ then both $T \pm \sqrt{T^2-4D} < 0$, sink

###### 3. If $D > 0$ and $T > 0$ then both $T \pm \sqrt{T^2-4D} > 0$, source

###### 4. If $D = 0$ and $T \neq 0$, we have one zero eigenvalue

We have $T \pm T$ 

###### 5. If $D = 0$ and $T = 0$ we have two zero eigenvalues

we have $\lambda^2 = 0$ 

##### Visual Summary

###### ![1536600386984](C:\Users\Renee\AppData\Local\Temp\1536600386984.png)

###### Remarks

1. This is a two-dimensional representation of what is a four-dimensional space, so for each point, there are infinitely many different matrices corresponding to it.
2. There may be subtle differences in the phase portraits, such as the direction of rotation, or the possibility of one or two independent eigenvectors in the repeated eigenvalue case
3. This is the analog of the bifurcation diagram for planar linear systems
   1. A one parameter family of linear systems corresponds to a curve in the TD-plane. 
   2. Curve undergoes bifurcation when it crosses
      1. the T-axis
      2. the positive D-axis
      3. $T^2-4D = 0$ 

### 4.2 Dynamical Classification

------

##### flow: the function $\phi(t,X_0) = \phi_t(X_0)$, denotes the solution satisfying the initial condition $X_0$ 

##### time t map of the flow: $\phi_t$ 

###### Book gives example for $X' = \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}X$ , with $\phi_t(x_0, y_0) = (x_0e^{2t}, y_0e^{3t})$ 

##### homeomorphism: a function *h* that is one-to-one, onto, and continuous and whose inverse is also continuous

##### Two systems are considered dynamically equivalent if there is a function *h* 

##### Definition of conjugate systems:

Suppose $X' = AX$ and $X' = BX$ have flows $\phi^A$ and $\phi^B$. These two systems are topologically *conjugate* if there exists a homeomorphism $h: \R^2 \rightarrow \R^2$ that satisfies

$\phi^B(t, h(X_0)) = h(\phi^A(t, X_0))$  

The homeomorphism *h* is called a *conjugacy*. Thus a conjugacy takes the solution curves of $X'=AX$ to those of $X' = BX$ 

###### Example: one-dimensional linear diff. eqn.'s $x' = \lambda_1 x$ and $x' = \lambda_2 x$ 

Flows: $\phi^j(t,x_0) = x_0e^{\lambda_jt}$ for j = 1,2

Suppose $\lambda_1, \lambda_2$ are nonzero and have the same sign.

THEN let: $h(x) = \begin{cases} x^{\lambda_2/\lambda_1} & x\geq 0 \\ -|x|^{\lambda_2/\lambda_1} & x < 0\end{cases}​$

Recall: $x^{\lambda_2/\lambda_1} = \exp(\frac{\lambda_2}{\lambda_1}\log(x))$ 

Note: *h* is a homeomorphism of the real line.

We claim that *h* is a conjugacy between $x' = \lambda_1x$ and $x' = \lambda_2x$ 

Proof:

When $x_0 > 0$

$h(\phi^1(t,x_0)) = (x_0e^{\lambda_1t})^{\lambda_2/\lambda_1} \\ = x_0^{\lambda_2/\lambda_1}e^{\lambda_2t} \\ = \phi^2(t, h(x_0))$

 A similar computation works when $x_0 < 0$ $\square$

Note:

1. $\lambda_1$ and $\lambda_2$ must have the same sign, because otherwise we would have $|h(0)| = \infin$ , in which case *h* is not a homeomorphism 
   1. because $h'(x) = x^{\lambda_2/\lambda_1 -1}$ as $x \rightarrow 0$ either approaches $\infin$ or $0$ 
   2. $h$ is diff @ 0 iff $h^{-1}$ is not
2. *h* is not a diffeomorphism ( a diff. homeomorphism with diff. inverse)
3. For differentiability, we must have $\lambda_1 = \lambda_2$ 

#### Classification of autonomous linear first-order differential equations

There are three conjugacy "classes": sinks, sources, and special "in-between" case, $x' = 0$ 

1. as $x \rightarrow 0$, $h'(x) \rightarrow \infin$, if $\lambda_2 < \lambda_1$ 
2. as $x \rightarrow 0$, $h'(x) \rightarrow 0$, if $\lambda_2 > \lambda_1$
3. as $x \rightarrow 0$, $h'(x) \rightarrow 1$, if $\lambda_2 = \lambda_1$ 

OR?

1. Both tend towards origin, both $\lambda_j$ are negative
2. Both tend away from origin, both $\lambda_j$ are positive
3. Both have all solutions are constants, both $\lambda_j = 0$ 

#### Planar version of conjugacy

##### Definition: hyperbolic matrices

A matrix $A$ is hyperbolic if none of its eigenvalues has real part 0. We also say that the system $X' = AX$ is hyperbolic

##### Theorem:

Suppose that the $2\times 2$ matrices $A_1$ and $A_2$ are hyperbolic. Then the linear systems $X'  = A_iX$ are conjugate $\iff$ each matrix has the same number of eigenvalues with negative real part.

Thus two hyperbolic matrices yield conjugate linear systems if both sets of eigenvalues fall into the same category below:

1. One is positive, the other is negative, saddle (only real?)
2. both eigenvalues have negative real parts, sink, spiral sink
3. both eigenvalues have positive real parts, source, spiral source

###### Proof of the Theorem: may assume all systems are in canonical form

**Case 1: Saddle**

each $A_i$ has eigenvalues $\lambda_i < 0 < \mu_i$ 

$x' = \lambda_ix$, $y' = \mu_iy$

$h_1(x) = \begin{cases} x^{\lambda_2/\lambda_1} &  x \geq 0 \\ -|x|^{\lambda_2/\lambda_1} &  x < 0 \end{cases}$ , $h_2(y) = \begin{cases} y^{\mu_2/\mu_1} &  y \geq 0 \\ -|y|^{\mu_2/\mu_1} &  y < 0 \end{cases}$

$H(x,y) = (h_1(x), h_2(y))$

$H$ provides a conjugacy between the two systems

I believe we'd look at each $h_i$ the way we looked at the linear first-order case.

so there's like 4 different possibilities?

**Case 2: negative real parts**

Assume $A$ not in the form $\begin{pmatrix} \lambda & 1 \\ 0 & \lambda \end{pmatrix}$ 

So must be in either $\begin{pmatrix} \alpha & \beta \\ -\beta & \alpha \end{pmatrix}$ or $\begin{pmatrix} \lambda & 0 \\ 0 & \mu \end{pmatrix}$ 

with $\alpha, \lambda, \mu < 0$ 

Show that the systems is conjugate to $X' = BX$ where $B = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$ 

and then it follows that any two systems of this form are conjugate

NOTE: this proof uses dot products.

uses $X(\theta) = (\cos\theta, \sin\theta)$ and $AX(\theta)\cdot N(\theta) < 0$, so $AX(\theta)$ points back inside the circle

Each nonzero solution of $X' = AX$ crosses $S^1$ (unit circle) exactly once.?????????? (i'm guessing this is due to t being allowed to be less than 0)

Note $\phi^A_t(x,y)$ makes the solution for $X' = AX$ at (x,y) travel time $t$ 

$\phi^B_s\phi^A_t(x,y)$ goes along the solution for $X' = AX$ at (x,y) until time $t$, then we travel along the solution for $X' = BX$ at point $\phi_t^A(x,y)$ for time $s$ 

So basically, we found a conjugacy by fixing time $\tau$ for how long it takes for solution satisfying $X' = AX$ with origin $X_0 = (x_0, y_0)$ to intersect with the unit circle

Then we take this point to be an initial condition for $X' = BX$ and travel ***back*** time $\tau$, and this gives us $H(x_0, y_0)$, the necessary starting point for $X' = BX$  such that after time $t$ of going along this unique solution, we get the same point as if we passed $\phi_t^A(x_0,y_0)$ through $H$,  

So what $H$ does is take a point $(x,y)$ and make it travel the necessary time along solution $A$ to get to unit circle, then switches to solution $B$ and travels back that same time

https://en.wikipedia.org/wiki/Implicit_function_theorem

Are time maps continuous?

We know that $\phi(t,X_0)$ is continuous

so compositions of them are going to be continuous

Also, what happens when we keep $t$ constant and vary $X_0$?

I think since we assume that $F(x,y) = (f(t,x), g(t,y))$ possesses (continuous?) first order partial derivatives, then $\phi_t(X_0)$ is continuous?

http://www.math.jhu.edu/mathcourses/202/Florin_notes/notes_02-15-05.pdf

Choose $\delta = \epsilon *\exp-[ \max(\lambda, \mu)]$ where $\sqrt{(x-x_0)^2 + (y-y_0)^2} < \delta \implies \sqrt{(xe^{\lambda t}-x_0e^{\lambda t})^2 + (ye^{\mu t}-y_0e^{\mu t})^2} < \epsilon$

so as $(x,y) \rightarrow (x_0, y_0), \phi_t(x,y) \rightarrow \phi_t(x_0, y_0)$ 

And for showing $H(x,y)$ is continuous, we have not only products of $\phi$'s but products of composition of $\phi(\tau(x,y), x,y)$, so we'd need to show that $\tau$ is continuous

but the issue is that $\tau$ depends on $|\phi_t^A(x,y)| = 1$... need to use implicit function theorem to show $\tau$ is differentiable at (x,y)

<u>This proof can be used for the positive counterpart.</u>

**Case 3:**

Finally, suppose that $A = \begin{pmatrix} \lambda & 1 \\ 0 & \lambda \end{pmatrix}$ , $\lambda < 1$ 

...Read proof on page 71, easy to grasp if you can understand proof for case 2.



### 4.3 Exploration: A 3D Parameter Space

## Chapter 5 Higher Dimensional Linear Algebra

### 5.1 Preliminaries from Linear Algebra

Note: Since I've learned these things more or less, I'm just writing down concepts and theorems mentioned

#### Linear Independence and Dependence

#### Subspaces

##### Spanning sets

#### Matrix Operations

#### Reduced row echelon form

##### Elementary row operations

##### Elementary matrices

#### Invertible matrices

##### AX = V has a unique solution iff A is invertible

##### A is invertible iff the columns of A form a linearly independent set of vectors

#### Determinant 

##### $\det A = \sum_{k=1}^n(-1)^{1+k}a_{1k}\det A_{1k}$ 

$\det A = \sum_{k=1}^n(-1)^{j+k}a_{jk}\det A_{jk}$

##### Lower/Upper Triangular matrices have a determinant = product of diagonal entries

##### Let $A$ and $B$ be $n\times n$ matrices

###### if B is obtained by adding a multiple of one row of $A$ to another row of $A$, Then $\det B = \det A$ 

###### If $B$ is obtained by interchanging two rows of $A$ then $\det B = - \det A$ 

###### If $B$ is obtained by multiplying each element of a row of $A$ by $k$. Then $\det B = k \det A$ 

##### A is invertible iff $\det A \neq 0$ 

##### $\det(AB) = (\det A)(\det B)$ 

### 5.2 Eigenvalues and Eigenvectors

##### Distinct eigenvalues yield linearly independent eigenvectors

##### If $A$ has real distinct eigenvalues then there exists a matrix $T$ such that $T^{-1}AT$ is a diagonal matrix where the diagonal entries are the eigenvalues 

### 5.3 Complex Eigenvalues

##### any collection of eigenvectors corresponding to distinct eigenvalues is linearly independent 

##### If We have $2n$ distinct eigenvalues, $2n$ linearly independent complex eigenvectors, each of the real and imaginary parts of these vectors are linearly independent

##### The canonical form of a matrix with 2n distinct complex eigenvalues:

$\begin{pmatrix} D_1 & & \\ & \ddots & \\ & & D_n \end{pmatrix}$ , where each $D_j = \begin{pmatrix} \alpha_j & \beta_j \\ -\beta_j & \alpha_j \end{pmatrix}$ 

##### If A matrix has distinct eigenvalues (in general) the canonical form is a mix of $k$ real distinct eigenvalues in the diagonal and $2\times2$ blocks for the complex eigenvalues

### 5.4 Bases and Subspaces

#### Basis of a subspace: Linearly independent vectors that span the subspace

##### Every basis of a subspace has the same number of elements

##### Dimension of a subspace = # of elements in its basis

#### Linear map/ Linear Transformation

##### $T(\alpha X + \beta Y) = \alpha T(X) + \beta T(Y)$ 

##### Kernel and Range of a linear transformation

##### $\dim Kernel\; T + \dim Range\; T = n$ where $T$ is a linear transformation from $\R^n \rightarrow \R^n$ 

##### If $T$ is a linear map with $\dim Kernel \; T = 0$ , then $T$ is invertible 

### 5.5 Repeated Eigenvalues

##### If $A$ is an $n \times n$ matrix, then there is a change of coordinates $T$ for which $T^{-1}AT = \begin{pmatrix} B_1 & & \\ & \ddots & \\ & & B_k \end{pmatrix}$ , where each of the $B_j's$ is a square matrix of one of two forms

###### one eigenvalue along the diagonal with ones on the upper sub-diagonal

###### $2\times2$ matrices corresponding to complex eigenvalues along the diagonal with the $2\times 2$ identity matrices on the upper sub-diagonal

![1537850088085](C:\Users\Renee\AppData\Local\Temp\1537850088085.png)

Of course, $B_j = (\lambda)$ or $B_j = \begin{pmatrix} \alpha & \beta \\ -\beta & \alpha \end{pmatrix}$ is allowed

##### The idea for $3\times3$ matrices:

We have that either $R \sub K$ or $K \sub R$ where K is the kernel, R is the range

So there's a vector that maps to an eigenvector

Or there's 

#### When   you can't find enough linearly independent vectors:

Solve $(A - \lambda I)X = V$ for $X$, where $V$ is an eigenvector corresponding to $X$ 

### 5.6 Genericity

## Chapter 6 Higher Dimensional Linear Systems

### 6.1 Distinct Eigenvalues

#### Consider a linear system $X' = AX$ where $n\times n$ matrix $A$ has $n$ distinct, real eigenvalues, $\lambda_1, . . ., \lambda_n$  

There is a change of coordinates $T$ so that the new system $Y' = (T^{-1}AT)Y$ assumes the form

$y_1' = \lambda_1 y_1 \\ \vdots \\y_n' = \lambda_ny_n$ 

General solution: $Y(t) = (c_1e^{\lambda_1 t}, . . ., c_ne^{\lambda_n t})$ , $Y(0) = (c_1, . . ., c_n)$ 

##### Negative eigenvalues associated with stable subspace

##### Positive eigenvalues associated with unstable space

##### All solutions tend toward unstable subspace as time increases

##### A system with both negative and positive eigenvalues is the higher dim. analog of a saddle

#### General

$n = k_1 + 2k_2$, where we have $k_1$ real eigenvalues, $2k_2$ nonreal

System's form under change of coordinates:

$x'_j = \lambda_jx_j \\ u_l' = \alpha_l u_l + \beta_l v_l \\ v_l' = -\beta_l u_l + a_l v_l $ Solutions of the form: $x_j(t) = c_je^{\lambda_j t} \\ u_l(t) = p_le^{\alpha_l t}\cos\beta_l t + q_l e^{\alpha_l t}\sin\beta_l t \\ v_l (t) = -p_le^{\alpha_l t}\sin\beta_l t + q_l e^{\alpha_l t}\cos\beta_l t$ 

for $j = 1, . . , k_1$ , $l = 1, . . . , k_2$ 

##### Theorem for solutions for distinct eigenvalues $\lambda_j, \alpha_l + i \beta_l$ 

![1537863222455](C:\Users\Renee\AppData\Local\Temp\1537863222455.png)

#### Examples

##### Saddle in three dimensions

![1537863469643](C:\Users\Renee\AppData\Local\Temp\1537863469643.png)

##### Sink in three dimensions

![1537863498293](C:\Users\Renee\AppData\Local\Temp\1537863498293.png)

##### Spiral Center

![1537863558998](C:\Users\Renee\AppData\Local\Temp\1537863558998.png)

Any solutinos that doesn't lie on the stable line, (z-axis in this case) lies on a cylinder spiraling toward the circular solutino of radius $\sqrt{x_0^2 + y_0^2}$ in the $xy$-plane

##### Spiral Saddle 

![1537863690213](C:\Users\Renee\AppData\Local\Temp\1537863690213.png)

![1537863731574](C:\Users\Renee\AppData\Local\Temp\1537863731574.png)

I.e., has a positive real eigenvalue, and complex values with negative real part

### 6.2 Harmonic Oscillators

Pair of undamped harmonic oscillators whose eqn.'s are:

$x_1'' = -\omega_1^2x_1 \\ x_2'' = -\omega_2^2x_2$ 

Introduce $y_j = x_j'$ for $j = 1, 2$ to obtain a system:

$x_j' = y_j \\ y_j' = \omega_j^2 x_j$ 

$X = (x_1, y_1, x_2, y_2)$ 

and $A = \begin{pmatrix} 0 & 1 & & \\ -\omega_1^2 & 0 & & \\ && 0 & 1 \\ && -\omega_2^2 & 0 \end{pmatrix}$ 

System has eigenvalues: $\pm i\omega_1$ and $\pm i\omega_2$ 

$V_1 = (1, i\omega_1, 0, 0)$ $V_2 = (0, 0, 1, i\omega_2)$ 

$W_1, W_2$ be real, imaginary for $V_1$, $W_3, W_4$ be real, imaginary for $V_2$ 

letting $TE_j$ $=$$W_j$ 

$T^{-1}AT = $$\begin{pmatrix} 0 & \omega_1  & & \\ -\omega_1 & 0  && \\ && 0 & \omega_2 \\ && -\omega_2 & 0\end{pmatrix}$ 

#### Looking for a periodic solution with period $\tau$ 

$\equiv$ finding integers $m, n$ s.t. $\omega_1\tau = m\cdot 2\pi$ and $\omega_2 \tau = n \cdot 2\pi$ 

For periodicity we must have:

$\tau = \frac{2\pi m}{\omega_1} = \frac{2\pi n}{\omega_2}$

Or equivalently $\frac{\omega_2}{\omega_1} \in \Q$ 

#### Poincare map for...this

We look at things in terms of $(r,\theta)$ 

$r$ doesn't matter, as it stays constant, so we fix $r_1, r_2$ = 1

$f(x_0) = x_0 + 2\pi(\omega_2/\omega_1) \mod 2\pi$ 

$x_0$ = $\theta_2(0)$ is the initial $\theta_2$ coordinate on the circle

The Poincare map on the circle is a function that rotates points on the circle by angle $2\pi(\omega_2/\omega_1)$ 

##### Definition: The set of points $x_0, \; x_1 = f(x_0),\; x_2 = f(f(x_0)),\; . . .\; , x_n = f(x_{n-1})$ is called the orbit of $x_0$ under iteration of $f$ 

The orbit of $x_0$ tracks how our solution successively crosses $\theta_1=2\pi$ as time increases 

##### Proposition. Suppose $\omega_2/\omega_1$ is irrational. Then the orbit of any initial point $x_0$ on the circle $\theta_1 = 0$ is dense in the circle 

no way for $2\pi (\omega_2/\omega_1) \equiv 0 \mod 2\pi$ 

say we keep adding $2\pi(\omega_2/\omega_1)$ (m times)

since $m$ is rational (integer) and if it were possible for $m*\omega_2/\omega_1 = z$ where $z \in Z$ 

then contradiction: $\omega_2/\omega_1 = z/m \in \Q$ 

##### When irrational, masses come back very close to their initial positions over and over again due to density of these solutions

### 6.3 Repeated Eigenvalues

For simple example: $X' = \begin{pmatrix} \lambda & 1 & 0 \\ 0 & \lambda & 1\\ 0 & 0 & \lambda \end{pmatrix}X$ 

1. $x_3' = \lambda x_3$ $\implies$ $x_3(t) = c_3e^{\lambda t}$ 
2. $x_2' = \lambda x_2 + c_3e^{\lambda t}$ $\implies x_2(t) = c_2e^{\lambda t} + c_3te^{\lambda t}$ 
   1. $x_2 = c_2e^{\lambda t} + \alpha t e^{\lambda t}$ 
   2. find that $\alpha = c_3$ 
3. $x_1' = \lambda x_1 + c_2e^{\lambda t} + c_3te^{\lambda t}$ $\implies x_1 = c_1e^{\lambda t} + c_2te^{\lambda t} + c_3 \frac{t^2}2e^{\lambda t}$ 
   1. Normally would do $(\alpha + \beta t)e^{\lambda t}$ , but since homogeneous is not linearly independent, we multiply by t

Despite presence for polynomial terms in this solution when $\lambda < 0$ , the exponential term dominates and all solutions do tend to zero

### 6.4 The Exponential of a Matrix

$e^x = \sum_{k=0}^\infin \frac{x^k}k!$ 

#### Definition of exponential of a matrix $A$ (square)

$\exp(A) =\sum_{k=0}^\infin \frac{A^k}k! $ 

#### Examples

##### $A = \begin{pmatrix} \lambda & 0 \\ 0 & \mu \end{pmatrix}$ $\exp(A) = \begin{pmatrix} e^\lambda & 0 \\ 0 & e^\mu \end{pmatrix}$ 

##### $A = \begin{pmatrix} 0 & \beta \\ -\beta & 0 \end{pmatrix}$ $\exp(A) = \begin{pmatrix} \cos \beta & \sin \beta \\ -\sin \beta  & \cos \beta \end{pmatrix}$ 

##### $A = \begin{pmatrix} \lambda & 1 \\ 0 & \lambda \end{pmatrix}$ $\exp(tA) = \begin{pmatrix} e^{t\lambda} &  te^{t\lambda} \\ 0 & e^{t\lambda} \end{pmatrix}$  

#### Proving Convergence

Let $a_{ij}(k)$ denote the $ij$ entry of $A^k$ , $a = \max|a_{ij}|$ 

in general: $|a_{ij}(k)| \leq n^{k-1}a^k$

So $\sum_{k=0}^\infin\frac{a_{ij}(k)}{k!}|\leq  \exp na$ 

#### Proposition. Let $A, B$ and $T$ be $n\times n$ matrices. 

##### 1. If $B = T^{-1}AT, then \exp(B) = T^{-1}\exp(A)T$ 

##### 2. If $AB = BA$, then $\exp(A+B) = \exp(A)\exp(B)$ 

##### 3. $\exp(-A) = (\exp(A))^{-1}$ 

##### Lemma. for any two $n\times n$ matrices $A, B$ (see picture)

![1537870341954](C:\Users\Renee\AppData\Local\Temp\1537870341954.png)

##### $\exp(A)$ is invertible for every matrix A 

#### Proposition. If $V \in \R^n$ is an eigenvector of $A$ associated to the eigenvalue $\lambda$  then $v$ is also an eigenvector of $\exp(A)$ associated to $e^\lambda$ 

#### Proposition. 

##### $\frac{d}{dt} \exp(tA) = A\exp(tA) = \exp(tA)A$ 

#### Theorem. Let $A$ be an $n\times n$ matrix. Then the solution of the initial value  $X' = AX$ with $X(0) = X_0$ is $X(t) = \exp(tA)X_0$. Moreover, this is the only such solution 

### 6.5 Nonautonomous Linear Systems

#### $X' = A(t)X$ 

$A(t) = [a_{ij}(t)]$ is an $n\times n$  matrix depending continuously on time 

#### $X' = AX + G(t)$ 

First-order, linear, nonhomogeneous system

##### Forced Harmonic Oscillator

$X' = \begin{pmatrix} 0 & 1 \\ -k & -b\end{pmatrix}X + G(t)$, $G(t) = \begin{pmatrix} 0 \\ f(t)\end{pmatrix}$ 

#### Variation of Parameters

##### Theorem: Consider the non-homogenous equation $X' = AX + G(t)$ where $A$ is an $n\times n$ matrix and $G(t)$ is a continuous function of $t$ Then

$X(t) = \exp(tA) (X_0 + \int_0^t \exp(-sA)G(s)ds)$ 

is a solution of this equation satisfying $X(0) = X_0$ 

##### Theorem: Consider the forced, damped harmonic oscillator equation $x'' + bx' + kx = \cos t$ with $k, b> 0$. Then all solutions of this equation tend to the steady-state solution, which is periodic with period $2\pi$ 

## Chapter 7 Nonlinear Systems

### 7.1 Dynamical Systems

##### Will use analytic, geometric, and topological techniques to derive results about the behavior of solutions

##### dynamical system: a way of describing the passage in time of all points of a given space $\mathcal S$ 

Given an initial po





##### Given an initial position $X \in \R^n$, a dynamical system on $\R^n$ tells us where $X$ is located 1 unit of time later, 2 units of time later, etc.

###### We denote these new positions of $X$ by $X_1, X_2$, and so forth

##### The "trajectory" of $X$ is given by $X_t$ 

##### discrete dynamical system: using only integer time values

##### continuous dynamical system: time is measured continuously with $t \in \R$ 

##### Smooth dynamical system: system depends on time in a cont. diff. manner

##### Assume function $X_t$ is cont. diff. 

##### The map $\phi_t: \R^n \rightarrow \R^n$ that takes $X$ into $X_t$ is defined for each $t$ 

reasonable to expect an inverse $\phi_{-t}$ 

Identity function: $\phi_0(X) = X$ 

$\phi_t(\phi_s(X)) = \phi_{t+s}(X)$ 

#### Definition: A smooth dynamical system on $\R^n$ is a continuously differentiable function $\phi:\R\times \R^n \rightarrow \R^n$ where $\phi(t, X) = \phi_t(X)$ satisfies

##### 1. $\phi_0: \R^n \rightarrow \R^n$  is the identity function $\phi_0(X_0) = X_0$ 

##### 2. The composition $\phi_t \circ\phi_s=\phi_{t+s}$ for each $t,s \in \R$  

###### take $s = -t$ to get an inverse function

##### Continuously Diff: partial derivatives exist and are continuous 

##### Note: A function that is k times cont. diff. is called a $C^k$ function

### 7.2 The Existence and Uniqueness Theorem

$X' = F(X)$ 

$F: \R^n \rightarrow \R^n$, A solution is a function $X: J \rightarrow \R^n$ defined on some interval $J\sub \R$ such that for all $t \in J$ $X'(t)= F(X(t))$ 

Geometrically: $X(t)$ in $\R^n$ whose tangent vector $X'(t)$ exists for all $t \in J$ and equals $F(X(t))$ 

#### Nonlinear differential equations may have no solutions satisfying certain initial conditions

##### Example: $x' = \begin{cases} 1 & \text{if } x <0 \\ -1 & \text{if }x\geq 0  \end{cases}$ (not continuous at 0)

no solution for $x(0) = 0$, this means that it initially decreases, but then it becomes negative and needs to increase again...

Not defined for all time: $x(t) = x_0 - t$ if $x_0 > 0$ but then at $x_0$, see above.

##### Example: $x' = 3x^{2/3}$ (many different solutions to same initial value problem, not diff at 0)

for $u(0) = 0$: $u(t) \equiv 0$ and $u_0(t) = t^3$ , $u_{\tau}(t) = \begin{cases} 0 & \text{if }t\leq \tau \\ (t-\tau)^3 & \text{if }t> \tau\end{cases}$ 

$3x^{2/3}$ is not differentiable at 0

#### Conditions must be imposed on F to ensure existence and uniqueness

#### The Existence and Uniqueness Theorem

Consider the IVP: 

$X' = F(X), X(t_0) = X_0$

where $X_0 \in \R^n$ . Suppose that $F$ is $C^1$ 

Then:

1. There exists a solution of this IVP
2. The solution is unique
3. $\exists a>0$ and a unique solution $X:(t_0 - a, t_0+a) \rightarrow \R^n$ of this differential equation satisfying the initial condition $X(t_0) = X_0$ 

#### Picard Iteration

##### $u_{k+1} = x_0 +\int_0^tF(u_k(s))\mathrm\,{dt}$

##### Example: $x' = x$ 

###### Construct sequence of functions $u_k(t)$, one for each $k$, whic converges to the actual solution $x(t)$ as $k\rightarrow \infin$ 

$u_0(t) = x_0$ 

$u_1(t) = x_0 + \int_0^t u_0(s)ds = x_0 + \int_0^tx_0 ds$ 

$u_1(t) = x_0 +tx_0$ 

$u_2 = x_0 + \int_0^t(x_0 + sx_0)ds = x_0 + tx_0 +\frac{t^2}2x_0$ 

$u_{k+1}(t) = x_0\displaystyle\sum_{i=0}^{k+1}\frac{t^i}{i!}$

as $k \rightarrow \infin$ $u_k(t)$ converges to $x_0 e^t$ 

##### Example $X' = F(X) = \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix}X$ 

$X(0) = (1,0)$ 

Using Picard Iteration

#### We always have a unique solution defined on a maximal time domain

##### Example: $x' = 1+x^2$ 

$x(t) = \tan(t+c)$ 

cannot be extended over interval larger than 

$-c - \frac{\pi}2 < t < -c + \frac{\pi}2$ because

$x(t) \rightarrow \pm \infin$b as $t\rightarrow -c \pm \pi/2$ 

#### Theorem: Let $U \sub \R^n$ be an open set, and let $F: U \rightarrow \R^n$ be $C^1$. Let $X(t)$ be a solution of $X' = F(X)$ defined on a maximal open interval $J = (\alpha, \beta)\sub \R$ with $\beta < \infin$. Then given any closed and bounded set $K \sub U$, there is some $t \in (\alpha, \beta)$ with $X(t) \notin K$ 

##### if $X(t)$ cannot be extended to a larger time interval, then the solution leaves any closed and bounded set in $U$

##### X(t) must come arbitrarily close to the boundary of $U$ as $t\rightarrow \beta$ or $\alpha$ 

### 7.3 Continuous Dependence of Solutions 

#### Theorem: basically, if solutions $X(t), Y(t)$ start out close together, then they remain close together for $t$ close to $t_0$ 

##### Corollary (Continuous dependence on initial conditions) $\phi(t,X)$ , flow of system $X' = F(X)$ where $F$ is $C^1$ is continuous function of $X$ 

#### When do solutions depend continuously on parameters (e.g., $b, k$ in harmonic oscillator)

##### When system depends on the parameters in a cont. diff. fashion.

##### artificially augment system , $x_j' = f_j(x_1, . . ., x_n, a)$ for $j =1, . . ., n$ and $a' = 0$ 

#### Theorem: Continuous Dependence on Parameters

### 7.4 The Variational Equation

#### Theorem: (Smoothness of Flows)

##### $\frac{\partial \phi}{\partial t}(t,X_0) = F(\phi(t, X_0))$ 

$\frac{\partial \phi}{\partial X}(t, X_0) = D\phi_t(X_0)$

###### $D_{\phi_t}$ is the Jacobian of the function $X \rightarrow \phi_t(X)$

A(t) is a family of $n\times n$   matrices that depend continuously on $t$ 

The system $X' = A(t)X$ is linear, nonautonomous 

#### Theorem: Let $A(t)$ be continuous family of $n \times n$ matrices defined for $t \in [\alpha,\beta]$. Then the initial value problem $X' = A(t)X, X(t_0)  =X_0$ has a unique solution that is defined on the entire interval $[\alpha, \beta]$ 

Returning to autonomous, nonlinear system

$X' = F(X)$, let $X(t)$ be a particuluar solution defined for $t$ in some interval $J = [\alpha, \beta]$ 

fix $t_0 \in J$ set $X(t_0) = X_0$ 

let $A(t) = DF_{X(t)}$, where $DF_{X(t)}$ denotes the Jacobian matrix of $F$ at the point $X(t) \in \R^n$ 

#### Variational equation along solution $X(t)$ : $U' = A(t)U$ 

Importance: if $U(t)$ is a solution satisfying $U(t_0) = U_0$ then the function

$t \rightarrow X(t) + U(t)$ is a good approximation to the solution $Y(t)$ of the autonomous equation with initial value $Y(t_0) = X_0 + U_0$ provided $U_0$ is suff. small. 

#### Proposition. Consider the system $X' = F(X)$ where $F$ is $C^1$ Suppose

##### 1. X(t) is a soln. defined for all $t \in [\alpha, \beta]$ satisfying $X(t_0)= X_0$ 

##### 2. U(t) is the solution to the variational eqn. along $X(t)$ that satisfies $U(t_0) = U_0$ 

##### 3. Y(t) is the soln. of $X' = F(X)$ that satisfies $Y(t_0) = X_0 + U_0$ 

##### Then: $\lim_{U_0 \rightarrow 0}\frac{|Y(t)- (X(t)+U(t))}{|U_0|}$ converges to 0 uniformly in $t \in [\alpha, \beta]$ 

Convenient to use X+U instead of Y since U depends on $U_0$ linearly

#### Linearized System at $X_0$ the system $U' = AU$, where $A = DF_{X_0}$ 

the flow: $\exp(tA)U_0$ 

Near equilibrium points of a nonlinear system, the phase portrait resembles that of the corresponding linearized system.

#### Theorem: Let $X' = F(X)$ be a system of diff. eqn.'s where $F$ is $C^1$. Let $X(t)$ be a soln. of this system satisfying $X(0)= X_0$ and define for $t \in [\alpha, \beta]$, and let $U(t, U_0)$ be the solution to the variational equation along $X(t)$ that satisfies $U(0, U_0) = U_0$. 

##### Then $D\phi_t(X_0)U_0 = U(t, U_0)$ 

That is, $\partial\phi/\partial X$ applied to $U_0$ is given by solving the corresponding variational equation starting at $U_0$ 

### 7.5 Exploration: Numerical methods

### Note About Jacobian Matrix

$f$ is a function from $R^n \rightarrow R^m$ 

$f(x_1, . . . , x_n) = \begin{pmatrix} f_1(x_1, . . ., x_n) \\ \vdots \\ f_m(x_1, . . ., x_n)\end{pmatrix}$ 

The jacobian:

a matrix with components $J_{ij} = \frac{\partial f_i}{\partial x_j}$ 