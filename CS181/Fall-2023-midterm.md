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
