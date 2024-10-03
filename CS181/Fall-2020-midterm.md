# Fall 2020 Midterm

[Exam paper](https://workdrive.zohopublic.com.cn/file/gkbi5fad4380a813d48f99d9df5cde2d197d0) | [Solution](https://workdrive.zohopublic.com.cn/file/gkbi5bf5616489c8f4b8dbada61144848a392)

## 1 Multiple choice

### Question 1

This question assumes that we are solving a shortest path problem.

A. DFS could return a path with any possible lengths.  
B. BFS will return a path with the smallest number of nodes.  
C. UCS will return a path with the smallest total edge weight.  
D. Greedy search could behave like a badly-guided DFS in the worst case.

### Question 2

A. BFS would take space complexity $O(b^d)$. (p.22, Slide 2, Fall 2023)  
B. If a solution exists, then the depth will be finite. So iterative deepening is guaranteed to find the solution, thus complete. The completeness of iterative deepening is equivalent to that of BFS. (p.22, Slide 2, Fall 2023)  
C. See p. 27, Slide 2, Fall 2023.  
D. In tree search, A* is optimal if the heuristic is admissible. (p. 43-47, Slide 2, Fall 2023)

### Question 3

This question assumes that we are running backtracking search with forward checking. Notice that this assumption is not necessarily true, so the question is not well-defined.

A. We cannot determine the correctness of the statement. This is because we do not know the color assignments of the variables. If the assignment strategy is LCV, then the statement is correct.  
B. After assigning R to A, we have B: {G, B}, C: {G, B}, D: {R, G, B}, E: {R, G, B}. Then we assign G to B, and we have C: {G, B}, D: {R, B}, E: {R, B}. Then we assign G to C, and we have D: {R, B}, E: {R, B}. Then we assign B to D, and we have E: {R}. Then we assign R to E. The assignment follows LCV.  
C. After assigning R to A, we have B: {G, B}, C: {G, B}, D: {R, G, B}, E: {R, G, B}. Then we assign G to B, and we have C: {G, B}, D: {R, B}, E: {R, B}. Then we assign B to C, and we have D: {R, B}, E: {R}. However, if we assign G to C, E will have 2 options. Thus, the assignment does not follow LCV.  
D. Similar to B, the assignment follows LCV. The key is to assign the same color to B and C.

### Question 4

This question assumes that we are visiting the nodes from left to right.

A formal method is to calculate the alpha-beta values for each node. Here, we provide an intuitive explanation.

A. G will not be pruned. After visiting M, we know $A \leq B = 50$, $C \geq F = 49$. If $G = 51$, then $A = 50$; if $G = 49$, then $A = 49$. Thus, G will not be pruned.  
B. K will be pruned. After visiting J, we've already known that $E \leq 1$, while $B \geq D = 50$. No matter what the value of K is, we know that $B = 50$. Thus, K will be pruned.  
C. Since G will not be pruned, N will not be pruned.  
D. O will be pruned. After visiting N, we know that $G \leq 0$, while $C \geq 49$. No matter what the value of O is, we know that $C = 49$. Thus, O will be pruned.
