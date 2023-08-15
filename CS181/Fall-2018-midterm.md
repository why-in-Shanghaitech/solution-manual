# Fall 2018 Midterm

[Exam paper](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2018/Exam%20%E8%80%83%E8%AF%95/Fall%202018%20Midterm%20Exam.pdf) | [Solution](https://nbviewer.org/github/i-TechX/iTechX/blob/file-base/courses/CS181/CS181.01_Fall_2018/Exam%20%E8%80%83%E8%AF%95/midtermf18_sol(1).pdf)

## 1 Multiple choice

### Question 1

A. Minimax search (w/o pruning) is nothing more than a DFS. Thus, the space complexity should be $O(bm)$ instead of $O(b^m)$.  
B. Of course it depends on the expanding order. A good (lucky) order may prune most of the nodes, which may boost the performance.  
C. This is true because the leftmost nodes and their children could never be pruned. These nodes have no prior information.  
D. Similar to C, the root node and its children will never be pruned, since the root node has no prior information ($\alpha=-\infty$, $\beta=+\infty$)

### Question 2

