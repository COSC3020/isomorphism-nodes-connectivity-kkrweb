# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.



//



Name: Kane Kriz

Start Date: 3 April 2025

Last Edited: 17 April 2025

Feedback Request 1 Date: 17 April 2025



//



Response: 

Per in-class definition: Isomorphic - Two graphs are isomorphic if they have the same structure (ignoring vertex names)


Beginning of Actual Proof Below:

Theorem: 

If two graphs $G_1=(V_1, E_1)$ and $G_2=(V_2, E_2)$ have $|V_1| = |V_2|$ and both are completely connected, then $G_1$ is isomorphic to $G_2$.


Proof:

Let $G_1=(V_1,E_1)$ and $G_2=(V_2,E_2)$ be complete graphs with $|V_1|=|V_2|=n$.


Because both graphs have the same number of vertices, we can pair their vertices in order. 

Let us label the vertices of $G_1$ as the sequence $v_1, v_2,$ continuing through to $v_n$, and similarly label the vertices of $G_2$ as $w_1, w_2,$ through to $w_n$.

Define the vertex mapping $f:V_1\rightarrow V_2$ by setting $f(v_k) = w_k$ for each integer $k$ starting from 1 up to and including $n$.


Proving $f$ is injective:

Suppose we have vertices $v_i$ and $v_j$ in $V_1$ where $f(v_i) = f(v_j)$.  

By our definition of $f$, this means $w_i = w_j$.  

All vertices $w_k$ in $G_2$ are distinct for $k$ from 1 to $n$. 

Since $w_i = w_j$, this can only occur if $i = j$.  

Therefore, it is evident that $v_i = v_j$.


Proving $f$ is surjective:

Take any vertex $w_k$ in $V_2$ where $1 \leq k \leq n$.  

By our labeling, $w_k$ is the $k$-th vertex of $G_2$.  

Our function definition gives $f(v_k) = w_k$ directly.  

This means every $w_k$ in $V_2$ is matched to some $v_k$ in $V_1$.  

Since we can find such a $v_k$ for every $w_k$, the function $f$ can be said to cover all vertices within $V_2$.  

Therefore $f$ is surjective.


Forward Edge Preservation:

Let $(v_i, v_j)$ be any edge in $E_1$.  

Since $G_1$ is establsihed as complete, $v_i \neq v_j$ must be true.  

From the injectivity of $f$,  $v_i \neq v_j$ implies $f(v_i) \neq f(v_j)$.  

As $G_2$ is complete, $(f(v_i), f(v_j)) \in E_2$ is also true.  

Thus $f$ is demonstrated to preserves edges in the forward direction.


Backward Edge Preservation:

Take any edge $(f(v_i), f(v_j)) \in E_2$.  

The completeness of $G_2$ gives $f(v_i) \neq f(v_j)$.  

Due to the injectivity of $f$, $f(v_i) \neq f(v_j)$ requires $v_i \neq v_j$.  

Per the above established completeness of $G_1$, $(v_i, v_j) \in E_1$ must exist.  

Therefore $f$ preserves edges in the reverse direction.


We have shown that $f$ is a bijection between $V_1$ and $V_2$ that preserves all edges in both directions.

Every edge in $G_1$ maps to an edge in $G_2$, and every edge in $G_2$ comes from an edge in $G_1$. 

Since $f$ is demonstrated to maintain vertex correspondence and edge relationships directly, $G_1$ and $G_2$ are isomorphic.

Q.E.D.



//



Plagiarism Acknowledgement: I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.


Citations:

“Isomorphisms and Subgraphs.” Tjyusun.com, 2025, tjyusun.com/mat202/sec-graph-isomorphisms.html. Accessed 17 Apr. 2025.

“11.4: Graph Isomorphisms.” Mathematics LibreTexts, 30 Mar. 2021, math.libretexts.org/Bookshelves/Combinatorics_and_Discrete_Mathematics/Combinatorics_(Morris)/03%3A_Graph_Theory/11%3A_Basics_of_Graph_Theory/11.04%3A_Graph_Isomorphisms.
