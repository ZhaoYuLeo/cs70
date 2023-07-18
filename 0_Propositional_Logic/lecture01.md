# Introduction

##### Tips

Proofs is all about convincing others.

Repetition and practice is the only way to learn the material

If you read a paragraph and it doesn't make sense, read it again!

##### Terminology

- "Formally"
    - Framing something in precise mathematical terms
    - Think of this as using "proofy" syntax, much like any programming language's syntax

- "Intuitively"
    - A fancy way of saying "not mathy"
    - Think of this as "opposite of formally" (or a way to get partical credit if you're stuck)

- Divides("|")
    - formally, if a | b, there exists some q such that aq = b (and vice versa)

- Parity(even/odd)
    - if n is even, there exists some k such that n = 2k (and vice versa)
    - if n is odd, there exists some k such that n = 2k + 1 (and vice versa)
    - a number cannot be both even and odd

### Note0

##### Cardinality

the size of a set, its cardinality. If *A* = {1,2,3,4}, then the cardinality of *A*, denoted by |*A*|, is 4. 

##### Subsets and Proper Subsets

If every element of a set *A* is also in set *B*, then we say that *A* is a **subset** of *B*, written *A* ⊆ *B*.

**proper subset**,  *A* ⊂ *B*, meaning that *A* excludes at least one element of *B*.

##### Intersections and Unions

**intersection**, both in A and in B; **disjoint**, *A*∩*B*=∅; **union**, either in A or in B or both

##### Complements

|   Symbol    | Digraph | Latex     | Comment                                                      |
| :---------: | ------- | --------- | ------------------------------------------------------------ |
| $\setminus$ |         | \setminus | [set difference](https://oeis.org/w/index.php?title=Set_difference&action=edit&redlink=1) |
|   $\mid$    |         | \mid      | divides                                                      |
|  $\notin$   |         | \notin    | is not member of                                             |
|    $\ne$    |         | \ne       | is not equal to                                              |

If *A* and *B* are two sets, then the **relative complement** of *A* in *B*, or the **set difference** between *B* and *A*, written as $B − A$ or $B \setminus A$, is the set of elements in *B*, but not in *A*:  $B \setminus A ={x \in B \mid x \notin A}$. 

$A \setminus A = \emptyset$ ; $A \setminus \emptyset = A$;  $\emptyset \setminus A = \emptyset$ 

##### Significant Sets

$\N$ $\Z$ $ \Q$ $ \R$ $\C$

##### Products and Power Sets

The **Cartesian product** (also called the **cross product**) of two sets A and B, written as $A \times B$. In set notation, $A \times B = \{(a,b)\mid a\in A, b \in B\}$. $\N \times \N = \{(0,0),(1,0),(0,1),(1,1),(2,0),...\}$. 

|    Symbol    | Digraph | Latex      | Comment                 |
| :----------: | ------- | ---------- | ----------------------- |
| $\mathscr P$ |         | \mathscr P | the power set operation |

The **power set** of S, denoted by $\mathscr P(S)$ , is the set of all subsets of S: $\{T \mid T \subseteq S\}$.

If $S = \{1,2,3\}$, then the power set of S is: $\mathscr P (S) = \{\{\}, \{1\}, \{2\}, \{3\}, \{1,2\}, \{1,3\}, \{2,3\}, \{1,2,3\}\}$.

Note that, if $|S| = k$, then $\mathscr P(S) = 2^k$. (All elements in S, in the subset or not in the subset.)

##### Mathematical Notation

$$\sum^{n}_{i=1}i = 1 + 2 + \cdots +n$$

$$\sum^{n}_{i=m}f(i) = f(m) + f(m+1) + \cdots + f(n)$$

$$\prod^{n}_{i=1}i = 1\cdot 2\cdots n$$

$$\prod^{n}_{i=m}f(i) = f(m)f(m+1)\cdots f(n)$$

The statement $(\forall n \in \N) (n^2+n+41\ is \ prime)$ is false. $41^2 + 41 + 41$

$(\exists x \in \Z)(x < 2\ and\ x^2 = 4)$ is true.

$(\forall x \in \Z)(\exists y \in \Z)(y > x)$: given an integer, we can find a larger one.

$(\exists y \in \Z)(\forall x \in \Z)(y > x)$: there is a largest integer!

# Propositional Logic

##### Propositons, Truth tables

| Symbol | Digraph | Latex    | Example |
| ------ | ------- | -------- | ------- |
| ∧      | <C-k>AN | \land    | P∧Q     |
| ∨      | <C-k>OR | \lor     | P∨Q     |
| ¬      | <C-k>NO | \neg     | ¬P      |
| ⇒      | <C-k>=> | \implies | P⇒Q     |

##### Implication

```python
def some_func(x):
    """
    >>> some_func(5):
    3
    >>> some_func(5)
    12
    """
    if x == 5:
        return 3

def test(x):
    return not (x == 5 and some_func(x) != 3)
```

P is the antecedent (or hypothesis/premise)
Q is the consequent (or conclusion/outcome)

| P(x==5) | Q(s.f.x.==3) | R(test(x)) | ¬P∨Q |
| :-----: | :----------: | :--------: | :--: |
|    T    |      T       |     T      |  T   |
|    T    |      F       |     F      |  F   |
|    F    |      T       |     T      |  T   |
|    F    |      F       |     T      |  T   |

Two propositional forms are logically equivalent if their truth tables are identical.

for example, $p \Rightarrow Q \equiv  \neg P\lor Q$

| Symbol | Digraph | Latex  | Example |
| ------ | ------- | ------ | ------- |
| ≡      | <C-k>=3 | \equiv | A≡A     |
| ⇔      | <C-k>== | \Leftrightarrow | P⇔Q     |

If pigs can fly, cats can talk
implications for which P is always false are called “vacuously true”

The **converse** of P ⇒ Q is Q ⇒ P
The **contrapositive** of P ⇒ Q is ¬Q ⇒ ¬P (implication and contrapositive are logically equivalent)
P ⇔ Q (If an implication and its converse are both true), "**P if and only if Q**" (iff)

Q: (P ⇒ Q) ⇒ (Q ⇒ P)?
A: This is true iff P ⇔ Q.

##### Quantifiers

x + 3 = 5, quantifiers it over some "universe", universal quantifier, existential quantifier.

| Symbol           | Digraph    | Latex     | Comment                                                      |
| ---------------- | ---------- | --------- | ------------------------------------------------------------ |
| ∀                | <C-k>FA    | \forall   | [for all](https://oeis.org/wiki/For_all)                     |
| ∃                | <C-k>TE    | \exists   | [there exists at least one](https://oeis.org/wiki/There_exists_at_least_one) |
| ∅ or $\emptyset$ | <C-k>/0    | \emptyset | the [empty set](https://oeis.org/wiki/Empty_set)             |
| ℤ                | <C-v>u2124 | \Z        | set of [integers](https://oeis.org/wiki/Integers)            |
| ℕ                | <C-v>u2115 | \N        | set of [natural numbers](https://oeis.org/wiki/Natural_numbers) |
| ℝ                | <C-v>u211D | \R        | set of [real numbers](https://oeis.org/wiki/Real_numbers)    |
| ∈                | <C-k>(-    | \in       | is member of                                                 |
| ∋                | <C-k>-)    | \ni       | owns (has member)                                            |
| ⊆                | <C-k>(_    | \subseteq | is subset of                                                 |
| ⊇                | <C-k>)_    | \supseteq | is superset of                                               |
| ⊂                | <C-k>(C    | \subset   | is proper subset of                                          |
| ⊃                | <C-k>)C    | \supset   | is proper superset of                                        |
| ∩                | <C-k>(U    | \cap      | [set intersection](https://oeis.org/w/index.php?title=Set_intersection&action=edit&redlink=1) |
| ∪                | <C-k>)U    | \cup      | [set union](https://oeis.org/w/index.php?title=Set_union&action=edit&redlink=1) |
| $\Q$             |            | \Q        | set of all rational numbers                                  |
| $\C$             |            | \C        | set of all complex numbers                                   |

 

##### DeMorgan’s Laws

 (Naming something after yourself is the old way of commenting "first!")

- ¬(P ∧ Q) ≡ ¬P ∨ ¬Q
- ¬(P ∨ Q) ≡ ¬P ∧ ¬Q

- ¬(∀xP(x)) ≡ ∃x¬P(x)
- ¬(∃xP(x)) ≡ ∀x¬P(x)

### Note1

##### Propositional logic

Propositions should not include fuzzy terms.

(6) Arnold Schwarzenegger often eats broccoli. [What is "often?"]

(7) Henry VIII was unpopular. [What is "unpopular?"]

<!--remainds me of many things-->

Propositions joined together to form more complex statements.

**Conjunction**	$P\and Q$, **Disjunction** $P \or Q$, **Negation** $\neg P$. Statements like these, with variables, are called *propositional forms*.

the **law of the excluded middle** says that, for any proposition $P$, either $P$ is true or $\neg P$ is true (but not both). Thus $P \and \neg P$ is always true, regardless of the truth value of $P$.

A propositional form that is always true regardless of the truth values of its variables is called a *tautology*.

Conversely, a statement such as $P \and \neg P$, which is always false, is called a *contradiction*.

$P$ stand for the proposition "3 is odd", $Q$ stand for "4 is odd", and $R$ for "4 + 5 = 49". 

If P was true, Q is false. If P was false, Q is true. Either P is true or Q is true. Thus $P \and Q$ is false.  $P \or Q$ is true.

$P \and R$ is false.

$P \or R$ is true.

$\neg Q$ is false.

**Truth table** are the same as function tables: you list all possible input values for the variables, and then list the outputs given those inputs.

**Implication** $P \implies Q$. This is same as "If P, then Q." is **logically equivalent** to $\neg P \or Q$, written as $(P \implies Q) \equiv (\neg P \or Q)$.

if P,then Q; <u>P if only Q;</u> Q if P; P is sufficient for Q; Q is necessary for P; Q unless not P.

##### Quantifiers

Two **quantifiers**: The *universal quantifier* ∀ (“for all”) and the *existential quantifier* ∃ (“there exists”).

The reason is that in these examples, there is an underlying "<u>universe</u>" that we are working in, and the statement are *quantified* over that universe.

We refer to a statement which refers to a variable as a *predicate* or as a *propositional formula* when replacing the variable with a value makes the statement either true or false. <!--not a proposition but a propositional formula since you can replace the variable with any kind of value. This statements assert something about lots of simple propositions all at once.-->

If our universe $U$ is $\{1,2,3,4\}$, then $(\exists x \in U)P(x) \equiv P(1) \or P(2) \or P(3) \or P(4)$, and $(\forall x \in U)P(x) \equiv P(1) \and P(2) \and P(3) \and P(4)$.



Some statements can have multiple quantifiers. However, quantifiers do not commute.

Poor Joe and larger integer.



##### Much Ado About Negation

$$\neg (P \and Q) \equiv (\neg P \or \neg Q)$$

Negating propositions involving quantifiers actually follows analogous laws.

$$\neg (\forall x P(x)) \equiv \exists x (\neg P(x))$$



$$\neg(\forall x \exists y P (x,y)) \equiv \exists x (\neg (\exists y P(x,y))) \equiv \exist x (\forall y(\neg P(x, y))) \equiv \exists x\forall y\neg P(x, y)$$

the negation goes inside, the quantifiers "flip"



"there are at least three distinct integers x that satisfy P(x)"

$$\exists x \exist y \exist z (x \neq y \and y \neq z \and z \neq x \and P(x) \and P(y) \and P(x))$$

(all quantifiers are over the universe $\Z$ of integers.)



"there are **at most** three distinct integers x that satisfy P(x)"

$$\exist x \exist y \exist z \forall d(P(d) \implies d = x \or d = y \or d = z)$$.

$$\forall x \forall y \forall v \forall z ((x \neq y \and y \neq v \and v \neq x \and x \neq z \and y \neq z \and v \neq z) \implies \neg(P(x) \and P(y) \and P(v) \and P(z)))$$.



"there are **exactly** three distinct integers x that satisfy P(x)"

*Conjunction* of the two propositions above.
