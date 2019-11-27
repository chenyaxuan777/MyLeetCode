# MyLeetCode

今日起开始记录我的LeetCode刷题之路

2019/11/14  
1.单链表反序 （迭代、递归  
2.单链表前n个反序  
3.单链表从n到m反序  
https://leetcode-cn.com/problems/reverse-linked-list-ii/solution/bu-bu-chai-jie-ru-he-di-gui-di-fan-zhuan-lian-biao/


```Python
class TreeNode:
    def __init__(self, x):
        self.val = x
        self.left = None
        self.right = None

class Solution:
    def preorderTraversal(self, root: TreeNode) -> [int]:
            stack, res = [root], []
            while len(stack) != 0:
                p = stack.pop(-1)
                res.append(p.val)
                if p.right != None:
                    stack.append(p.right)
                if p.left != None:
                    stack.append(p.left)
```
