# Homework Solutions: Markov Chains, Transition Matrices, and Stationarity

## Problem 1

From state 1, $\pi_1=(0.8,0.2)$ and
$\pi_2=(0.8,0.2)P=(0.70,0.30)$. Continuing,
$\pi_3=(0.65,0.35)$, so the requested probability is $0.35$.
For a stationary vector $(a,1-a)$, the first coordinate equation is
$a=0.8a+0.3(1-a)$, giving $a=0.6$. Thus $\pi=(0.6,0.4)$.
The self-loops and communication in both directions make this finite chain
irreducible and aperiodic, so initial effects decay.

## Problem 2

The path probability is
$P_{23}P_{32}P_{23}=0.2(0.5)(0.2)=0.02$. State 1 is absorbing; states 2
and 3 are transient because both can eventually reach 1. Absorption by time 2
from state 2 occurs on step 1 or on step 2 after remaining in state 2:
$$
0.4+0.4(0.4)=0.56.
$$
There is a unique stationary distribution, $(1,0,0)$, because the only closed
class is the absorbing state 1.

## Problem 3

Let $\pi=(a,b,c)$. The first-coordinate equation gives
$0.5a+0.2b=a$, so $a=0.4b$. The third gives
$c=0.3b+0.6c$, hence $c=0.75b$. Normalizing gives
$(a,b,c)=(8/43,20/43,15/43)$. Multiplication confirms the same vector.
Starting at state 1, $\pi_1=(0.5,0.5,0)$, so the state-3 indicator mean is
$0$. Then $\pi_2=\pi_1P=(0.35,0.5,0.15)$, so it is $0.15$ after two steps.
Positive diagonal entries make the chain aperiodic; combined with
irreducibility, this supports convergence to the stationary vector.

## Problem 4

One trajectory algorithm is: draw $X_0\sim\pi_0$; for $n=0,\ldots,99$, draw
$U\sim\operatorname{Uniform}(0,1)$ and choose the smallest state $j$ whose
cumulative row probability $\sum_{k\le j}P_{X_nk}$ exceeds $U$; store
$X_{n+1}$. For 50,000 independent paths, the mean of
$\mathbf1\{X_{10}^{(r)}=4\}$ estimates $P(X_{10}=4)$. For one long path,
discard the first 1,000 states and average $\mathbf1\{X_n=4\}$ over the next
100,000; this estimates the stationary mass. Initial-state choice and
insufficient burn-in can bias the latter, while finite sample size creates
variance in both. Dependence along one path usually makes its effective sample
size smaller.

## Problem 5

For transient states, $Q=\begin{bmatrix}0.5&0.3\\0.4&0.6\end{bmatrix}$ and
$R=(0.2,0)^T$. Since
$$
I-Q=\begin{bmatrix}0.5&-0.3\\-0.4&0.4\end{bmatrix},\qquad
N=(I-Q)^{-1}=\begin{bmatrix}5&15/4\\5&25/4\end{bmatrix},
$$
the absorption probabilities are $NR=(1,1)^T$. The expected visit counts
starting in states 2 and 3 are the rows of $N$; expected absorption times are
row sums, $35/4$ and $45/4$. First-step recursion gives
$h_2=1+0.5h_2+0.3h_3$ and
$h_3=1+0.4h_2+0.6h_3$, whose solution is $(35/4,45/4)$.
