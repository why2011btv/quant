# Coding

## Data Type
int64 max value = 2^63 - 1
4 byte：int32

## Order 
1. moving average
2. moving median

## Sorting
1. Counting Sort
 - 条件：数组中都是正整数、最大值比较小的
 - step 1: 先找到最大值
 - step 2: count
 - step 3: count -> prefix sum (看有几个元素 <= k)，count[i] = count[i-1] + count[i]
 - step 4: 从后往过一遍input array，在count中找到这个元素应该去的位置；更新count[i]  
2. Radix Sort 数位排序
 - 排序是稳定的：在排序算法中，**稳定**意味着如果两个元素具有相同的键值（即相等的值），它们在排序后的相对顺序与排序前保持一致。
 - 先排最不重要的数位（个位），再依次排十位、百位。。。
 - 每个数位的排序：任意一个稳定的排序算法（stable sort）如counting sort


## heapq
<img width="1052" alt="Screenshot 2024-11-07 at 4 51 11 PM" src="https://github.com/user-attachments/assets/5333284d-1525-4bf2-abe0-15af5f6e9aaf">
