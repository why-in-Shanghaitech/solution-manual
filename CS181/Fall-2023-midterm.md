# Fall 2023 Midterm

[Exam paper](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2023/Exam%20%E8%80%83%E8%AF%95/F23_CS181_Midterm.pdf) | [Solution](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2023/Exam%20%E8%80%83%E8%AF%95/F23_CS181_Midterm_solution.pdf)

## 1 Multiple choice

### Question 1

A. BFS takes $O(b^s)$ space. (p. 22, Slide 2, Fall 2023)  
B. It is correct.  
C. No, UCS requires that the edge weights are non-negative. Imagine that we have a graph with one edge of a large negative weight. If UCS does not explore this edge, then it will never find the optimal solution.  
D. Yes, it is correct. 3D maze is similar to a 2D maze.

### Question 2

A. Yes. Tree-Structured CSPs run time is $O(n d^2)$. (p. 41, Slide 3, Fall 2023)  
B. No. Remove backward takes place from leaf to root. (p. 42, Slide 3, Fall 2023) It is not possible to check AC before CF.  
C. No. It will be {red, orange, yellow}.  
D. Yes. A is possible to be assigned with green and F is possible to be assigned with red.

### Question 3

A. No. In zero-sum games, the agents have opposite utilities. (p. 39, Slide 4, Fall 2023)  
B. Yes. See p. 20, Slide 4, Fall 2023.  
C. Yes. See p. 39, Slide 4, Fall 2023.  
D. No. See p. 37, Slide 4, Fall 2023.

### Question 4

Perhaps the simplest check is as follows: pruning of children of a minimizer node m is possible (for some assignment to the terminal nodes), when both of the following conditions are met: (i) the value of another child of m has already been determined, (ii) somewhere on the path from m to the root node (include), there is a maximizer node M for which an alternative option has already been explored. The pruning will then happen if any such alternative option for the maximizer had a higher value than the value of the “another child” of m for which the value was already determined.

Here, only the last pruning strategy is possible. The first pruning operation on other strategies are all impossible.

### Question 5

A. No. We need to prove $KB \land \neg \alpha$ is unsatisfiable. (p. 23, Slide 5, Fall 2023)  
B. Yes. See p. 19, Slide 5, Fall 2023.  
C. No. Horn clause must have form of $P_1 \land P_2 \land \cdots \land P_n \Rightarrow Q$, or $\neg P_1 \lor \neg P_2 \lor \cdots \lor \neg P_n \lor Q$. (p. 26, Slide 5, Fall 2023)  
D. No. Consider $A = B = False, C = True$. Then $LHS = False$ and $RHS = True$.

### Question 6

A. Yes. See p. 49, Slide 6, Fall 2023.  
B. No. Backward chaining is goal-driven. (p. 48, Slide 5, Fall 2023)  
C. No. The two negatitions cancel each other.  
D. No. It only has one predicate, one sentence. Therefore, it is not a complex sentence.

### Question 7

A. No. It is $\forall x \exists y Loves(x, y)$.  
B. Yes. Modified from p. 15, Slide 6, Fall 2023.  
C. Yes. It is equivalent to $\forall x \forall y (Dog(y) \land Have(x, y) \Rightarrow \neg Lonely(x))$.  
D. No. At least it should be $\exists x \forall y Eat(x, y)$.

### Question 8

1. Joining over $B$. This will join all the factors with $B$, which are all the factors in this case. The result factor is $P(A, B, C)$.
2. Summing out $B$. This will sum out $B$ from the result factor. The result factor is $P(A, C)$.

### Question 9

This question goes beyond the scope of the course. It was created by mistake.

We say we "convert" a BN to a MN, it means that the MN can encode the same distribution as the BN. However, it is possible that the MN can encode more distributions than the BN. So the MN and BN will be likely to encode different sets of conditional independence.

In this question, the MN is fully connected, so it can encode any distributions. For BNs, only option D can do this.

To prove it, suppose A,B,C,D are binary variables. Consider the following joint distribution:

| A | B | C | D | P(A,B,C,D) |
|:-:|:-:|:-:|:-:|:-:|
|+a|+b|+c|+d| 0.1 |
|+a|-b|+c|+d| 0.2 |
|-a|+b|+c|+d| 0.3 |
|-a|-b|+c|+d| 0.4 |

and 0 for other assignments. We claim that the MN is able to encode this distribution. For example, we define the following potentials:

| A | B | C | D | $\phi$(A,B,C,D) |
|:-:|:-:|:-:|:-:|:-:|
|+a|+b|+c|+d| 0.1 |
|+a|-b|+c|+d| 0.2 |
|-a|+b|+c|+d| 0.3 |
|-a|-b|+c|+d| 0.4 |

and 0 for other assignments. However, option A cannot encode this distribution. Since $P(+a,+b)=0.1, P(+a)=0.3, P(+b)=0.4$, we find that $P(+a)P(+b)=0.12 \ne P(+a,+b)$. So variable A and B are dependent. However, in option A, variable A and B are independent if no other variables are observed. Similarly, we can prove that option B and C cannot encode this distribution.

### Question 10

A. Yes. A, C, D are fully connected, while there does not exist 4 nodes that are fully connected. See p. 86, Slide 7, Fall 2023.  
B. Yes. All paths are inactive. See p. 88, Slide 7, Fall 2023.  
C. Yes. $\phi(A, B, C, D) = \phi(A, C, D)\phi(B, C, D)$. Observe that $\sum_{a,b} \phi(a, b, C, D) = \sum_{a,b} \phi(a, C, D)\phi(b, C, D) = \sum_a \phi(a, C, D) \sum_b \phi(b, C, D) = 50 \times 50 = 2500$, we have $\sum_{a, b, c, d} \phi(a, b, c, d) = \sum_{c, d} \sum_{a, b} \phi(a, b, c, d) = 4 \times 2500 = 10000$. So $P(+a, +b, +c, +d) = \frac{\phi(+a, +b, +c, +d)}{\sum_{a, b, c, d} \phi(a, b, c, d)} = \frac{\phi(+a, +c, +d)\phi(+b, +c, +d)}{\sum_{a, b, c, d} \phi(a, b, c, d)} = \frac{10 \times 40}{10000} = 0.04$. See p. 87, Slide 7, Fall 2023.  
D. Yes. See p. 88, Slide 7, Fall 2023.
