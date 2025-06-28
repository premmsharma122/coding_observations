# How we can apply a loop on TreeNode/ListNode
<pre>  public void pushAll(TreeNode root) {
            for (; root != null; arr.push(root), root = root.left); }  </pre>

# How we can apply a sorting in hashMap to acces their key 
<prev>
            ArrayList<Integer> arr= new ArrayList<>(hm.keySet()); // here hm -> HashMap
            arr.sort((a,b)->hm.get(b) - hm.get(a)); // sorting based on value.<prev/>

