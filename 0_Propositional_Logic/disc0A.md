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

(a) $(\exist x \in \mathbb{R})(x \notin \mathbb{Q})$

This statement is true, $\pi$, $e$, $\sqrt{2}$ , for example.

(b) $(\forall x \in \mathbb{Z})(((x \in \mathbb{N})\or(x < 0)) \and \neg ((x \in \mathbb{N})\and (x < 0))$

True. Natural numbers are integers which are not negative.

(c) $(\forall x \in \N) ((6 \mid x) \implies ((2 \mid x) \or (3 \mid x))$

True. $x = 6n = 2\times(3n) = 3\times(2n)$

(d) All integers are rational numbers.

True. 

(e) If an integers is divisible by 2 or it is divisible by 3, it is divisible by 6.

False. 4 is divisible by 2 but not divisible by 6.

(f) If a natural number is larger than 7, it can be the sum of two natural numbers.

True. a = x, b = 0;a = x - 1, b = 1; etc.



### 3. Logical Equivalence?

Decide whether each of the following logical equivalences is correct and justify your answer.

(a)	$\forall x (P(x)\and Q(x)) \equiv \forall x P(x) \and \forall x Q(x)$



Correct.



(b)	$\forall x (P(x) \or Q(x)) \equiv \forall x P(x) \or \forall x Q(x)$



Incorrect. 

Counterexample: $\forall x (x>3 \or x \leq 3)$ is true but $\forall x(x >3) \or \forall x (x \leq 3)$ is false.



(c)	$\exist x (P(x) \or Q(x)) \equiv \exist x P(x) \or \exist x Q(x)$



Correct.



(d)	$\exist x (P(x) \and Q(x)) \equiv \exist x P(x) \and \exist x Q(x)$



Incorrect.

Counterexample: $\exist x(x>3) \and \exist x (x\leq 3)$ is true but $\exist x ((x >3) \and (x \leq 3)$ is false.:
