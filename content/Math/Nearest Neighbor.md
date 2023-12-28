1 Dimension
brute force: $O(n)$
binary tree: $O(\log_2 n)$

d Dimension: real $d$ dimensional space $R^d$
the distance between any two points can be computed in $O(d)$ time
brute force: $O(dn)$
k-dimensional trees: between $O(\log_2 n)$ and $O(n)$

## KD Tree
**The k-d tree is a binary tree in which every node is a k-dimensional point.** Every non-leaf node can be thought of as implicitly generating a splitting hyperplane that divides the space into two parts, known as half-spaces. Points to the left of this hyperplane are represented by the left subtree of that node and points to the right of the hyperplane are represented by the right subtree. The hyperplane direction is chosen in the following way: every node in the tree is associated with one of the k dimensions, with the hyperplane perpendicular to that dimension's axis. So, for example, if for a particular split the "x" axis is chosen, all points in the subtree with a smaller "x" value than the node will appear in the left subtree and all points with a larger "x" value will be in the right subtree. In such a case, the hyperplane would be set by the x value of the point, and its normal would be the unit x-axis. (standard kd tree splitting rule)

default tree constrution algorithm: sliding midpoint rule
default search algorithm: 

The algorithm operates recursively.  When first encountering a node of the kd-tree the algorithm first visits the child that is closest to the query point. On return, if the box containing the other child lies within $1/(1 + \epsilon)$ times the distance to the closest point seen so far, then the other child is visited recursively.

Note from [Arya et al. 1998](https://www.cs.umd.edu/~mount/Papers/dist.pdf) 
$O(n)$ space and $O(\log n)$ query time are achievable in the expected case through the use of kd-trees (Friedman, Bentley and Finkel, 1977). The constant factors hidden in the asymptotic running time grow at least as fast as $2^d$ (depending on the metric). From the perspective of worst-case performance, an ideal solution would be to preprocess the points in $O(n \log n)$ time, into a data structure requiring $O(n)$ space so that queries can be answered in $O(\log n)$ time.

Main result from Arya et al. (1998) is stated in the following theorem
**Theorem 1.** Consider a set $S$ of $n$ data points in $R^d$. There is a constant $c_{d,\epsilon} \leq d(1+6d/\epsilon)^d$, such that in $O(dn\log n)$ time it is possible to construct a data structure of size $O(dn)$, such that for any Minkowski metric:
1.  Given any $\epsilon > 0$ and $q \in R^d$, a $(1 + \epsilon)$-approximate nearest neighbor of $q$ in $S$ can be reported in $O(c_{d,\epsilon}\log n)$ time
2. More generally, given $\epsilon > 0$, $q \in R^d$, and any $k$, $1\leq k \leq n$, a sequence of $k$ $(1+\epsilon)$-approximate nearest neighbors of $q$ in $S$ can be computed in $O((c_{d,\epsilon} + kd)\log n)$ time.