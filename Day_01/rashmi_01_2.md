Date: 24 Aug 2024

Link: https://neetcode.io/problems/is-anagram

# Question 2: 
### Is Anagram
Given two strings s and t, return true if the two strings are anagrams of each other, otherwise return false.

An anagram is a string that contains the exact same characters as another string, but the order of the characters can be different.

### Example 1:

Input: s = "racecar", t = "carrace"

Output: true
### Example 2:

Input: s = "jar", t = "jam"

Output: false
### Constraints:

s and t consist of lowercase English letters.

# Solution 

```
class Solution {
    public boolean isAnagram(String s, String t) {
       char[] new_s = s.toCharArray();
       char[] new_t = t.toCharArray();
       
       Arrays.sort(new_s);
       Arrays.sort(new_t);

       if(s.length()!=t.length()){
        return false;
       }
       for(int i=0;i<new_s.length;i++){
        if(new_s[i]!=new_t[i]){
            return false;
        }
       }
       return true;
    }
}
```