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
1. `nth_element`(first,nth,last) if we just focus on if the kth elements in the sorted array, don't need to sort entire. <br>
This STL allows abtain the kth element satisfy the comparasion condition. And it's Time O(n) <br>
2. cmp in sort()<Br>
[1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)<br>
3. Priority_queue to sort in reel time(*****) && cmp in priority_queue<br>
In defaut, the bigger number is in front of the queue.<br>
Prefix sum [1508. Range Sum of Sorted Subarray Sums](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1508.%20Range%20Sum%20of%20Sorted%20Subarray%20Sums)<br>
Linked list [23. Merge k Sorted Lists](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/23.%20Merge%20k%20Sorted%20Lists)

## Array
1. Permutation of two parts of sub-arrray<br>
[1442. Count Triplets That Can Form Two Arrays of Equal XOR](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1442.%20Count%20Triplets%20That%20Can%20Form%20Two%20Arrays%20of%20Equal%20XOR)<br>
2. Contanation of two array : 
```cpp
vec1.insert(vec1.end(), vec2.begin(), vec2.end());
```
3. Permutation<br>
All of elements in a array, add un new elements in the previous resultats and keep it as a new possible result<br>
[78. Subsets](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/78.%20Subsets)
4. Conbination<br>
Number of Conbination => unordered_map as a count of element so that they can be pair<br>
[1512. Number of Good Pairs](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1512.%20Number%20of%20Good%20Pairs)<br>
a string pb[1513. Number of Substrings With Only 1s](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/String/1513.%20Number%20of%20Substrings%20With%20Only%201s)
## Bit wise
[Properties of XOR ](https://accu.org/index.php/journals/1915)
## Link list
A doublely Linked List<br>
[430. Flatten a Multilevel Doubly Linked List](https://github.com/AL2O3-Z/Leetcode/blob/master/Link%20List/430.%20Flatten%20a%20Multilevel%20Doubly%20Linked%20List)
### Tips
* modulo of a number(n or p): 
```cpp
int modulo = (sum % k + k )% k;
```
