# Leetcode
[文字格式](https://blog.csdn.net/u012067966/article/details/50736647)
## *Subsequence Sum :
When all elements are positive and negative, we can use prefix sum + hashmap and this is more general.<br>
Otherwise, we can use sliding window and verify if the condition is satisfied.<br>
`Solution 1: prefix sum + hashmap`<br>
[LC974](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Unordered_map/974.%20Subarray%20Sums%20Divisible%20by%20K)<br>
`Solution 2: sliding window`<br>
[1477. Find Two Non-overlapping Sub-arrays Each With Target Sum](https://github.com/AL2O3-Z/Leetcode/blob/master/Slide%20Window/1477.%20Find%20Two%20Non-overlapping%20Sub-arrays%20Each%20With%20Target%20Sum)
## Frequent pb :
`hashmap` to store the pair of element and its frequence. <br>
If needed, use `priority_queue` or `bucket sorting` to sort the frequence.<br>
[692. Top K Frequent Words](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Queue/692.%20Top%20K%20Frequent%20Words)<br>
[347. Top K Frequent Elements](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/347.%20Top%20K%20Frequent%20Elements)<br>
[1481. Least Number of Unique Integers after K Removals](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1481.%20Least%20Number%20of%20Unique%20Integers%20after%20K%20Removals)<br>
## Sliding window
K moves - focus on the sliding window of size n - k;<br>
prefix sum  [1423. Maximum Points You Can Obtain from Cards](https://github.com/AL2O3-Z/Leetcode/blob/master/Slide%20Window/1423.%20Maximum%20Points%20You%20Can%20Obtain%20from%20Cards)<br>
difference in sw [1509. Minimum Difference Between Largest and Smallest Value in Three Moves](https://github.com/AL2O3-Z/Leetcode/blob/master/Slide%20Window/1509.%20Minimum%20Difference%20Between%20Largest%20and%20Smallest%20Value%20in%20Three%20Moves)<br>
## DFS in matrix
Just pay attention to the edge of the matrix and the condition of termination of current recursion<br>
What is more interesting is if we must do the backtrack or not : The same cell may or may not be used more than once.<br>
[463. Island Perimeter](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/463.%20Island%20Perimeter)<br>
[130. Surrounded Regions](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/130.%20Surrounded%20Regions)<br>
[79. Word Search(with backtrack)](https://leetcode.com/problems/word-search/)<br>
[140. Word Break II](https://github.com/AL2O3-Z/Leetcode/blob/master/Hard/212.%20Word%20Search%20II)<br>
## BFS in matrix
count and push the node in the queue<br>
[994. Rotting Oranges](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/994.%20Rotting%20Oranges)<br>
[542. 01 Matrix]<br>
[675. Cut Off Trees for Golf Event]
## Sort
1. `nth_element`(first,nth,last) if we just focus on if the kth elements in the sorted array, don't need to sort entire. <br>
This STL allows abtain the kth element satisfy the comparasion condition. And it's Time O(n) <br>
2. cmp in sort()<Br>
[1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)<br>
3. Priority_queue to sort in reel time(*****) && cmp in priority_queue<br>
In defaut, the bigger number is in front of the queue.<br>
Prefix sum [1508. Range Sum of Sorted Subarray Sums](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1508.%20Range%20Sum%20of%20Sorted%20Subarray%20Sums)<br>
Linked list [23. Merge k Sorted Lists](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/23.%20Merge%20k%20Sorted%20Lists)

## Trie
[720. Longest Word in Dictionary](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/String/720.%20Longest%20Word%20in%20Dictionary)<br>
[211. Add and Search Word - Data structure design](https://leetcode.com/problems/add-and-search-word-data-structure-design/)<br>
## Array
1. Permutation of two parts of sub-arrray<br>
[1442. Count Triplets That Can Form Two Arrays of Equal XOR](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1442.%20Count%20Triplets%20That%20Can%20Form%20Two%20Arrays%20of%20Equal%20XOR)<br>
2. Contanation of two array : 
```cpp
vec1.insert(vec1.end(), vec2.begin(), vec2.end());
```
3. Permutation<br>
3.1 All of elements in a array, add un new elements in the previous resultats and keep it as a new possible result<br>
[78. Subsets](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/78.%20Subsets)<br>
3.2 Expand the result like a tree, and pay attention to the termination condition<br>
Or the same idea like last one, the difference is that we use the previous results and abandon them<br>
[17. Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)<br>
[46. Permutations](https://leetcode.com/problems/permutations/)<br>
4. Conbination<br>
with and without repeating elements. And in the pb 39, some code for permutation to compare the difference.<br>
[39. Combination Sum](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/39.%20Combination%20Sum)<br>
[40. Combination Sum II](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/40.%20Combination%20Sum%20II)<br>
[322. Coin Change](https://github.com/AL2O3-Z/Leetcode/blob/master/DP/322.%20Coin%20Change)(DP && conbination && permutation)<br>
[518. Coin Change 2](https://github.com/AL2O3-Z/Leetcode/blob/master/DP/518.%20Coin%20Change%202)(DP && combination)<br>
Number of Conbination => unordered_map as a count of element so that they can be pair<br>
[1512. Number of Good Pairs](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1512.%20Number%20of%20Good%20Pairs)<br>
[1513. Number of Substrings With Only 1s](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/String/1513.%20Number%20of%20Substrings%20With%20Only%201s)(string pb)
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
*GOOD PB:
[1488. Avoid Flood in The City](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1488.%20Avoid%20Flood%20in%20The%20City)<Br>
[1419. Minimum Number of Frogs Croaking](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/String/1419.%20Minimum%20Number%20of%20Frogs%20Croaking)<BR>
[1493. Longest Subarray of 1's After Deleting One Element](https://github.com/AL2O3-Z/Leetcode/blob/master/Slide%20Window/1493.%20Longest%20Subarray%20of%201's%20After%20Deleting%20One%20Element)(DP, SW, 2Pointers)<br>
[1482. Minimum Number of Days to Make m Bouquets](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/1482.%20Minimum%20Number%20of%20Days%20to%20Make%20m%20Bouquets)(Binary Search)<br>
[621. Task Scheduler](https://leetcode.com/problems/task-scheduler/)(Priority_queue)<br>
