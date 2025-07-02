# There is a observation in 783. Minimum Distance Between BST Nodes.
###  Here **private Integer prev = null;** // that a need thing i learn in 
###  also is you want difference,  sorting somthing like that in tree questions so apply inorder traversal(asacding order arrangment) then it easy to operate them.

#  652. Find Duplicate Subtrees 
###  In this question's solution i find out a string based apporach which design a unique path for tree's left + right node,          then apply hashmap to count the particular path.
<pre> ```java String stringformed = currroot + "$" + left + "$" + right; ``` </pre>

#  1642. Furthest Building You Can Reach
##  In this question we have to limited componets to use so, we apply greedy + Priority Q.
###  👀 Observation 1: Not all climbs are equal
Some height differences are small (e.g., 1), some are large (e.g., 10).
Bricks are best used on small climbs

Ladders should be used on large climbs (since one ladder = infinite height jump)
###  👀 Observation 2: We don’t know climbs in advance
You only see each climb = heights[i+1] - heights[i] as you iterate.
So you track each climb and decide later which ones should use ladders or bricks.

###  In interval question Do a shorting based on first or second element (using in most of questions).
