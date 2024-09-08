## Trees in Data Structures

A **tree** is a hierarchical data structure consisting of nodes connected by edges. It is used to represent hierarchical relationships and has various applications in computer science, such as in file systems, databases, and algorithms.

### Basic Representation

1. **Node**: The basic unit of a tree. Each node contains a value or data and may have zero or more child nodes.
2. **Root**: The top node of the tree, which has no parent.
3. **Edge**: The connection between two nodes. An edge connects a parent node to its child node.
4. **Leaf**: A node with no children.
5. **Subtree**: A tree formed by a node and all its descendants.

A tree can be represented using different data structures:

- **Node Class**:
  Each node can be represented as an object with attributes for its value and its children. For example, in Python:
  
  ```python
  class TreeNode:
      def __init__(self, value):
          self.value = value
          self.children = []
