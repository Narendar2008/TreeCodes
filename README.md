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
### **Height of the Tree**
```java
public static int height(BinaryTreeNode<Integer> root) {
        if(root==null){
            return 0;
        }
        int smallLeftOutput = height(root.left);
        int smallRightoutput = height(root.right);
        if(smallRightoutput>smallLeftOutput){
            return smallRightoutput+1;
        }else{
            return smallLeftOutput+1;
        }

System.out.println("Height of the Tree:"+ height(root));

```

## **Traversal Methods**
```java
 public static void preOrder(BinaryTreeNode<Integer> root) {
        if (root == null) {
            return;
        }
        System.out.print(root.data + " ");
        preOrder(root.left);
        preOrder(root.right);
    }

    public static void inOrder(BinaryTreeNode<Integer> root) {
        if (root == null) {
            return;
        }
        inOrder(root.left);
        System.out.print(root.data + " ");
        inOrder(root.right);
    }

    public static void postOrder(BinaryTreeNode<Integer> root) {
        if (root == null) {
            return;
        }
        postOrder(root.left);
        postOrder(root.right);
        System.out.print(root.data + " ");
    }

System.out.println("Pre-order Traversal:");
        preOrder(root);
        System.out.println();

        System.out.println("In-order Traversal:");
        inOrder(root);
        System.out.println();

        System.out.println("Post-order Traversal:");
        postOrder(root);
        System.out.println();
```
