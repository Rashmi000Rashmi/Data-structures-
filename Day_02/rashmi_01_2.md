- Date : 28 Aug 2024
- Link : https://neetcode.io/problems/anagram-groups

# Question 
### Anagram Groups

Given an array of strings strs, group all anagrams together into sublists. You may return the output in any order.

An anagram is a string that contains the exact same characters as another string, but the order of the characters can be different.

### Example 1:

Input: strs = ["act","pots","tops","cat","stop","hat"]

Output: [["hat"],["act", "cat"],["stop", "pots", "tops"]]
### Example 2:

Input: strs = ["x"]

Output: [["x"]]
### Example 3:

Input: strs = [""]

Output: [[""]]
### Constraints:

1 <= strs.length <= 1000.
0 <= strs[i].length <= 100
strs[i] is made up of lowercase English letters.

# Solution 
```
class Solution {
    public List<List<String>> groupAnagrams(String[] strs) {

        HashMap<String,List<String>> anagram = new HashMap<>();

        // Add the anagram to the hashMap
        for(int i = 0;i<strs.length;i++){
            String sort_element = sort(strs[i]);

            if(anagram.containsKey(sort_element)){
                anagram.get(sort_element).add(strs[i]);
            }else{
                List<String> val_list = new ArrayList<>();
                val_list.add(strs[i]);
                anagram.put(sort_element, val_list);
            }
        }

        List<List<String>> result = new ArrayList<>();

        for(Map.Entry<String, List<String>> val : anagram.entrySet()){
            result.add(val.getValue());
        }

        return result;
        
    }

    public String sort(String element){
        // Change to char array
        char elementArray[] = element.toCharArray();

        // Sort the char array
        Arrays.sort(elementArray);

        // Change the array back to String
        String sorted = new String(elementArray);

        return sorted;
    }
}
