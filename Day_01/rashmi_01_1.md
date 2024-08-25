Date: 24 Aug 2024

Link:  https://neetcode.io/problems/duplicate-integer

# Question 1: 
### Duplicate Integer
Given an integer array `nums`, return true if any value appears more than once in the array, otherwise return false.

### Example 1:

**Input:** `nums = [1, 2, 3, 3]`

**Output:** `true`

### Example 2:

**Input:** `nums = [1, 2, 3, 4]`

**Output:** `false`

## Solution:
1. **Comparing each value of the array with the other values of the array.**
   - Time complexity: O(n²)
   - Space complexity: O(1)

```java
class Solution {
    public boolean hasDuplicate(int[] nums) {
        for(int i = 0; i < nums.length; i++) {
            for(int j = i + 1; j < nums.length; j++) {
                if(nums[i] == nums[j]) {
                    return true;
                }
            }
        }
        return false;
    }
}
```
2. **Sorting the array then comparing**
 - Time complexity: O(n log n)
 - Space complexity: O(1)

```
import java.util.Arrays;

class Solution {
    public boolean hasDuplicate(int[] nums) {
        Arrays.sort(nums);
        for (int i = 0; i < nums.length - 1; i++) {
            if(nums[i] == nums[i + 1]) {
                return true;
            }
        }
        return false;
    }
}