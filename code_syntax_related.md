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
### Simplest syntax to loop over keys in HashMap
```java
for(int n : hm.keySet()){
            if(hm.get(n) > k){
                ans.add(n);
            }
}
```
## How to optimize a nested loop like find sum of pairs == target , Here a simple hashMap based approach 
###  we have given 2 int[] arr, so we create a hashmap add all values for arr2 in hashmap , and then iterate a for each loop on arr1 like that->
```java
 HashMap<Integer, Integer> hm = new HashMap<>();
        for (int n : arr2){
         hm.put(n,hm.getOrDefault(n,0)+1);
        }
        for(int a : arr1){
         int comple = tot - a; // complement to optimize nested loop.
         c+= hm.getOrDefault(comple,0);
        }
       return c;
```
