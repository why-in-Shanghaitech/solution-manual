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

### Question 5

A. $\neg S$ also can be satisfiable.  
B. $\neg S$ is valid.  
C. Let $A=X_1 \lor X_2$, B=$\neg X_1 \lor X_3$, C=$X_2 \lor X_3$. Applying resolution to $A, B$ produces $C$. Consider $X_1 = False, X_2 = False, X_3 = True$, then $A = False, B = True, C = True$. $A \land B \not \equiv C$.  
D. From $A$ and $B$ we can infer $C$. Thus, $A \land B \Rightarrow C$. See p. 22, Slide 5, Fall 2023 for resolutions.

### Question 6

A. This is ambiguous. Based on the syntax on p. 258, Figure 8.3, AIMA 4th edition, the statement is correct. The sentence is syntactically correct, but semantically incorrect. See p. 20, Slide 6, Fall 2023.  
B. No. This sentence means "Every thing is a cat and it is cute."  
C. Yes. This is the rule of quantifier duality. (p.19, Slide 6, Fall 2023)

### Question 7

A. It is possible that the MGU does not exist. (p. 40, Slide 6, Fall 2023)  
B. This is ambiguous. Forward chaining is complete for definite clause knowledge bases. That is, it answers every query whose answers are entailed by any knowledge base of definite clauses. (p. 288, Section 7.8, AIMA 4th edition) However, this is not necessarily true for indefinite clause knowledge bases.  
C. Backward chaining can avoid repeated subgoals by caching previous results. (p. 57, Slide 6, Fall 2023)  
D. This is true. The former says that there exists a person that everyone loves him/her. The latter says that everyone loves a person. The former one is stronger than the latter one and can entail the latter one.

### Question 8

1. Joining over $C$. This will join all the factors with $C$, which are all the factors in this case. The result factor is $P(B, C, D|A)$.
2. Summing out $C$. This will sum out $C$ from the result factor. The result factor is $P(B, D|A)$.

### Question 9

A. No. Bayes Net is a directed acyclic graph. (p. 35, Slide 7, Fall 2023)  
B. Yes. Every variable is conditionally independent of its non-descendants given its parents. (p. 48, Slide 7, Fall 2023)  
C. Yes. Simple chain rule. (p. 31, Slide 7, Fall 2023)  
D. No. See p. 54, Slide 7, Fall 2023 as an example.

### Question 10

See p. 57, Slide 7, Fall 2023 for the active/inactive paths.

A. No. G-E-H is an active path.  
B. Yes. All paths are inactive.  
C. No. D-B-F-C is an active path.  
D. Yes. All paths are inactive.
