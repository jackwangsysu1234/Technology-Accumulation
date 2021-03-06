## 二叉树相关知识点

1. 遍历二叉树

   前序：递归即先加入根节点，再依次递归访问左孩子节点和右孩子节点；非递归即使用一个栈，先加入右孩子节点，再插入左孩子节点，从栈依次弹出栈顶元素。

   中序：递归先遍历左孩子节点，再加入当前节点，再遍历右孩子节点；非递归使用一个栈，循环访问左孩子节点，直至最下层的左孩子，然后判断其是否有右孩子，有的话继续循环其左孩子。

   后序：递归先遍历左孩子节点，再遍历右孩子节点，最后插入当前节点元素；非递归使用一个栈，因为后序是左右根的顺序输出，我们可以反向输出列表，即按照根右左的顺序插入到栈中。

   层序：使用一个队列，按照根左右顺序插入到队列中，然后从队列头弹出元素。如果需要记录每层的元素，可以在插入的队列时加入当前层级。

2. 统计二叉树节点数量

   可以使用深度优先遍历或者广度优先遍历的方法来统计所有节点数量；

   使用递归的方法，以root为根的节点数量等于以root.left为根节点数量和以root.right为根节点数量和加1。

3. 求二叉树的深度

   使用递归的方法（左右子树深度更大值加1）；

   使用层次遍历二叉树，求出最大深度。

4. 求二叉树第k层的节点个数

   使用层次遍历二叉树，并根据层数统计该层节点；

   使用递归法，以root为根的第k层节点数量等于root左孩子为根第k-1层和root右孩子为根第k-1层节点数量和。

5. 求二叉树叶子节点个数

   层次遍历二叉树，如果是叶节点则加1；

   使用递归法，等于左右子树叶节点数量和。

6. 判断两棵二叉树是否是相同的树

   判断根植是否相同，再递归判断其左子树和右子树是否都相同。

7. 判断一棵树是否是平衡二叉树

   判断其左右子树高度差是否超过1，若超过则不是平衡二叉树，递归其左右子树。

8. 翻转二叉树

   使用递归法自上而下递归翻转。

9. 求两个节点的最低公共祖先节点

   使用递归法，分别求出他们在左子树和右子树是否存在公共祖先，如果节点分别在左右子树中，则最小公共祖先就是root根节点。

10. 判断一棵树是否是二叉搜索树

    使用中序遍历二叉树，如果数组是增序就是二叉搜索树。

11. 路径和问题

    判断是否存在一条路径，使得数值和等于某个值。使用递归遍历二叉树。

    返回所有路径，使得路径和等于某个值。递归遍历二叉树，使用列表保存当前路径节点。

12. 
