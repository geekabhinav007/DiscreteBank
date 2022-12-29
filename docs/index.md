# Discrete

## Sets

### EQUIVALENT SETS

- Two sets A and B are said to be equivalent if their cardinal number is same, i.e.,n(A) = n(B).
- The symbol for denoting an equivalent set is‘↔’.

### OVERLAPPING SETS

Two sets A and B are said to be overlapping if
they contain at least one element in common.

### DISJOINT SETS

Two sets A and B are said to be disjoint, if theydo not have any element in common.

### EQUAL SETS

- Two sets A and B are said to be equal if they contain the same elements.
- Every element of A is an element of B and every element of B is an element of A.

### PROPER SUBSET

- If A and B are two sets, then A is called the proper subset of B if A ⊆ B but B ⊇ A i.e., A ≠ B. The symbol ‘⊂’ is used to denote proper subset. Symbolically, we write A ⊂ B.

### POWER SET

The collection of all subsets of set A is called the power set of A. It is denoted by P(A). In P(A), every element is a set.

#### Formula for power set

`n[P(A)] = 2^m`
<br>
where m is the number of elements in set A.

### OPERATIONS ON SETS

- UNION
- INTERSECTION
- DIFFERENCE
- COMPLEMENT
- SYMMETRIC DIFFERENCE

**Difference** : The difference of two sets A and B is a set of all those elements which belong to A but do not belong to B and is denoted by A - B or A/B

**SYMMETRIC DIFFERENCE** : The symmetric difference of two sets A and B is the set containing all the elements that are in A or in B but not in both and is denoted by AΘB.

```
i.e., A ⊕ B = (A ∪ B)\(A ∩ B) or
A ⊕ B = (A\B) ∪ (B\A)
Eg. A={1,2,3,4,5} B={4,5,6,7,8}
(A u B)= { 1,2,3,4,5,6,7,8}
(A n B)= {4,5}
A ⊕ B = (A u B) - (A n B) = { 1,2,3,6,7,8}
```

### Laws of set theory

![laws](https://raw.githubusercontent.com/geekabhinav007/DiscreteBank/main/docs/img/dis3.png)

### INCLUSION–EXCLUSION PRINCIPLE

Suppose A and B are finite sets and they are not disjoint.
Then

```
n(A ∪ B) = n(A) + n(B) − n(A ∩ B)
```

Also suppose A, B, C are finite sets.
Then
`A ∪ B ∪ C is finite`
and

```
n(A ∪ B ∪ C) = n(A) + n(B) + n(C) − n(A ∩ B) −n(A ∩ C) − n(B ∩ C) + n(A ∩ B ∩ C)
```

## Relations

- In set order doesn't matters but in relation it's matters a lot.
- if A and B are sets with m‟ and „n‟ elements respectively. Then total number of ordered pairs will be `A × B= mn`. So the total number of relations from A to B is `2^(mn).`

### Properties of relations

### Types of relations

- Reflexive Relations
- Symmetric Relation
- Antisymmetric Relation
- Transitive Relations
- EQUIVALENCE RELATION

### Composition of relations

-  Let A, B and C be sets, and let R be a relation from A to B and let S be a relation from B to C.That is, R is a subset of A × B and S is a subset of B × C. Then R and S give rise to a relation from A to C denoted by R◦S
- R ◦ S = {(a, c) | there exists b ∈ B for which (a, b) ∈ R and (b, c) ∈ S}
- The relation R◦S is called the composition of Rand S; it is sometimes denoted simply by RS.

### Closure properties of relations

### Equivalence relations

A relation R on S is an equivalence relation if R is reflexive, symmetric, and transitive.

### Compatibility relations

### Partial order relations

A relation R on a set S is called a partial ordering or a partial order of S if R is reflexive, antisymmetric, and transitive.

## Function

Let A and B be two finite sets having m and n
elements respectively. Then total number of
functions from A to B is `n ^m`.

```
image is Range
pre-image is domain
```

### Types of functions

- ONE-TO-ONE (Injective) Function (`f (a) = f (a’) implies a = a’`)
- ONTO (Surjective) Function { A function `f: X → Y` is said to be an onto function if each element of Y is the image of some element of X }
- 1-1 AND ONTO ( Bijective) Function { A function which is both injective and bijective. }
- Invertible ( Inverse) Function
- Identity Function { A function f: A → A is identity relation if `f(a) = a` for all a belonging to A. }

```
For ONE-ONE we folow Horizontal Line Test.
For ONTO we folow Vertical Line Test.
```

### Composition of functions

Consider functions `f: A → B` and `g: B → C`; that is, where the codomain of f is the domain of g. Then we may define a new function from A to C, called the composition of f and g and written `g◦f`, as follows:

```
(g◦f)(a) ≡ g(f(a))
```

*here we use the functional notation `g◦f` for the composition of f and g instead of the notation `f◦g` which was used for relations.*

### Invertible function

- A function f: A → B is invertible if and only if f is both one-to-one and onto.
- In general, the inverse relation f^(−1) may not be a function.

### Hashing functions

- Hashing can be used to build, search, or delete from a table.
- The basic idea behind hashing is to take a field in a record, known as the key, and convert it through some fixed process to a numeric value, known as the hash key, which represents the position to either store or find an item in the table. The numeric value will be in the range of 0 to n-1, where n is the maximum number of slots (or buckets) in the table.
- The fixed process to convert a key to a hash key is known as a hash function. This function will be used whenever access to the table is needed.

#### What is meant by Good Hash Function?

A good hash function should have the following
properties:

1. Efficiently computable. (Easy and quick to complete).
1. Should uniformly distribute the keys (Each table position equally likely for each key.

#### 3 Methods of Hashing

1. Division (MOD) Method
1. Mid-square Method
1. Universal or Folding Method

*Division (MOD) Method*
![MOD](https://raw.githubusercontent.com/geekabhinav007/DiscreteBank/main/docs/img/dis4.png)

*Mid Square*<br>
In this method firstly key is squared and then
mid part of the result is taken as the index.
For example: consider that if we want to place a
record of 3101 and the size of table is 1000.
So `3101*3101=9616201`<br>
i.e. `h (3101) = 162 (middle 3 digit)`

*Folding Method*

- The folding method for constructing hash functions begins by dividing the item into equalsize pieces (the last piece may not be of equal size).
- These pieces are then added together to give the resulting hash value.
- For example, if our item was the phone number 436-555-4601, we would take the digits and divide them into groups of 2 (43,65,55,46,01). After the addition, `[43+65+55+46+01]`, we get `210`.
- If we assume our hash table has `11` slots, then we need to perform the extra step of dividing by `11` and keeping the remainder

### Recursively defined functions

- A function is said to be recursively defined if the function definition refers to itself.
- The function definition must have the following two properties:
    1. There must be certain arguments, called base values, for which the function does not refer to itself.
    1. Each time the function does refer to itself, the argument of the function must be closer to a base value

## PREPOSITIONAL AND PREDICATE LOGIC

### Propositional logic

#### Applications are

1) Translating English Sentences into logical statements
2) System Specifications
3) Logical Puzzles
4) Boolean Searches
5) Logic/Computer Circuits
6) Inference and Decision Making
7) Artificial Intelligence – Fuzzy Logic

*Operator Precedence*
![OP](https://www.geeksforgeeks.org/wp-content/ql-cache/quicklatex.com-9b1b328cc6588215aa7b424fc426cfc1_l3.png)

*TAUTOLOGIES* : Some propositions P(p, q, . . .) contain only T (True) in the last column of their truth tables or, in other words, they are true for any truth values of their variables

*CONTRADICTIONS* : if propositions P(p q, . . .) contains only F in the last column of its truth table or, in other words, if it is false for any truth values of its variables.

#### Important

- Implication / if-then (→) is also called a conditional statement. It has two parts −
  - Hypothesis, p
  - Conclusion, q
As mentioned earlier, it is denoted as `p → q`

```
“If you do your homework, you will not be
punished.”

Here, "you do your homework" is the hypothesis,p, and "you will not be punished" is the conclusion, q.
```

*Inverse* − An inverse of the conditional
statement is the negation of both the hypothesis and the conclusion.

- If the statement is “If p, then q”, the inverse will be “If not p, then not q”.
- Thus the inverse of `p → q` is `¬p → ¬q`.

```
Example − The inverse of “If you do your
homework, you will not be punished” is
“If you do not do your homework, you will be
punished.”
```

*Converse* − The converse of the conditional
statement is computed by interchanging the
hypothesis and the conclusion.

- If the statement is “If p, then q”, the converse will be “If q, then p”. The converse of p → q is q → p.

```
Example − The converse of "If you do your
homework, you will not be punished" is
"If you will not be punished, you do your
homework”.
```

*Contra-positive* − The contra-positive of the conditional is computed by interchanging the hypothesis and the conclusion of the inverse statement.

- If the statement is “If p, then q”, the contrapositive will be “If not q, then not p”.
- The contra-positive of p → q is ¬q → ¬p. (1 inverse ¬p →¬q. ; 2 converse : ¬q → ¬p)

```
Example − The Contra-positive of " If you do
your homework, you will not be punished” is
"If you are punished, you did not do your
homework”.
```

##### NOTES

```
The proposition ¬ q → ¬ p is called the
Contrapositive of the proposition p → q.

They are logically equivalent. p → q ≡ ¬ q → ¬ p
```

#### Trute table for implication and double implication

![tti](https://i.stack.imgur.com/R2aRo.png)
![ttdi](https://www.chilimath.com/wp-content/uploads/2020/03/truth-table-of-a-biconditional-919x1024.gif)

### Logical Eqivalence

- Two propositions P(p, q, . . .) and Q(p, q, . . .) are said to be logically equivalent, or simply equivalent or equal, denoted by `P(p, q, . . .) ≡ Q(p, q, . . .)`if they have identical truth tables.
- Example: ￢(p ∧ q) ≡ ￢ p ∨ ￢ q

### Normal forms (conjunctive and disjunctive)

### Validity of well-formed formula

### Algebra of Propositions

![aop](https://tutorialspoint.dev/image/quicklatex.com-67ea85d519042c10897afc964c777539_l3.png)

### Predicate logic

### Universal and existential quantifiers

## Combinatorial Mathematics

### Basic counting principles

### Permutations and combinations

### Pigeonhole principle

### Recurrence relations

### Solving homogeneous and non-homogeneous recurrence relations

### Generating function
