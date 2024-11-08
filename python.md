1. Iterable
   - can be looped over with a for loop
   - can be converted to an iterator
```Python
iterable = [1, 2, 3]
iterator = iter(iterable)
print(next(iterator))  # Output: 1
print(next(iterator))  # Output: 2
print(next(iterator))  # Output: 3
```
Some common types of iterables in Python include:

- List (list): e.g., [1, 2, 3]
- Tuple (tuple): e.g., (1, 2, 3)
- String (str): e.g., "hello"
- Dictionary (dict): e.g., {"a": 1, "b": 2}
- Set (set): e.g., {1, 2, 3}
- Generator (generator): e.g., a generator expression like (x for x in range(3))
  - The yield statement is used within a function to turn it into a generator

2. Linear structure
   - array
   - linked list
   - string
  


3. Double Ended Queue (BFS)
   - collections.deque()
     - popleft()
     - pop()
     - appendleft()
     - append()
     <img width="600" alt="Screenshot 2024-11-08 at 3 17 44 PM" src="https://github.com/user-attachments/assets/b2da10c1-689a-4b74-be1d-c132c6312205">
  
4. heapq （kth largest; median; ...）
   - heapq.heapify([])
      - heapq.heappush()
      - heapq.heappop()
      - heap[0]: min value
      - 默认是最小堆，如果想要最大堆，heappush的时候 val *（-1）
<img width="600" alt="Screenshot 2024-11-07 at 4 51 11 PM" src="https://github.com/user-attachments/assets/5333284d-1525-4bf2-abe0-15af5f6e9aaf">


5. Counter
   - collections.Counter
```Python
from collections import Counter

def top_k_frequent(nums, k):
    count = Counter(nums)
    return [item for item, _ in count.most_common(k)]
```

5. defaultdict 带默认值的字典
```Python
from collections import defaultdict

def group_anagrams(strs):
    anagrams = defaultdict(list)
    for s in strs:
        sorted_s = ''.join(sorted(s))
        anagrams[sorted_s].append(s)
    return list(anagrams.values())
```

6. bisect
```Python
import bisect

def search_insert(nums, target):
    return bisect.bisect_left(nums, target)
```

7. lru_cache
```Python
from functools import lru_cache

# Decorator
@lru_cache(None)
def fibonacci(n):
    if n < 2:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)
```

8. itertools.permutations
```Python
from itertools import permutations

def permute(nums):
    return list(permutations(nums))
```

9. itertools.combinations
```Python
from itertools import combinations

nums = [1, 2, 3, 4]
result = list(combinations(nums, 2))
print(result)
# [(1, 2), (1, 3), (1, 4), (2, 3), (2, 4), (3, 4)]
```

```Python
def combination_sum(nums, target):
    result = []
    for r in range(1, len(nums) + 1):
        for combo in combinations(nums, r):
            if sum(combo) == target:
                result.append(combo)
    return result

print(combination_sum([2, 3, 5, 7], 10))
# [(3, 7), (2, 3, 5)]
```
