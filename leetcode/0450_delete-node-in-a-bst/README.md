# 0450_delete-node-in-a-bst

分支都在代码里写明了, 删除节点时, 最麻烦的情况是被删节点同时有左右节点.
此时我们的目的, 是要找到被删除节点所在子树的`predecessor`(或者`successor`).

一个节点的`predecessor`(就是大小顺序紧挨着的小一点的数), 就是它的往左走一步后一直往右直到不能走下去为止的节点.

`predecessor`节点:

- 是叶子节点的话: 直接提上来.
- 不是叶子节点的话: 用`predecessor`的值覆盖被删节点, 然后在`predecessor`为根的子树里递归做删除操作.
