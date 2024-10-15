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
