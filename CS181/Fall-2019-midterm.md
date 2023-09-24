# Fall 2019 Midterm

Exam paper | [Solution](https://workdrive.zohopublic.com.cn/file/xse0ob18cbc315a4c4a4586328d4a0e28ac28)

## 1 Multiple choice

### Question 1

A. Quick answer: When all the edge costs are the same, BFS is equivalent to UCS, thus complete and optimal. Detailed: BFS is complete if the branching factor is finite, which is true since the graph has finite state space; BFS is optimal if step costs are all identical. (p.91, Section 3.4.7, AIMA 3rd. ver.)  
B. The space complexity of BFS is $O(b^d)$, while that of iterative deepening is $O(bd)$, where $b$ is the branching factor and $d$ is the depth of the shallowest solution. (p.91, Section 3.4.7, AIMA 3rd. ver.)  
C. See example in p.64, Slide 02, Fall 2022.  
D. Since this is a graph with finite state space, greedy algorithm can always find the goal state after visiting all the states, thus it is complete. However, it is not necessarily optimal.

### Question 2

Source: [Q3, (b), (i), Midterm 1, Fall 2013, Berkeley Exam](https://inst.eecs.berkeley.edu/~cs188/fa19/assets/exams/cs188-fa13-mt1-sol.pdf)

For tree-structured CSP, the order should be: Choose a root variable, order variables so that parents preceed children. (p.40, Slide 03, Fall 2022)

A. B is not a child of A.  
B. E is not a child of D.  
C. C is a child of B; D is a child of B/C; A is a child of B/C/D; E is a child of A/B/C/D; F is a child of A/B/C/D/E.  
D. D is not a child of B.

### Question 3

A. (p.250, Section 7.5, AIMA 3rd. ver.)  
B. We show $(A \land B) \land \neg A$ is unsatisfiable. We find $A$ and $\neg A$ resolve to yield the empty clause.  
C. A horn clause has the form $P_1 \land P_2 \land \dots \land P_n \Rightarrow Q$ or $\neg P_1 \lor \neg P_2 \lor \dots \lor \neg P_n \lor Q$ where Ps and Q are non-negated proposition symbols (atoms). Here, $C$ and $D$ violate the rule.  
D. In **propositional logic**, these two algorithms run in linear time (p.27, Slide 05, Fall 2022), thus linear space. The complexity of backward chaining can be much less than linear in size of KB (p.48, Slide 05, Fall 2022). Forward chaining is sound: every inference is essentially an application of Modus Ponens. Forward chaining is also complete: every entailed atomic sentence will be derived (p.258, Section 7.5.4, AIMA 3rd. ver.). So does backward chaining since Modus Ponens is sound and complete for Horn logic (p.27, Slide 05, Fall 2022). Inference is the process of deriving new sentences from old ones. Sound inference algorithms derive only sentences that are entailed; complete algorithms derive all sentences that are entailed (p.274, Section 7.8, AIMA 3rd. ver.).

### Question 4

A. This is true if someone is not at SIST. See example (p.18, Slide 06, Fall 2022).  
B. $y$ is not bounded. In a FOL sentence, every variable must be bound (p.20, Slide 06, Fall 2022).  
C. Consider when the domain is integers. That is, $x, y \in \mathbb{Z}$.  
D. Standardizing apart will eliminate overlap of variables, for example, replace $x$ with $z$ in $Marries(x, Bob)$ so that we have $Marries(z, Bob)$ (p.39, Slide 06, Fall 2022).

### Question 5

A. Consider A=True, B=False, C=False, LHS is False while RHS is True  
B. Consider A=True, B=False, C=False, LHS is True while RHS is False  
C. $(A \land B) \Rightarrow (A \land \neg A) \equiv (A \land B) \Rightarrow False \equiv \neg (A \land B) \equiv (\neg A \lor \neg B)$  
D. Notice that $(C \land X) \lor C \equiv C$, so we have $(\neg A \land \neg B) \lor (C \land \neg B) \lor (\neg A \land C) \lor C \equiv (\neg A \land \neg B) \lor C$

### Question 6

A. By definition, $P(X, Y|Z) = P(X | Z) P(Y | Z)$. Combine with product rule $P(X, Y|Z) = P(X|Y, Z)P(Y | Z)$ and we have the result. (p.28, Slide 07, Fall 2022)  
B. No information about the condition.  
C. Consider `A -> B <- C -> D`. Given `A`, `B` and `D` are dependent.  
D. See (p.50, Slide 07, Fall 2022).

