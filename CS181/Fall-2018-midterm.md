# Fall 2018 Midterm

[Exam paper](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2018/Exam%20%E8%80%83%E8%AF%95/Fall%202018%20Midterm%20Exam.pdf) | [Solution](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2018/Exam%20%E8%80%83%E8%AF%95/midtermf18_sol(1).pdf)

## 1 Multiple choice

### Question 1

A. Minimax search (w/o pruning) is nothing more than a DFS. Thus, the space complexity should be $O(bm)$ instead of $O(b^m)$.  
B. Of course it depends on the expanding order. A good (lucky) order may prune most of the nodes, which may boost the performance.  
C. This is true because the leftmost nodes and their children could never be pruned. These nodes have no prior information.  
D. Similar to C, the root node and its children will never be pruned, since the root node has no prior information ($\alpha=-\infty$, $\beta=+\infty$)

### Question 2

A. Consider A=True, B=False, LHS is True while RHS is False  
B. Consider A=True, B=False, LHS is True while RHS is False  
C. The distributive law  
D. Consider A=False, B=False, LHS is False while RHS is True

### Question 3

A. You can never substitute Jane with x. The substitution replaces a variable with a term (a piece of syntax) to produce a new sentence. (p.323, Section 9.1, AIMA 3rd. ver.)  
B. That's right.  
C. Consider A=False, E=False, D=True, LHS is False while RHS is True.  
D. x is not bounded here. In a FOL sentence, every variable must be bound. (p.20, Slide 06, Fall 2022)

### Question 4

A. All paths are blocked.  
B. A - D - E is active.  
C. A - D - B - E is active.  
D. A - C - G is active.  
E. C - F - D is active. (Since H is observed)

### Question 5

A. No. They only encode the same distribution, not the same set of conditional independence. (p.97, Slide 07, Fall 2022)  
B. Markov network is undirected.  
C. It is possible to have cycles. See slides for an example. (p.98, Slide 07, Fall 2022)  
D. Constraint graphs can be seen as Markov networks with 0/1 potentials (p.100, Slide 07, Fall 2022)

### Question 6

A. DFS for tree search is incomplete, for example, it may expand the wrong branch all the time (p.86, Section 3.4.3, AIMA 3rd. ver.). An algorithm is complete if it is guaranteed to find a solution when there is one (p.80, Section 3.3.2, AIMA 3rd. ver.).  
B. Iterative deepening is complete. Since it explores a complete layer of new nodes at each iteration before going on to the next layer, which is analogous to breadth-first search (p.90, Section 3.4.5, AIMA 3rd. ver.).  
C. UCS is complete and optimal (if you want to find the path with minimal cost, which is our goal for search problems by default).  
D. A* is complete and optimal with consistent heuristics.

### Question 7

A. That is true. An inference algorithm that derives only entailed sentences is called sound or truth-preserving. (p.242, Section 7.3, AIMA 3rd. ver.).  
B. Yes. More specifically, $\neg S$ is valid. A sentence is satisfiable if it is true in, or satisfied by, some model. (p.250, Section 7.5, AIMA 3rd. ver.) A sentence is valid if it is true in all models. (p.249, Section 7.5, AIMA 3rd. ver.)  
C. Forward chaining is sound and complete. It is sound, because every inference is just an application of Generalized Modus Ponens, which is sound. It is complete for definite clause knowledge bases; that is, it answers every query whose answers are entailed by any knowledge base of definite clauses (p.331, Section 9.3.2, AIMA 3rd. ver.). Backward chaining (unlike forward chaining) suffers from problems with repeated states and incompleteness. (p.337, Section 9.4.1, AIMA 3rd. ver.) See example in textbook Figure 9.10 (p.343, Section 9.4.4, AIMA 3rd. ver.).  
D. Yes. Horn clause has the form $P_1 \land P_2 \land \dots \land P_n \Rightarrow Q$ or alternatively $\neg P_1 \lor \neg P_2 \lor \dots \lor \neg P_n \lor Q$ (p.26, Slide 05, Fall 2022).

### Question 8

A. There are 3 samples with +a among the 5 samples. $P(+a) = 3/5 = 0.6$  
B. There are 3 samples with +c, where b is always +b.  
C. There are 3 samples with +d, +e. $P(-c | +d, +e) = \frac{0.2 + 0.2}{0.2 + 0.2 + 0.1} = 0.8$  
D. $P(-d | +e) = \frac{0.12 + 0.12}{0.12 + 0.2 + 0.2 + 0.12 + 0.1} \approx 0.324$

### Question 9

A. The size of the largest factor determines the time and space complexity of VE (p.29, Slide 08, Fall 2022).  
B. The elimination ordering can greatly affect the size of the largest factor (p.29, Slide 08, Fall 2022).  
C. There does not always exist an ordering that only results in small factors (p.29, Slide 08, Fall 2022). The problem is still NP-hard (p.20, Slide 08, Fall 2022).  
D. Absolute nonsense.  
E. For poly-tree BNs, the complexity of VE is linear in the BN size (p.33, Slide 08, Fall 2022).

### Question 10

A. Bayesian networks express all the conditional independence relationships in a domain (p.34, Slide 07, Fall 2022).  
B. Bayes net has size $O(nd^{k+1})$, where $n$ is the number of variables and $d$ is the maximum domain size (p.44, Slide 07, Fall 2022).  
C. BN is a directed, acyclic graph (DAG) (p.40, Slide 07, Fall 2022).  
D. See choice B.  
E. A variable's Markov blanket consists of parents, children, and children's other parents (p.50, Slide 07, Fall 2022).


## 2 Search

### 2.1.1

DFS may return any path to the goal; BFS may only return the path with the minimum number of edges (in this problem, 2); UCS and A* may only return the path with the minimum cost.

### 2.1.2 (1)

A-C-D-F-G is not an optimal path. Let's run the A* algorithm to see what is happening. We first expand node $A$. Then we have
   - $B$: $2+h(B)$
   - $C$: $5+h(C)=10$

in the priority queue. Then we claim that the algorithm must expand C before B, since otherwise it will find that A-B-C is shorter than A-C. This requires $2+h(B) \geq 10$, which leads to the solution $h(B) \geq 8$.

### 2.1.2 (2)

If $h$ is consistent, then
- for admissibility, $h(B) \leq 7$
- for consistency, consider A-B. we have $h(A) - h(B) \leq 2$, i.e. $h(B) \geq 6$
- for consistency, consider B-C. we have $h(B) - h(C) \leq 1$, i.e. $h(B) \leq 6$

Thus $h(B) = 6$.

### 2.2

Source: [Q7, (d), Midterm, Spring 2011, Berkeley Exam](https://inst.eecs.berkeley.edu/~cs188/fa19/assets/exams/cs188-sp11-mt1-sol.pdf)

1. If $H_1$ is 0 for all states, then $(H_1 + H_2) / 2$ is easy to be inconsistent.
2. Similarly, consider $H_1$ is 0 for all states.
3. Take $h$ in the previous problem as an example. Let $H_1$ be $h$, $H_2$ be zero for all states except a very large $A$.


## 3 CSP

### 3.3

An arc $A \rightarrow B$ is inconsistent after enforcing constraint (2), there is only one possibility: $B$ has only one single value in its domain, and the domain of $A$ contains this value.

From 3.2 we know that only $X_3$ and $X_5$ have one value $c_2$ in its domain. From 3.1, we know the possible arcs:
$X_1 \rightarrow X_3$,
$X_6 \rightarrow X_3$,
$X_1 \rightarrow X_5$.

And the domain of $X_1$ and $X_6$ contains $c_2$. So these 3 arcs are not consistent.

### 3.4

Starting from 3.3, let's delete from the tail:

| Variable | Domain          |
| -------- | --------------- |
| $X_1$    | $c_1$           |
| $X_2$    | $c_1, c_2, c_3$ |
| $X_3$    | $c_2$           |
| $X_4$    | $c_1, c_3$      |
| $X_5$    | $c_2$           |
| $X_6$    | $c_1, c_3$      |

Then, consider $X_i \rightarrow X_1$, where $i=2,4,6$. We have

| Variable | Domain     |
| -------- | ---------- |
| $X_1$    | $c_1$      |
| $X_2$    | $c_2, c_3$ |
| $X_3$    | $c_2$      |
| $X_4$    | $c_3$      |
| $X_5$    | $c_2$      |
| $X_6$    | $c_3$      |

Finally, consider $X_2 \rightarrow X_6$, the domain of $X_2$ only has $c_2$. 

| Variable | Domain |
| -------- | ------ |
| $X_1$    | $c_1$  |
| $X_2$    | $c_2$  |
| $X_3$    | $c_2$  |
| $X_4$    | $c_3$  |
| $X_5$    | $c_2$  |
| $X_6$    | $c_3$  |

Check the constraints, we find that they are all satisfied.


## 4 Logic

The solution is illustrative enough.

## 5 Winner, winner, chicken dinner

The solution is illustrative enough.
