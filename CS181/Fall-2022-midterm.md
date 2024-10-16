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

A. Yes. Rational is one of the assumptions in minimax. (p. 39, Slide 5, Fall 2023)  
B. Yes. See p. 37, Slide 5, Fall 2023.  
C. No. It is similar to DFS and the time complexity is $O(b^m)$.  
D. Yes. See p. 22, Slide 5, Fall 2023.

### Question 4

A. Yes. Since $X_1 \leq a \leq X_3$.  
B. No. Consider $a = 1, b = c = d = 10$. It is possible that $X_1 = 1, X_2 = 10$.  
C. No. Consider $a = 1, b = c = d = 10$. It is possible that $X_2 = 1, X_3 = 10$.  
D. Yes. Consider $b = 10, a = c = d = 1$. It is possible that $X_2 = 10, X_3 = 1$.
