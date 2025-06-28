# How we can apply a loop on TreeNode/ListNode
<pre>  public void pushAll(TreeNode root) {
            for (; root != null; arr.push(root), root = root.left); }  </pre>

# How we can apply a sorting in hashMap to acces their key 
<prev>  ArrayList<Integer> arr= new ArrayList<>(hm.keySet()); // here hm -> HashMap
            arr.sort((a,b)->hm.get(b) - hm.get(a)); // sorting based on value. <prev/>
# Priority Queue Compare + Sorting Syntax 
<prev>   PriorityQueue<int[]> pq = new PriorityQueue<>(
            (a,b)->Integer.compare(b[0]*b[0] + b[1]*b[1], a[0]*a[0] + a[1]*a [1])); <prev/>
