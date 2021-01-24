# Data structures for tree traversal:
  
      Traversing a tree involves iterating over all nodes in some manner. 
      Because from a given node there is more than one possible next node (it is not a linear data structure), then, assuming sequential computation (not parallel), some nodes must be deferred—stored in some way for later visiting. 
      This is often done via a stack (LIFO) or queue (FIFO).
      As a tree is a self-referential (recursively defined) data structure, traversal can be defined by recursion or, more subtly, corecursion, in a very natural and clear fashion; 
      in these cases the deferred nodes are stored implicitly in the call stack.
      Depth-first search is easily implemented via a stack, including recursively (via the call stack), while breadth-first search is easily implemented via a queue, including corecursively.

Inorder Traversal (Practice):

        Algorithm Inorder(tree)
           1. Traverse the left subtree, i.e., call Inorder(left-subtree)
           2. Visit the root.
           3. Traverse the right subtree, i.e., call Inorder(right-subtree)

Preorder Traversal (Practice):

        Algorithm Preorder(tree)
           1. Visit the root.
           2. Traverse the left subtree, i.e., call Preorder(left-subtree)
           3. Traverse the right subtree, i.e., call Preorder(right-subtree) 
           
Postorder Traversal (Practice):      

        Algorithm Postorder(tree)
           1. Traverse the left subtree, i.e., call Postorder(left-subtree)
           2. Traverse the right subtree, i.e., call Postorder(right-subtree)
           3. Visit the root.

# Example:
        class Node: 
            def __init__(self,key): 
                self.left = None
                self.right = None
                self.val = key 


        # A function to do inorder tree traversal 
        def printInorder(root): 

            if root: 

                # First recur on left child 
                printInorder(root.left) 

                # then print the data of node 
                print(root.val), 

                # now recur on right child 
                printInorder(root.right) 



        # A function to do postorder tree traversal 
        def printPostorder(root): 

            if root: 

                # First recur on left child 
                printPostorder(root.left) 

                # the recur on right child 
                printPostorder(root.right) 

                # now print the data of node 
                print(root.val), 


        # A function to do preorder tree traversal 
        def printPreorder(root): 

            if root: 

                # First print the data of node 
                print(root.val), 

                # Then recur on left child 
                printPreorder(root.left) 

                # Finally recur on right child 
                printPreorder(root.right) 
# Output:

      Preorder traversal of binary tree is
      1 2 4 5 3 
      Inorder traversal of binary tree is
      4 2 5 1 3 
      Postorder traversal of binary tree is
      4 5 2 3 1

![Preorder-from-Inorder-and-Postorder-traversals](https://user-images.githubusercontent.com/52716203/82768933-e7524e00-9e29-11ea-85da-e02d2376f55d.jpg)
