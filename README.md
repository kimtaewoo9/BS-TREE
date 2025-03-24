# BS-TREE

### Binary Search Tree (BST) Implementation
This project implements a Binary Search Tree (BST) in C++. The BST maintains height and size information for each node, allowing for efficient operations and potential future enhancements like balancing.

#### Features
- Insert nodes into the BST

- Delete nodes from the BST

- Inorder traversal for displaying the tree structure

- Memory management to prevent leaks

#### Key Components
```
Node Structure
cpp
typedef struct _TREENODE_{
    element key;
    struct _TREENODE_* left;
    struct _TREENODE_* right;
    int height;
    int size;
} TREENODE;
```

#### Main Operations

`insertBST`: Inserts a new key into the BST

`deleteBST`: Removes a key from the BST

`inorderTraverse`: Displays the BST structure

#### Usage

The program accepts two types of commands:

`i key`: Insert key into the BST

`d key`: Delete key from the BST

After each operation, the tree structure is displayed using inorder traversal.

#### Implementation Details
- Uses a stack to keep track of parent nodes during insertion and deletion

- Maintains height and size information for each node

- Implements both single-child and two-child deletion cases

- Chooses successor based on subtree height and size in two-child deletion

#### Memory Management
The clearTree function performs a post-order traversal to properly deallocate all nodes, preventing memory leaks.

#### Compilation and Execution
Compile the program using a C++ compiler. For example:

text
```
g++ -std=c++11 bst.cpp -o bst
Run the compiled program:
```

text
```
./bst
```
