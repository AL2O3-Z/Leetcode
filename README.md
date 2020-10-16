# Leetcode
[文字格式](https://blog.csdn.net/u012067966/article/details/50736647)
[Template](https://blog.csdn.net/fuxuemingzhu/article/details/101900729)
## *Subsequence Sum :
When all elements are positive and negative, we can use prefix sum + hashmap and this is more general.<br>
Otherwise, we can use sliding window and verify if the condition is satisfied.<br>
`Solution 1: prefix sum + hashmap`<br>
[974. Subarray Sums Divisible by K](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Unordered_map/974.%20Subarray%20Sums%20Divisible%20by%20K)<br>
[1546. Maximum Number of Non-Overlapping Subarrays With Sum Equals Target](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Unordered_map/1546.%20Maximum%20Number%20of%20Non-Overlapping%20Subarrays%20With%20Sum%20Equals%20Target)<br>
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
## Binary Search
A TRICK : In this problem, you can transfer a 2D array to 1D array using `x * y = r => matrix[r/x][r%y]`
and we can use binary search.<Br>
[74. Search a 2D Matrix](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/74.%20Search%20a%202D%20Matrix)<br>

## Tree
Using a string or a long int to represent a tree (a long int improve the time)<br>
[652. Find Duplicate Subtrees](https://github.com/AL2O3-Z/Leetcode/blob/master/Tree/652.%20Find%20Duplicate%20Subtrees)<br>

## DFS
### In matrix
>Just pay attention to the edge of the matrix and the condition of termination of current recursion<br>
What is more interesting is if we must do the backtrack or not : The same cell may or may not be used more than once.<br>
[463. Island Perimeter](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/463.%20Island%20Perimeter)<br>
>[130. Surrounded Regions](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/130.%20Surrounded%20Regions)<br>
[417. Pacific Atlantic Water Flow](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/417.%20Pacific%20Atlantic%20Water%20Flow)<br>
### In word
>[79. Word Search(with backtrack)](https://leetcode.com/problems/word-search/)<br>
>[140. Word Break II](https://github.com/AL2O3-Z/Leetcode/blob/master/Hard/212.%20Word%20Search%20II)<br>
### In Graph
>In this pb, we use map to mapping the node visited rather than a set, because it's more easy to find the relation of mapping<br>
and it works also with DFS.
[133. Clone Graph](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/133.%20Clone%20Graph)<br>
>COLORING <br>
Node's coloring [785. Is Graph Bipartite?](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/785.%20Is%20Graph%20Bipartite%3F) same with 886. Possible Bipartition<br>
Edge's coloring [1129. Shortest Path with Alternating Colors](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/1129.%20Shortest%20Path%20with%20Alternating%20Colors)<br>
## BFS 
Distance/non-weight => BFS or DP
### In Matrix
unique or multi source, to find the shortest route from the source, level by level<br>
just extends outwards and push the nodes of next level to the queue and treat them as new source <br>
[994. Rotting Oranges](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/994.%20Rotting%20Oranges)<br>
[542. 01 Matrix](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/542.%2001%20Matrix) && 1162. As Far from Land as Possible<br>
[675. Cut Off Trees for Golf Event]
### In Tree
If we need to backward to the parent, we can build an undirected graph to reprente the relation<br>
[863. All Nodes Distance K in Binary Tree](https://github.com/AL2O3-Z/Leetcode/blob/master/Tree/863.%20All%20Nodes%20Distance%20K%20in%20Binary%20Tree)<br>
### In Graph
In this pb, we use map to mapping the node visited rather than a set, because it's more easy to find the relation of mapping<br>
and it works also with DFS.
[133. Clone Graph](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/133.%20Clone%20Graph)
## Graph
### Union Find
No direction, no cycle => every cluster/set includes all the nodes. If another added edge, but their points of this edge is in the same cluster, we think this edge isn't valid.<br>
[684. Redundant Connection](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/684.%20Redundant%20Connection)<br>
[547. Friend Circles](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/547.%20Friend%20Circles)<br>
Hard one. And here is a trick to play with : eliminating the second candidate while checking the cycle without it.<br>
If there still exist a cycle, it's the old one creat it. so return it.<br>
else maybe it's the second candidate's fault or nothing to delecting.<br>
[685. Redundant Connection II](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/685.%20Redundant%20Connection%20II)<br>
Interesting One. 0 : if two surfaces are merged, they are in the same cluster => `Union find`<br>
A : reforme a 2D array to 1D by indexing i and j and the offset of every triangle in the square <br>
B : merge the triangle inner connection and inter connection <br>
[959. Regions Cut By Slashes](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/959.%20Regions%20Cut%20By%20Slashes)<br>
Interesting One : another view of 2D => a stone(data) represente the connection of col and row, all the stones in the same col or row represente the same island, so the index of col or row can represente different island<br>
[947. Most Stones Removed with Same Row or Column](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/947.%20Most%20Stones%20Removed%20with%20Same%20Row%20or%20Column)<br>
Interesting One : a pair of swap represente one connection. All of the characters in the same clusters can be sorted. So this problem could be transformed to find the connection component.<br>
[1202. Smallest String With Swaps](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/1202.%20Smallest%20String%20With%20Swaps)<br>
### Shortest path 
#### Multisource + single-destination (Floyd-Warshall + V*Dijkstra) (weight)
non-directed, weight[1334. Find the City With the Smallest Number of Neighbors](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/1334.%20Find%20the%20City%20With%20the%20Smallest%20Number%20of%20Neighbors%20at%20a%20Threshold%20Distance)<br>
#### Multisource + multi-destination (DFS + BFS) (non-weight)
non-directed, non weight[934. Shortest Bridge](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/934.%20Shortest%20Bridge)<br>
#### Single Source
Directed, non-weight => BFS [1129. Shortest Path with Alternating Colors](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/1129.%20Shortest%20Path%20with%20Alternating%20Colors)<br>
Directed, weight => BFS/DFS/Bellman-ford[787. Cheapest Flights Within K Stops](https://github.com/AL2O3-Z/Leetcode/blob/master/Graph/787.%20Cheapest%20Flights%20Within%20K%20Stops)<br>
## Sort
### Sort-1. Have fun
1. `nth_element`(first,nth,last) if we just focus on if the kth elements in the sorted array, don't need to sort entire. <br>
This STL allows abtain the kth element satisfy the comparasion condition. And it's Time O(n) <br>
2. cmp in sort()<Br>
[1471. The k Strongest Values in an Array](https://leetcode.com/problems/the-k-strongest-values-in-an-array/)<br>
3. Priority_queue to sort in reel time(*****) && cmp in priority_queue<br>
In defaut, the bigger number is in front of the queue.<br>
Prefix sum [1508. Range Sum of Sorted Subarray Sums](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1508.%20Range%20Sum%20of%20Sorted%20Subarray%20Sums)<br>
Linked list [23. Merge k Sorted Lists](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/23.%20Merge%20k%20Sorted%20Lists)<br>
4. Sort of vector<br>
Value max by incrementing of its frequence == Value min by decreasing it. In addition, we can use operator ==, <, > to compare two sorting array.<br>
[1366. Rank Teams by Votes](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1366.%20Rank%20Teams%20by%20Votes)<br>

### Sort-2. [Sorting methods](https://www.cnblogs.com/onepixel/p/7674659.html)
1. Counting Sort => Time O(n + k) || Space O(n + k)<br>
this type of sorting is for the data in the some range. It's not comparable sorting, and it needs extra space, but it is faster than any sorting method<br>
[274. H-Index](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/274.%20H-Index)<br>
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
[1513. Number of Substrings With Only 1s](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/String/1513.%20Number%20of%20Substrings%20With%20Only%201s)(string pb)<br>
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
[1488. Avoid Flood in The City](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1488.%20Avoid%20Flood%20in%20The%20City)<br>
[1419. Minimum Number of Frogs Croaking](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/String/1419.%20Minimum%20Number%20of%20Frogs%20Croaking)<br>
[1493. Longest Subarray of 1's After Deleting One Element](https://github.com/AL2O3-Z/Leetcode/blob/master/Slide%20Window/1493.%20Longest%20Subarray%20of%201's%20After%20Deleting%20One%20Element)(DP, SW, 2Pointers)<br>
[1482. Minimum Number of Days to Make m Bouquets](https://github.com/AL2O3-Z/Leetcode/blob/master/Search/1482.%20Minimum%20Number%20of%20Days%20to%20Make%20m%20Bouquets)(Binary Search)<br>
[621. Task Scheduler](https://leetcode.com/problems/task-scheduler/)(Priority_queue)<br>
[1558. Minimum Numbers of Function Calls to Make Target Array](https://github.com/AL2O3-Z/Leetcode/blob/master/Bit%20Wise/1558.%20Minimum%20Numbers%20of%20Function%20Calls%20to%20Make%20Target%20Array)(Bit wise)<br>
[1560. Most Visited Sector in a Circular Track](https://github.com/AL2O3-Z/Leetcode/blob/master/Structure/Array/1560.%20Most%20Visited%20Sector%20in%20a%20Circular%20Track)<br>
[1366. Rank Teams by Votes](https://github.com/AL2O3-Z/Leetcode/blob/master/Sort/1366.%20Rank%20Teams%20by%20Votes)<br>

