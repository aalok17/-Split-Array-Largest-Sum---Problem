# Split Array Largest Sum -Problem
Problem of Day Solution (13-dec-2022) (GFG)

```
class Solution:
    def splitArray(self, arr, N, K):
        a,b = max(arr), sum(arr)
        
        while a < b:
            mid = (a + b) // 2
            cursum, count = 0, 0
            for num in arr:
                cursum += num
                if cursum > mid:
                    cursum = num
                    count += 1
            if count >= K: a = mid + 1
            
            else: b = mid
        return b
