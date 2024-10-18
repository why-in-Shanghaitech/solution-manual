# Fall 2022 Midterm

[Exam paper](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2022/Exam%20%E8%80%83%E8%AF%95/F22_CS181_Midterm.pdf) | [Solution](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2022/Exam%20%E8%80%83%E8%AF%95/F22_CS181_Midterm_solution.pdf)

## 1 Multiple choice

### Question 1

This question was adapted from [AIMA exercise 3.31](https://aimacode.github.io/aima-exercises/search-exercises/ex_31/).

A. No. Consider $w=1$, then the algorithm is a greedy algorithm with admissible heuristics, which is not optimal.  
B. Yes. It is equivalent to UCS.  
C. No. It is greedy search.  
D. Yes. It is obvious that the algorithm is equivlent if the multiply $f(n)$ with a constant $t > 0$. Then the algorithm becomes $f'(n) = tf(n) = t(1-w)g(n) + twh(n)$. Let $t = \frac{1}{1-w} \in (1, 2]$. Then $f'(n) = g(n) + \frac{w}{1-w}h(n)$. This is A* search with $h'(n) = \frac{w}{1-w}h(n)$. Since $0 \leq w \leq 0.5$, we have $0 \leq \frac{w}{1-w} \leq 1$. Thus, the algorithm is A* search with admissible heuristics.  
E. No. It is A* search.

### Question 2

Definition, see p. 32, Slide 3, Fall 2023.

### Question 3

A. Yes. Rational is one of the assumptions in minimax. (p. 39, Slide 4, Fall 2023)  
B. Yes. See p. 37, Slide 4, Fall 2023.  
C. No. It is similar to DFS and the time complexity is $O(b^m)$.  
D. Yes. See p. 22, Slide 4, Fall 2023.

### Question 4

A. Yes. Since $X_1 \leq a \leq X_3$.  
B. No. Consider $a = 1, b = c = d = 10$. It is possible that $X_1 = 1, X_2 = 10$.  
C. No. Consider $a = 1, b = c = d = 10$. It is possible that $X_2 = 1, X_3 = 10$.  
D. Yes. Consider $b = 10, a = c = d = 1$. It is possible that $X_2 = 10, X_3 = 1$.

### Question 5

A. No. $\neg S$ also can be satisfiable.  
B. No. Backward chaining is goal-driven. (p. 48, Slide 5, Fall 2023)  
C. Yes. Distributivity of $\land$ over $\lor$. (p. 14, Slide 5, Fall 2023)  
D. Yes. See p. 19, Slide 5, Fall 2023.

### Question 6

A. Yes. Since $B \lor (A \land B) \equiv B$.  
B. Yes. $LHS \equiv (\neg A \lor B) \lor (\neg B \lor A) \equiv True \equiv RHS$.  
C. No. Consider $A = B = False$, then $LHS = True$ and $RHS = False$.  
D. No. Consider $A = False, B = True$, then $LHS = True$ and $RHS = False$.

### Question 7

A. Yes. However, this is conflict with the slides (p. 23, Slide 6, Fall 2023), where there are two parents. Therefore, we decide to give the point to the students no matter whether they choose this option.  
B. Yes. Quantifier duality. (p. 19, Slide 6, Fall 2023)  
C. No. Consider 4 people, 1 makes friends with 2, 2 makes friends with 1, 3 makes friends with 4, 4 makes friends with 3. LHS is False while RHS is True.  
D. Yes, exactly.
