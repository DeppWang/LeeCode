个人 LeetCode 题解，用图片的形式展示解题思路。

## 目录

* [画解 LeetCode：1. 两数之和](docs/1.%20two-sum.md)：使用哈希表的 contains() 来比较其他元素是否符合条件。标签：`哈希表`
* [画解 LeetCode：7. 整数反转](docs/7.md)：依次除 10 取余，考虑溢出。标签：`数学`
* [画解 LeetCode：9. 回文数](docs/9.md)：依次比较最高位和最低位是否相等。标签：`数学`
* [画解 LeetCode：13. 罗马数字转整数](docs/13.md)：
  IV=4 等 6 种特殊情况总结为一种：左边数比右边数小。减去当前值。标签：`字符串`
* [画解 LeetCode：14. 最长公共前缀](docs/14.%20longest-common-prefix.md)：先将第一个字符串作为公共前缀。标签：`字符串`
* [画解 LeetCode：20. 有效的括号](docs/14.%20valid-parentheses.md)：将字符串的字符依次入栈，弹出直接闭合的字符，最后栈为空，则为有效字符。标签：`栈`
* [画解 LeetCode：21. 合并两个有序链表](docs/21.%20merge-two-sorted-lists.md)：较小的头结点作为结果头结点，next 节点从剩余节点中取最小。标签：`递归`
* [26. 删除排序数组中的重复项](docs/26.md)：一个指针从前往后遍历数组，一个指针记录不重复元素的数量（数组下标）。标签：双指针。

## 栈

双栈法（辅助栈）

- [155. 最小栈](docs/155.md)：使用两个栈，一个栈用于存放最小元素，一个栈存放正常元素。第一个元素为最小元素，如果后面比它小，入「小栈」，否则入「正常栈」
- [232. 用栈实现队列](docs/232.md)：使用两个栈，一个栈 s1 作为数据存储，一个栈 s2 作为临时缓冲。入队：元素压入栈 s1；出队：s1 倒入 s2，弹出 s2 顶部元素。优化：s2 不用倒回。

## 链表

假节点

- [2. 两数相加](docs/2.md)：使用一个假节点来链接链表。

假节点+双指针

- [19. 删除链表的倒数第 N 个节点](/docs/19.md)：快慢两个指针相隔 K 个节点，同时往后遍历，当快指针到达末节点，慢指针就是倒数第 K 个节点。
- [141. 环形链表]()：同一个圆中，快指针总会追上慢指针。

指针

* [画解 LeetCode：24. 两两交换链表中的节点](docs/24.%20swap-nodes-in-pairs.md)：25，k 固定为 2 
* [画解 LeetCode：25. K 个一组翻转链表](docs/25%reverse-nodes-in-k-group.md)：分为已翻转、待翻转、未翻转，利用「指针」，分离原链表

[237. 删除链表中的节点](docs/237.md)：将下一个节点赋给当前节点，删除下一个节点。

## 树

递归 or 栈

* [94. 二叉树的中序遍历](docs/94.md)：左根右，如果没有左子树，记录其值。
* [114. 二叉树的前序遍历](/docs/114.md)：根左右，先记录其值，再递归调用左右子树。

## 动态规划

> Dynamic programming，简称 DP。通过子问题解决父问题，即父问题答案可以通过子问题得到。

- [5. 最长回文子串](docs/5.md)：先将字符串反转，两者比较，利用动态规划得到最长公共子串。再排除字符串首尾是反向副本的情况（`aacdcaa`）
- [91. 解码方法](/docs/91.md)：从后往前遍历，当前子序列总和为上一个加上上一个

## Sliding Window

- [3. 无重复字符的最长子串](docs/3.md)：滑动找到所有不重复的子字符串，如果长度最长，记录为最长字符串。

LeetCode 题库地址：https://leetcode-cn.com/problemset/all/

> 深度优先遍历：递归（栈）实现
>
> 广度优先遍历：队列实现