### 1 Truth Tables

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


### 2 Propositional Practice
(a) There is a real number which is not rational.

(b) All integers are natural numbers or are negative, but not both.

(c) If a natural number is divisible by 6, it is divisible by 2 or it is divisible by 3. 

(d) (∀x∈Z)(x∈Q)

(e) (∀x∈Z)(((2|x)∨(3|x)) =⇒ (6|x))

(f) (∀x∈N)((x>7) =⇒ ((∃a,b∈N)(a+b=x)))
