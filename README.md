# Leetcode
[文字格式](https://blog.csdn.net/u012067966/article/details/50736647)
## *Subsequence Sum :
When all elements are positive and negative, we can use prefix sum + hashmap and this is more general.<br>
Otherwise, we can use sliding window and verify if the condition is satisfied.<br>
`Solution 1: prefix sum + hashmap`<br>
[LC974](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Unordered_map/974.%20Subarray%20Sums%20Divisible%20by%20K)<br>
`Solution 2: sliding window`<br>
[LC1477](https://github.com/AL2O3-Z/Leetcode/blob/master/Slide%20Window/1477.%20Find%20Two%20Non-overlapping%20Sub-arrays%20Each%20With%20Target%20Sum)
## *Frequent pb :
`hashmap` to store the pair of element and its frequence. <br>
If needed, use `priority_queue` or `bucket sorting` to sort the frequence.<br>
[692. Top K Frequent Words](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Queue/692.%20Top%20K%20Frequent%20Words)<br>
[347. Top K Frequent Elements](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/347.%20Top%20K%20Frequent%20Elements)<br>
[1481. Least Number of Unique Integers after K Removals](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1481.%20Least%20Number%20of%20Unique%20Integers%20after%20K%20Removals)<br>
## DFS in matrix
Just pay attention to the edge of the matrix and the condition of termination of current recursion<br>
What is more interesting is if we must do the backtrack or not : The same cell may or may not be used more than once.<br>
[463. Island Perimeter](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/463.%20Island%20Perimeter)<br>
[130. Surrounded Regions](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/130.%20Surrounded%20Regions)<br>
[79. Word Search(with backtrack)](https://leetcode.com/problems/word-search/)
## Sort
1. nth_element(first,nth,last) if we just focus on if the kth elements in the sorted array, don't need to sort entire. <br>
This STL allows abtain the kth element satisfy the comparasion condition. And it's Time O(n) <br>
2. cmp in sort()<Br>
[1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)
### Tips
* modulo of a number(n or p): 
```cpp
int modulo = (sum % k + k )% k;
```
