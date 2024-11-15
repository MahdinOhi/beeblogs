---
title: Tree Traversal
author: Mahdin Ohi
pubDatetime: 2024-11-14T09:00:00
slug: tree-traversal
featured: false
draft: false
tags:
  - DSA
description: Learn the fundamentals of tree traversal in this guide, covering pre-order, in-order, post-order. Includes clear pseudocode and C examples!
---

# Tree Traversal

Tree traversal refers to the process of **systematically visiting all the nodes** in a tree data structure in a specific order.

In this guide, we'll dive deep into tree traversal, exploring its types, implementations, and practical examples using pseudocode and C. Let's get started!

For Image Depictions: Kindly Visit

---

## What is Tree Traversal?

**Tree traversal** refers to the process of visiting (or examining) all the nodes of a tree in a specific order. Traversal is essential to perform operations such as searching, inserting, or modifying data in a tree.

Each tree node contains:

- **Data**: The value stored in the node.
- **Left Child**: Reference to the left subtree.
- **Right Child**: Reference to the right subtree.

### Types of Tree Traversals

There are **two main categories of tree traversal** techniques:

1. **Depth-First Traversal (DFT)**:
   - Pre-order Traversal
   - In-order Traversal
   - Post-order Traversal
2. **Breadth-First Traversal (BFT)**:
   - Level-order Traversal

Let's explore each type with examples.

---

## Depth-First Traversal (DFT)

Depth-First Traversal explores as far as possible along each branch before backtracking. We'll discuss its three main types:

### A. Pre-order Traversal (Root, Left, Right)

In **pre-order traversal**, nodes are visited in the following order:

1. Visit the root node.
2. Traverse the left subtree.
3. Traverse the right subtree.

**Use Case**: Pre-order traversal is useful for creating a copy of the tree.

#### Pseudocode: Pre-order Traversal

```
PreOrderTraversal(root):
    if root is not NULL:
        print root.data
        PreOrderTraversal(root.left)
        PreOrderTraversal(root.right)
```

#### C Code: Pre-order Traversal

```c
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* left;
    struct Node* right;
};

// Function to create a new node
struct Node* createNode(int data) {
    struct Node* node = (struct Node*)malloc(sizeof(struct Node));
    node->data = data;
    node->left = node->right = NULL;
    return node;
}

void preOrderTraversal(struct Node* root) {
    if (root != NULL) {
        printf("%d ", root->data);
        preOrderTraversal(root->left);
        preOrderTraversal(root->right);
    }
}

int main() {
    struct Node* root = createNode(1);
    root->left = createNode(2);
    root->right = createNode(3);
    root->left->left = createNode(4);
    root->left->right = createNode(5);

    printf("Pre-order Traversal: ");
    preOrderTraversal(root);
    return 0;
}
```

<img src="https://maxnilz.com/images/tree/Preorder-Traversal.png" alt="Description of Image" width="300" height="200">

---

### B. In-order Traversal (Left, Root, Right)

In **in-order traversal**, nodes are visited in the following sequence:

1. Traverse the left subtree.
2. Visit the root node.
3. Traverse the right subtree.

**Use Case**: In-order traversal is commonly used for binary search trees because it visits nodes in ascending order.

#### Pseudocode: In-order Traversal

```
InOrderTraversal(root):
    if root is not NULL:
        InOrderTraversal(root.left)
        print root.data
        InOrderTraversal(root.right)
```

#### C Code: In-order Traversal

```c
void inOrderTraversal(struct Node* root) {
    if (root != NULL) {
        inOrderTraversal(root->left);
        printf("%d ", root->data);
        inOrderTraversal(root->right);
    }
}

int main() {
    struct Node* root = createNode(1);
    root->left = createNode(2);
    root->right = createNode(3);
    root->left->left = createNode(4);
    root->left->right = createNode(5);

    printf("In-order Traversal: ");
    inOrderTraversal(root);
    return 0;
}
```

<img src="https://maxnilz.com/images/tree/Inorder-Traversal.png" alt="Description of Image" width="300" height="200">

---

### C. Post-order Traversal (Left, Right, Root)

In **post-order traversal**, nodes are visited in the following order:

1. Traverse the left subtree.
2. Traverse the right subtree.
3. Visit the root node.

**Use Case**: Useful for deleting or freeing nodes, such as in garbage collection.

#### Pseudocode: Post-order Traversal

```
PostOrderTraversal(root):
    if root is not NULL:
        PostOrderTraversal(root.left)
        PostOrderTraversal(root.right)
        print root.data
```

#### C Code: Post-order Traversal

```c
void postOrderTraversal(struct Node* root) {
    if (root != NULL) {
        postOrderTraversal(root->left);
        postOrderTraversal(root->right);
        printf("%d ", root->data);
    }
}

int main() {
    struct Node* root = createNode(1);
    root->left = createNode(2);
    root->right = createNode(3);
    root->left->left = createNode(4);
    root->left->right = createNode(5);

    printf("Post-order Traversal: ");
    postOrderTraversal(root);
    return 0;
}
```

<img src="https://maxnilz.com/images/tree/Postorder-Traversal.png" alt="Description of Image" width="300" height="200">

---

## Tree Traversal Complexity Analysis

| Traversal Type | Time Complexity | Space Complexity |
| -------------- | --------------- | ---------------- |
| Pre-order      | O(n)            | O(h)             |
| In-order       | O(n)            | O(h)             |
| Post-order     | O(n)            | O(h)             |
| Level-order    | O(n)            | O(n)             |

- **n**: Total number of nodes
- **h**: Height of the tree

---

### Key Takeaways:

- Depth-first traversals explore the depth of a tree before moving to the next sibling.
