### 1. Truth Tables

$P\bigwedge Q$ is **True** if both P and Q are **True**; $P\bigvee Q$ is **True** if one of P or Q is **True**.

(a) P∧(Q∨P) ≡ P∧Q

(b) (P∨Q)∧R ≡ (P∧R)∨(Q∧R)

(c) (P∧Q)∨R ≡ (P∨R)∧(Q∨R)

(a) not equivalent.
```math
\begin{array}{cc|c|c}
	       P&Q&P\bigwedge (Q\bigvee P)&P\bigwedge Q\\\hline
	       T&T&T&T\\
	       T&F&T&F\\
	       F&T&F&F\\
	       F&F&F&F
\end{array}
```

(b) equivalent.
```math
\begin{array}{ccc|c|c}
	       P&Q&R&(P\bigvee Q)\bigwedge R&(P\bigwedge R)\bigvee (Q\bigwedge R)\\\hline
	       T&T&T&T&T\\
	       T&T&F&F&F\\
	       T&F&T&T&T\\
	       T&F&F&F&F\\
	       F&T&T&T&T\\
	       F&T&F&F&F\\
	       F&F&T&F&F\\
	       F&F&F&F&F
\end{array}
```
(c) equivalent.
```math
\begin{array}{ccc|c|c}
	       P&Q&R&(P\bigwedge Q)\bigvee R&(P\bigvee R)\bigwedge (Q\bigvee R)\\\hline
	       T&T&T&T&T\\
	       T&T&F&T&T\\
	       T&F&T&T&T\\
	       T&F&F&F&F\\
	       F&T&T&T&T\\
	       F&T&F&F&F\\
	       F&F&T&T&T\\
	       F&F&F&F&F
\end{array}
```



### 2. Propositional Practice

(a) There is a real number which is not rational.

(b) All integers are natural numbers or are negative, but not both.

(c) If a natural number is divisible by 6, it is divisible by 2 or it is divisible by 3. 

(d) (∀x∈Z)(x∈Q)

(e) (∀x∈Z)(((2|x)∨(3|x)) ⇒ (6|x))

(f) (∀x∈N)((x>7) ⇒ ((∃a,b∈N)(a+b=x)))



**Answer:**

(a) $(\exists x \in \mathbb{R})(x \notin \mathbb{Q})$

This statement is true, $\pi$, $e$, $\sqrt{2}$ , for example.

> $(\exists x \in \mathbb{R})(x \notin \mathbb{Q})$, or equivalently $(\exists x \in \mathbb{R}) \neg (x \in \mathbb(Q))$. This is true, and we can use π as an example to prove it.

(b) $(\forall x \in \mathbb{Z})(((x \in \mathbb{N})\lor(x < 0)) \land \neg ((x \in \mathbb{N})\land (x < 0))$

True. Natural numbers are integers which are not negative.

> $(\forall x \in \mathbb{Z})(((x \in \mathbb{N})\lor(x < 0)) \land \neg ((x \in \mathbb{N})\land (x < 0))$. This is true, since we define the naturals to contain all integers which are not negative.

(c) $(\forall x \in \mathbb{N}) ((6 \mid x) \implies ((2 \mid x) \lor (3 \mid x))$

True. $x = 6n = 2\times(3n) = 3\times(2n)$

> $(\forall x \in \mathbb{N}) ((6 \mid x) \implies ((2 \mid x) \lor (3 \mid x)))$. This is true, since any number divisible by 6 can be written as $6k = (2 · 3)k = 2(3k)$, meaning it must also be divisible by 2.


(d) All integers are rational numbers.

True. 

> All integers are rational numbers. This is true, since any integer number n can be written as n/1.

(e) If an integers is divisible by 2 or it is divisible by 3, it is divisible by 6.

False. 4 is divisible by 2 but not divisible by 6.

>  Any integer that is divisible by 2 or 3 is also divisible by 6. This is false–2 provides the easiest counterexample. Note that this statement is false even though its converse (part c) is true.

(f) If a natural number is larger than 7, it can be the sum of two natural numbers.

True. a = x, b = 0;a = x - 1, b = 1; etc.
> If a natural number is larger than 7, it can be written as the sum of two other natural numbers. This is trivially true, since we can take a = x and b = 0. (Aside: this is a refererence to the very weak Goldback Conjecture (https://xkcd.com/ 1310/).)


### 3. Logical Equivalence?

Decide whether each of the following logical equivalences is correct and justify your answer.

(a)	$\forall x (P(x)\land Q(x)) \equiv \forall x P(x) \land \forall x Q(x)$



Correct.

> **Correct.**
Assume that the left hand side is true. Then we know for an arbitrary $x \ P(x) \land Q(x)$ is true.
This means that both $\forall x P(x)$ and $\forall x Q(x)$. Therefore the right hand side is true.
Now for the other direction, assume that the right hand side is true. Since for any $xP(x)$ and for any $yQ(y)$ holds, then for an arbitrary $x$ both $P(x)$ and $Q(x)$ must be true. Thus the left hand side is true.


(b)	$\forall x (P(x) \lor Q(x)) \equiv \forall x P(x) \lor \forall x Q(x)$



Incorrect. 

Counterexample: $\forall x (x>3 \lor x \leq 3)$ is true but $\forall x(x >3) \lor \forall x (x \leq 3)$ is false.

> **Incorrect.**
> Note, there are many possible counterexamples - here we present only one. Suppose that the universe (i.e. the values that $x$ can take on) is ${1, 2}$ and that $P$ and $Q$ are truth functions defined on this universe. If we set $P(1)$ to be true, $Q(1)$ to be false, $P(2)$ to be false and $Q(2)$ to be true, the left-hand side will be true, but the right-hand side will be false. Hence, we can find a universe and truth functions $P$ and $Q$ for which these two expressions have different values, so they must be different.

(c)	$\exists x (P(x) \lor Q(x)) \equiv \exists x P(x) \lor \exists x Q(x)$


Correct.

> **Correct**
> Assuming that the left hand side is true, we know there exists some $x$ such that one of $P(x)$ and $Q(x)$ is true. Thus $\exists x P(x) \lor \exists x Q(x)$ and the right hand side is true. To prove the other direction, assume the left hand side is false. Then there does not exists an $x$ for which $P(x) \lor Q(x)$ is true, which means there is no x for which $P(x)$ or $Q(x)$ is true. Therefore the right hand side is false.

(d)	$\exists x (P(x) \land Q(x)) \equiv \exists x P(x) \land \exists x Q(x)$



Incorrect.

Counterexample: $\exists x(x>3) \land \exists x (x\leq 3)$ is true but $\exists x ((x >3) \land (x \leq 3)$ is false.

> **Incorrect.**
> Note, there are many possible counterexamples - here we present only one. Suppose that the universe (i.e. the values that $x$ can take on) is the natural numbers $\mathbb{N}$, and that $P$ and $Q$ are truth functions defined on this universe. If we set $P(1)$ to be true and $P(x)$ to be false for all other $x$, and $Q(2)$ to be true and $Q(x)$ to be false for all other $x$, then the right hand side would be true. However, there would be no value of $x$ at which both $P(x)$ and $Q(x)$ would be simultaneously true, so the left hand side would be false. Hence, we can find a universe and truth functions $P$ and $Q$ for which these two expressions have different values, so they must be different.
