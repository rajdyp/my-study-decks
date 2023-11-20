# [Python for Coding Interviews](https://neetcode.io/courses/lessons/python-for-coding-interviews)

## Big O Complexity 
| Method or Data Type             | Time Complexity (Average/Worst Case)  | Space Complexity       |
|---------------------------------|---------------------------------------|------------------------|
| **List Methods**                |                                       |                        |
| `append()`                      | O(1)                                  | O(1)                   |
| `insert()`                      | O(n)                                  | O(1)                   |
| `pop()` (from the end)          | O(1)                                  | O(1)                   |
| `pop()` (from a specific index) | O(n)                                  | O(1)                   |
| `extend()` (concatenation)      | O(k)                                  | O(k)                   |
| `remove()`                      | O(n)                                  | O(1)                   |
| `sort()`                        | O(n log n)                            | O(n)                   |
| `reverse()`                     | O(n)                                  | O(1)                   |
| **Dictionary Methods**          |                                       |                        |
| Access by key                   | O(1) average, O(n) worst case (rare)  | O(n)                   |
| `get()`                         | O(1) average, O(n) worst case (rare)  | O(n)                   |
| `set()`                         | O(1) average, O(n) worst case (rare)  | O(n)                   |
| `keys()`                        | O(n)                                  | O(n)                   |
| `values()`                      | O(n)                                  | O(n)                   |
| `items()`                       | O(n)                                  | O(n)                   |
| **Set Methods**                 |                                       |                        |
| `add()`                         | O(1)                                  | O(1)                   |
| `remove()`                      | O(1)                                  | O(1)                   |
| `discard()`                     | O(1)                                  | O(1)                   |
| `union()`                       | O(len(s))                             | O(len(s))              |
| `intersection()`                | O(min(len(s), len(t)))                | O(min(len(s), len(t))) |
| **String Methods**              |                                       |                        |
| `len()`                         | O(1)                                  | O(1)                   |
| `split()`                       | O(n)                                  | O(n)                   |
| `join()`                        | O(n)                                  | O(n)                   |
| `replace()`                     | O(n)                                  | O(n)                   |
| **Tuples**                      |                                       |                        |
| Indexing                        | O(1)                                  | O(1)                   |
| Slicing                         | O(k) where k is the size of the slice | O(k)                   |
| **Sets**                        |                                       |                        |
| Membership test (in `x in s`)   | O(1)                                  | O(1)                   |
| **Queue (collections.deque)**   |                                       |                        |
| `append()` and `popleft()`      | O(1)                                  | O(1)                   |
| **Stack (list-based)**          |                                       |                        |
| `push()` and `pop()`            | O(1)                                  | O(1)                   |

## Popular Problem-Solving Techniques and Patterns

- **Two-Pointers Technique**: This technique involves using two pointers to traverse an array or sequence, often from opposite ends or within a subarray, to solve problems efficiently.

- **Sliding Window Technique**: This technique involves maintaining a "window" of elements in an array and sliding it through the array to solve problems like finding subarrays with a specific sum, longest substring with distinct characters, or substring matching.

- **Divide and Conquer**: This technique breaks down a problem into smaller subproblems, solves the subproblems recursively, and then combines their solutions to solve the overall problem. Examples include binary search, merge sort, and quicksort.

- **Greedy Algorithm**: Greedy algorithms make locally optimal choices at each step in the hope of finding a global optimum. They are often used for optimization problems where a series of decisions must be made.

- **Dynamic Programming**: This is a technique for solving problems by breaking them down into smaller overlapping subproblems and storing the results of these subproblems to avoid redundant calculations. It is commonly used for problems like finding the longest common subsequence, shortest path, or optimizing resource allocation.

- **Backtracking**: Backtracking is an algorithmic technique that incrementally builds a solution and abandons a candidate solution as soon as it is determined to be unworkable. It's often used for problems that involve searching for valid solutions within a search space, such as the N-Queens problem.

- **Depth-First Search (DFS) and Breadth-First Search (BFS)**: These are graph traversal techniques used to explore and search through nodes in graphs or trees. They have applications in problems like finding connected components, shortest paths, and more.

- **Binary Search**: Binary search is a divide-and-conquer technique used to search for a specific element in a sorted array. It significantly reduces the search space by repeatedly dividing it in half.

- **Topological Sort**: This technique is used for directed acyclic graphs (DAGs) to find a linear ordering of the nodes that respects the partial order imposed by the edges. It's essential for solving problems like scheduling and task dependency resolution.

- **Hashing**: Hashing is used to achieve fast data retrieval in situations where the data can be mapped to a fixed number of indices, such as dictionaries or implementing data structures like hash tables.

- **Floyd-Warshall Algorithm**: This is used to find the shortest paths between all pairs of nodes in a weighted graph. It's essential for solving problems related to network routing or distance calculations.

- **Trie (Prefix Tree)**: Tries are data structures used for efficient retrieval of keys in a large dataset, particularly in problems related to text or dictionary-like operations.

- **Bit Manipulation**: Bit manipulation techniques are often used for problems related to binary representation, bitwise operations, and combinatorial problems.

- **Heap Data Structure**: Heaps, such as binary heaps and priority queues, are used for maintaining a set of elements with specific ordering properties, like finding the smallest or largest elements efficiently.

- **Segment Tree and Fenwick Tree**: These are data structures for solving problems related to range queries, such as finding the minimum, maximum, or sum of elements in a specific range.

## Variables
```python
# variables are dynamicly typed
n = 0
print('n =', n)
>>> n = 0

n = "abc"
print('n =', n)
>>> n = abc

# multiple assignments
n, m = 0, "abc"
n, m, z = 0.125, "abc", False

# increment
n = n + 1     # good
n += 1        # good
n++           # bad

# none is null (absence of value)
n = 4
n = None
print("n =", n)
>>> n = None
```

## Math
```python
# division is decimal by default
print(5 / 2)
>>> 2.5

# double slash (aka floor division) rounds down
print(5 // 2)
>>> 2

# CAREFUL: most languages round toward 0 by default
# Python floor division round away from 0
print(-3 // 2)
>>> -2

# workaround for rounding toward 0 is to use decimal division and then convert to int
print(int(-3 / 2))
>>> -1

# modding is similar to most languages
print(10 % 3)
>>> 1

# except for negative values
print(-10 % 3)
>>> 2

# to be consistent with other languages modulo
import math
print(math.fmod(-10, 3))
>>> -1.0

# more math helpers
print(math.floor(3 / 2))
>>> 1

print(math.ceil(3 / 2))
>>> 2

print(math.sqrt(2))
>>> 1.4142135623730951

print(math.pow(2, 3))
>>> 8.0

# max and min int
float("inf")
float("-inf")

# python numbers are infinite so they never overflow
print(math.pow(2, 200))
>>> 1.6069380442589903e+60

# but still less than infinity
print(math.pow(2, 200) < float("inf"))
>>> True
```

## Array (List)
```python
# array
arr = [1, 2, 3]
print(arr)
>>> [1, 2, 3]

# can be used as a stack (Last In, First Out)
arr.append(4)
arr.append(5)
print(arr)
>>> [1, 2, 3, 4, 5]

arr.pop()
print(arr)
>>> [1, 2, 3, 4]

# stack is used to solve problems like:
# Tower of Hanoi
# N-Queens Problem
# Infix to Prefix Conversion

arr.insert(1, 7)
print(arr)
>>> [1, 7, 2, 3, 4]

arr[0] = 0
arr[3] = 0
print(arr)
>>> [0, 7, 2, 0, 4]

# initialize array of size n with default value of 1
n = 5
arr = [1] * n
print(arr)
>>> [1, 1, 1, 1, 1]
print(len(arr))
>>> 5

# -1 is last value
arr = [1, 2, 3]
print(arr[-1])
>>> 3

# indexing -2 is the second to last value, etc.
print(arr[-2])
>>> 2

# sublists (aka slicing)
arr = [1, 2, 3, 4]
print(arr[1:3])
>>> [2, 3]

# similar to for-loop ranges, last index is non-inclusive
print(arr[0:4])
>>> [1, 2, 3, 4]

# but no out of bounds error
print(arr[0:10])
>>> [1, 2, 3, 4]

# unpacking
a, b, c = [1, 2, 3]
print(a, b, c)
>>> 1 2 3

# be careful though
a, b = [1, 2, 3]
print(a, b)
>>> ValueError: too many values to unpack (expected 2)

# loop through arrays
nums = [1, 2, 3]

# using index
for i in range(len(nums)):
    print(nums[i])
>>> 1
>>> 2
>>> 3

# without index
for n in nums:
    print(n)
>>> 1
>>> 2
>>> 3

# with index and value
for i, n in enumerate(nums):
    print(i, n)
>>> 0 1
>>> 1 2
>>> 2 3

# loop through multiple arrays simultaneously with unpacking
nums1 = [1, 3, 5]
nums2 = [2, 4, 6]
for n1, n2 in zip(nums1, nums2):
    print(n1, n2)
>>> 1 2
>>> 3 4
>>> 5 6

# reverse
nums = [1, 2, 3]
nums.reverse()
print(nums)
>>> [3, 2, 1]

# sorting
arr = [5, 4, 7, 3, 8]
arr.sort()
print(arr)
>>> [3, 4, 5, 7, 8]

arr.sort(reverse=True)
print(arr)
>>> [8, 7, 5, 4, 3]

arr = ["bob", "alice", "jane", "doe"]
arr.sort()
print(arr)
>>> ['alice', 'bob', 'doe', 'jane']

# custom sort (by length of string)
arr.sort(key=lambda x: len(x))
print(arr)
>>> ['bob', 'doe', 'jane', 'alice']

# list comprehension
arr = [i for i in range(5)]
print(arr)
>>> [0, 1, 2, 3, 4]

# 2-D lists
arr = [[0] * 4 for i in range(4)]
print(arr)
>>> [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]
print(arr[0][0], arr[3][3])
>>> 0 0

# this won't work
arr = [[0] * 4] * 4
print(arr)
[[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]    # not creating unique four rows
```

## Strings
```python
# strings are similar to arrays
s = "abc"
print(s[0:2])
>>> ab

# but they are immutable
# s[0] = "A"
>>> TypeError: 'str' object does not support item assignment

# in rare cases you may need the ASCII value of a char
print(ord("a"))
>>> 97
print(ord("b"))
>>> 98

# combine a list of strings (with an empty string delimitor)
strings = ["ab", "cd", "ef"]
print("".join(strings))
>>> abcdef
```

## Queues
```python
# queues (double ended queue)
from collections import deque

queue = deque()
queue.append(1)
queue.append(2)
print(queue)
>>> deque([1, 2])

queue.popleft()
print(queue)
>>> deque([2])

queue.appendleft(1)
print(queue)
>>> deque([1, 2])

queue.pop()
print(queue)
>>> deque([1])
```

## HashSet (Set)
```python
# HashSet
mySet = set()

mySet.add(1)
mySet.add(2)
print(mySet)
>>> {1, 2}
print(len(mySet))
>>> 2

print(1 in mySet)
>>> True
print(2 in mySet)
>>> True
print(3 in mySet)
>>> False

mySet.remove(2)
print(2 in mySet)
>>> False

# list to set
print(set([1, 2, 3]))
>>> {1, 2, 3}

# set comprehension
mySet = {i for i in range(5)}
print(mySet)
>>> 0, 1, 2, 3, 4}
```

## HashMap (Dictionary)
```python
# HashMap
myMap = {}
myMap["alice"] = 88
myMap["bob"] = 77
print(myMap)
>>> {'alice': 88, 'bob': 77}
print(len(myMap))
>>> 2

myMap["alice"] = 80
print(myMap["alice"])
>>> 80

print("alice" in myMap)
>>> True
myMap.pop("alice")
print("alice" in myMap)
>>> False

myMap = {"alice": 90, "bob": 70}
print(myMap)
>>> {'alice': 90, 'bob': 70}

# dict comprehension
myMap = {i: 2*i for i in range(3)}
print(myMap)
>>> {0: 0, 1: 2, 2: 4}

# looping through maps
myMap = {"alice": 90, "bob": 70}
for key in myMap:
    print(key, myMap[key])
>>> alice 90
>>> bob 70

for val in myMap.values():
    print(val)
>>> 90
>>> 70

for key, val in myMap.items():
    print(key, val)
>>> alice 90
>>> bob 70
```

## Tuples
```python
# tuples are like arrays but immutable
tup = (1, 2, 3)
print(tup)
>>> (1, 2, 3)
print(tup[0])
>>> 1
print(tup[-1])
>>> 3

# can't modify (immutable)
tup[0] = 0
>>> TypeError: 'tuple' object does not support item assignment

# can be used as key for hashmap/hashset
myMap = {(1,2): 3}
print(myMap[(1,2)])
>>> 3

mySet = set()
mySet.add((1, 2))
print((1, 2) in mySet)
>>> True

# list can't be key for hashmap/hashset
myMap = {}
myMap[[3, 4]] = 5
print(myMap)
>>> {'x': 5}
# myMap["x"] = 5
print(myMap)
>>> TypeError: unhashable type: 'list'
```

## Heaps
```python
import heapq    # min-heap implementation

# under the hood are arrays
minHeap = []
heapq.heappush(minHeap, 3)
print(minHeap)
>>> [3]
heapq.heappush(minHeap, 2)
print(minHeap)
>>> [2, 3]
heapq.heappush(minHeap, 4)
print(minHeap)
>>> [2, 3, 4]

# min is always at index 0
print(minHeap[0])
>>> 2

while len(minHeap):
    print(heapq.heappop(minHeap))
>>> 2
>>> 3
>>> 4

# no max heaps by default, work around is to use min heap and multiply by -1 when push & pop
maxHeap = []
heapq.heappush(maxHeap, -3)
print(maxHeap)
>>> [-3]
heapq.heappush(maxHeap, -2)
print(maxHeap)
>>> [-3, -2]
heapq.heappush(maxHeap, -4)
print(maxHeap)
>>> [-4, -2, -3]

# max is always at index 0
print(-1 * maxHeap[0])
>>> 4

while len(maxHeap):
    print(-1 * heapq.heappop(maxHeap))
>>> 4
>>> 3
>>> 2

# build heap from initial values
arr = [2, 1, 8, 4, 5]
heapq.heapify(arr)
while arr:
    print(heapq.heappop(arr))
>>> 1
>>> 2
>>> 4
>>> 5
>>> 8
```

## Functions
```python
def myFunc(n, m):
    return n * m

print(myFunc(3, 4))
>>> 12

# nested functions have access to outer variables
def outer(a, b):
    c = "c"

    def inner():
        return a + b + c
    return inner()

print(outer("a", "b"))
>>> abc

# can modify objects but not reassign unless using nonlocal keyword
def double(arr, val):
    def helper():
        # modifying array works
        for i, n in enumerate(arr):
            arr[i] *= 2
        
        # will only modify val in the helper scope
        # val *= 2

        # this will modify val outside helper scope
        nonlocal val
        val *= 2
    helper()
    print(arr, val)

nums = [1, 2]
val = 3
double(nums, val)
>>> [2, 4] 6
```

## Classes
```python
class MyClass:
    # constructor
    def __init__(self, nums):
        # Create member variables
        self.nums = nums
        self.size = len(nums)
    
    # self key word required as param
    def getLength(self):
        return self.size

    def getDoubleLength(self):
        return 2 * self.getLength()

myObj = MyClass([1, 2, 3])
print(myObj.getLength())
print(myObj.getDoubleLength())
```
