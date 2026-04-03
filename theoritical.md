# There is a observation in 783. Minimum Distance Between BST Nodes.
###  Here **private Integer prev = null;** // that a need thing i learn in 
###  also is you want difference,  sorting somthing like that in tree questions so apply inorder traversal(asacding order arrangment) then it easy to operate them.

#  652. Find Duplicate Subtrees 
###  In this question's solution i find out a string based apporach which design a unique path for tree's left + right node,          then apply hashmap to count the particular path.
```java
String stringformed = currroot + "$" + left + "$" + right; 
```

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
###  Expression	Behavior
```java
Double.compare(a, b)	ascending (default) — min heap
Double.compare(b, a)	descending — max heap ✅
```
###  Arrays.sort(pairs, (a, b) -> Double.compare(a[0], b[0]));
```java
pairs is the 2D array you're sorting
(a, b) is a lambda expression that compares two rows
a[0] and b[0] are the first elements of each row (ratios)
Double.compare(a[0], b[0]) compares two doubles safely
```
###  Always sort the array first if you’re dealing with distance or position based problems.
Keep track of:
Binary search conditions
Feasibility function correctness.
###  Time Complexity Realted MarkDowns ->
When solving a problem📑 Look at the input size  & Use the rule of thumb:
Max n                |             Best Time Complexity You Should Aim For
≤ 10	                              Try anything (even brute force)
≤ 100	                              O(n³) or O(2ⁿ) works
≤ 1000	                            O(n²) is OK
≤ 10⁵	                              Try O(n log n) or O(n)
≤ 10⁶	                              Only O(n) will work

##  About Eularian Circuit Questions (Graph) -
###  if any grpah has two odd degree of vertices nd rest are even then it will be Eular path.
###  if any grpah has all even degree of vertices then it will be Eular circuit
###  If the graph has no edges, it’s trivially considered connected for the purpose of Eulerian path/circuit check.
###  Steps to check Eualr circuit or path -> 1. check all compontents are connected or not if not then return 0;
###                                          2. then check for odd degree of every vertices if odd count is 2 then return 1 (eular path) if count is zero then return 2 (eular ciruit). GFG Q. -> https://www.geeksforgeeks.org/problems/euler-circuit-and-path/1

#  🔑 Rule of Thumb 
###  Whenever you split on a character that has a special meaning in regex (., *, +, ?, |, ^, $, (, ), [, ], {, }, \\), you must escape it like this:
-   \\. for .
-  \\* for *
-  \\+ for +
-  etc.

#  Pick the medians
```java
-  After sorting, the two middle elements (arr[n-1] and arr[n]) are the closest possible medians you can get for any split into odd-sized classes.
-  So the minimum absolute difference between class medians = arr[n] - arr[n-1]. 
```
#  TreeMap Function IMP..
```java
✅ lowerEntry(x)
👉 Meaning:
x se strictly chhota sabse bada key

(= equal allow nahi karta)
  --
✅ floorEntry(x)
👉 Meaning:
x se chhota ya barabar sabse bada key
Difference in one table
Function	Equal allowed?	Example
floorEntry(x)	✅ YES	≤ x
lowerEntry(x)	❌ NO	< x
```
##  SubArray Problem Observation: 
```java
absolute difference between any two elements ≤ limit

Ye line sabse important hai.

“any two elements” ka matlab kya?

❌ sirf adjacent nahi
❌ sirf first–last nahi

✅ pure subarray ka max aur min matter karta hai

Kyuki:

max difference = max − min
```
###  Sliding Window Kab Use Hoga ?
```java
sliding window idea aata hai

Subarray continuous hai ❗

👉 whenever you see:

subarray / longest / continuous


💡 sliding window automatically dimag me aani chahiye.
```
## CP
```sql
The Problem: Arrays.sort()In Java, Arrays.sort(long[]) uses a Dual-Pivot Quicksort. While usually fast, it has a worst-case time complexity of $O(N^2)$ on specifically crafted inputs (like those in Test #7). Since $N = 200,000$, $N^2$ is $4 \cdot 10^{10}$, which causes the TLE.The Fix: Shuffle or Use a Different SortTo fix this, you have two main options:Shuffle the array before sorting to break the anti-quicksort pattern.Use Arrays.sort(Long[]) (the boxed version) which uses TimSort, guaranteed to be $O(N \log N)$.Use Collections.sort() on an ArrayList, which also uses TimSort.
```
