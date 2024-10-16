# Fall 2021 Midterm

[Exam paper](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2021/Exam%20%E8%80%83%E8%AF%95/F21_CS181_Midterm.pdf) | [Solution](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2021/Exam%20%E8%80%83%E8%AF%95/F21_CS181_Midterm_solution.pdf)

## 1 Multiple choice

### Question 1

A. Yes. See p. 15, Slide 2, Fall 2023.  
B. It is ambiguous. It depends on the goal: if we want to find the shortest path, then BFS is optimal; if we want to find the path with the smallest total edge weight, then BFS is not optimal. By default, we consider the goal to be finding the shortest path. (p. 15, Slide 2, Fall 2023)  
C. Yes. See p. 22, Slide 2, Fall 2023.  
D. No. The heuristic function needs to be admissible and consistent. (p. 62, Slide 2, Fall 2023)

### Question 2

A heuristic function $h$ is admissible if $0 \leq h(n) \leq h^*(n)$, where $h^*(n)$ is the true cost to a nearest goal. (p. 42, Slide 2, Fall 2023)

A. No. It is possible that $h_1(n)+h_2(n)\gt h^*(n)$.  
B. Yes. It is guaranteed that $0 \leq max(h_1(n), h_2(n)) \leq h^*(n)$.  
C. Yes. It is guaranteed that $0 \leq min(h_1(n), h_2(n)) \leq h^*(n)$.  
D. Yes. It is guaranteed that $0 \leq \alpha h_1(n) + (1-\alpha) h_2(n) \leq h^*(n)$.

### Question 3

A. Yes. See p. 153, 5.2.4, AIMA 4th edition.  
B. Yes. See p. 174, Chapter 5 Summary, AIMA 4th edition.  
C. Yes. See p. 150, 5.2.1, AIMA 4th edition.  
D. Yes. See p. 48, Slide 4, Fall 2023.

### Question 4

Perhaps the simplest check is as follows: pruning of children of a minimizer node m is possible (for some assignment to the terminal nodes), when both of the following conditions are met: (i) the value of another child of m has already been determined, (ii) somewhere on the path from m to the root node (include), there is a maximizer node M for which an alternative option has already been explored. The pruning will then happen if any such alternative option for the maximizer had a higher value than the value of the “another child” of m for which the value was already determined.
