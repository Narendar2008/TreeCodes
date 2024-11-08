# **Tree Implementation**

```java
public class BinaryTreeNode<T> {

    public T data;
    public BinaryTreeNode<T> left;
    public BinaryTreeNode<T> right;

    public BinaryTreeNode(T data){
        this.data= data;
    }
}
```

```java
import java.util.*;
public class BinaryTreeUse {

    public static BinaryTreeNode<Integer> takeTreeInputBetter(boolean isRoot, int parentData, boolean isLeft) {
        if (isRoot) {
            System.out.println("Enter root data");
        } else {
            if (isLeft) {
                System.out.println("Enter left child of " + parentData);
            } else {
                System.out.println("Enter right child of " + parentData);
            }
        }

        Scanner s = new Scanner(System.in);
        int rootData = s.nextInt();

        if (rootData == -1) {
            return null;
        }

        BinaryTreeNode<Integer> root = new BinaryTreeNode<>(rootData);
        BinaryTreeNode<Integer> leftChild = takeTreeInputBetter(false, rootData, true);
        BinaryTreeNode<Integer> rightChild = takeTreeInputBetter(false, rootData, false);
        root.left = leftChild;
        root.right = rightChild;
        return root;
    }

    public static void printTreeDetailed(BinaryTreeNode<Integer> root) {
        if (root == null) {
            return;
        }
        System.out.print(root.data + ": ");
        if (root.left != null) {
            System.out.print("L" + root.left.data + ", ");
        }
        if (root.right != null) {
            System.out.print("R" + root.right.data);
        }
        System.out.println();
        printTreeDetailed(root.left);
        printTreeDetailed(root.right);
    }
   
    public static void main(String[] args) {
        BinaryTreeNode<Integer> root = takeTreeInputBetter(true, 0, true);
        printTreeDetailed(root);
    }
}

```


### Execution Methods
Files --> Save it as BinaryTreeNode.java
and  BinaryTreeUse.java
```
javac BinaryTreeNode.java
javac BinaryTreeUse.java
java BinaryTreeUse
```
## **Height of the Tree**
```java
 public static int height(BinaryTreeNode<Integer> root){
        if(root==null){
            return 0;
        }
        int leftoutput=height(root.left);
        int rightoutput=height(root.right);
        if(rightoutput>leftoutput){
            return rightoutput+1;

        }else{
            return leftoutput+1;
        }
    }
System.out.print("Height oF the tree: "+height(root));
```

## **Number of Nodes**
```java
 public static int numNodes(BinaryTreeNode<Integer> root){
        if(root==null) return 0;
        int leftNodeCount=numNodes(root.left);
        int rightNodeCount=numNodes(root.right);
        return 1+leftNodeCount+rightNodeCount;
    }
System.out.println("Number of Nodes in Tree: "+numNodes(root));

```

## **Linked list**

```java
class Solution {
  public boolean isPalindrome(ListNode head) {
    ListNode slow = head;
    ListNode fast = head;

    while (fast != null && fast.next != null) {
      slow = slow.next;
      fast = fast.next.next;
    }

    if (fast != null)
      slow = slow.next;
    slow = reverseList(slow);

    while (slow != null) {
      if (slow.val != head.val)
        return false;
      slow = slow.next;
      head = head.next;
    }

    return true;
  }

  private ListNode reverseList(ListNode head) {
    ListNode prev = null;
    while (head != null) {
      ListNode next = head.next;
      head.next = prev;
      prev = head;
      head = next;
    }
    return prev;
  }
}
```
