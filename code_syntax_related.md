### How we can apply a loop on TreeNode/ListNode

```java
public void pushAll(TreeNode root) {
    for (; root != null; arr.push(root), root = root.left);
}
```
### How we can apply sorting in a HashMap to access their keys

```java
ArrayList<Integer> arr = new ArrayList<>(hm.keySet()); // hm is a HashMap
arr.sort((a, b) -> hm.get(b) - hm.get(a)); // sort keys based on value (descending)
```
### Priority Queue Compare + Sorting Syntax

```java
PriorityQueue<int[]> pq = new PriorityQueue<>(
    (a, b) -> Integer.compare(
        b[0]*b[0] + b[1]*b[1],
        a[0]*a[0] + a[1]*a[1]
    )
);
```
