# Search insert position
## https://leetcode.com/problems/search-insert-position 

Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

You must write an algorithm with O(log n) runtime complexity.

 
```
Example 1:

Input: nums = [1,3,5,6], target = 5
Output: 2

Example 2:

Input: nums = [1,3,5,6], target = 2
Output: 1

Example 3:

Input: nums = [1,3,5,6], target = 7
Output: 4
``` 

## Constraints:
```
1 <= nums.length <= 10^4
-10^4 <= nums[i] <= 10^4
nums contains distinct values sorted in ascending order.
-10^4 <= target <= 10^4
```

# Implementation 1 :
```java
class Solution {
    public int searchInsert(int[] nums, int target) {
        if(nums == null)
            return -1;
        if(nums.length == 0)
            return 0;
        int i = 0;
        for(;i < nums.length; i++) {
            if(nums[i] >= target)
                return i;
        }
        return i;
    }
}
```
