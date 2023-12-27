# Day01
## 二分查找
方法一：二分查找
在升序数组 nums\textit{nums}nums 中寻找目标值 target\textit{target}target，对于特定下标 iii，比较 nums[i]\textit{nums}[i]nums[i] 和 target\textit{target}target 的大小：

如果 nums[i]=target\textit{nums}[i] = \textit{target}nums[i]=target，则下标 iii 即为要寻找的下标；

如果 nums[i]>target\textit{nums}[i] > \textit{target}nums[i]>target，则 target\textit{target}target 只可能在下标 iii 的左侧；

如果 nums[i]<target\textit{nums}[i] < \textit{target}nums[i]<target，则 target\textit{target}target 只可能在下标 iii 的右侧。

基于上述事实，可以在有序数组中使用二分查找寻找目标值。

二分查找的做法是，定义查找的范围 [left,right][\textit{left}, \textit{right}][left,right]，初始查找范围是整个数组。每次取查找范围的中点 mid\textit{mid}mid，比较 nums[mid]\textit{nums}[\textit{mid}]nums[mid] 和 target\textit{target}target 的大小，如果相等则 mid\textit{mid}mid 即为要寻找的下标，如果不相等则根据 nums[mid]\textit{nums}[\textit{mid}]nums[mid] 和 target\textit{target}target 的大小关系将查找范围缩小一半。

由于每次查找都会将查找范围缩小一半，因此二分查找的时间复杂度是 O(log⁡n)O(\log n)O(logn)，其中 nnn 是数组的长度。

二分查找的条件是查找范围不为空，即 left≤right\textit{left} \le \textit{right}left≤right。如果 target\textit{target}target 在数组中，二分查找可以保证找到 target\textit{target}target，返回 target\textit{target}target 在数组中的下标。如果 target\textit{target}target 不在数组中，则当 left>right\textit{left} > \textit{right}left>right 时结束查找，返回 −1-1−1。

作者：力扣官方题解
链接：https://leetcode.cn/problems/binary-search/solutions/980494/er-fen-cha-zhao-by-leetcode-solution-f0xw/
来源：力扣（LeetCode）
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
