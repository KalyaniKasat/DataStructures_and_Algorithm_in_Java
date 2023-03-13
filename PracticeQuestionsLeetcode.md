# BLIND 75 🧠

## Table of Contents

1. [Arrays & Hashing](#arrays--hashing)


## Arrays & Hashing  


**[1.1] Contains Duplicate [link](https://leetcode.com/problems/contains-duplicate/description/)**

```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        HashSet<Integer> ToStoreValueOnce = new HashSet<Integer>();
        for(int i=0;i<nums.length;i++)
        {           
            if(ToStoreValueOnce.contains(nums[i])) 
            {
                return true;
            }
            ToStoreValueOnce.add(nums[i]);
        }
        return false;  
    } 
}
```

**[1.2] Valid Anagram [link](https://leetcode.com/problems/valid-anagram/description/)**

```java
class Solution {
    public boolean isAnagram(String s, String t) {
        char ConvertingString_S [] = s.toCharArray();
        char ConvertingString_t [] = t.toCharArray();
        Arrays.sort(ConvertingString_S);
        Arrays.sort(ConvertingString_t);
        
        if(Arrays.equals(ConvertingString_S,ConvertingString_t))
        {
            return true;
        }
        return false;
    }
}
```

**[1.3] Two Sum [link](https://leetcode.com/problems/two-sum/description/)**

```java
class Solution {
    public int[] twoSum(int[] nums, int target) 
    {
        int[] OutputArray= new int[2];
        for(int i=0;i<nums.length;i++)
        {
            for(int j=i+1;j<nums.length;j++)
                {
                   if(nums[i] + nums[j] == target)
                   {
                       OutputArray[0]=i;
                       OutputArray[1]=j;                      
                   }                   
                }           
        }
        return OutputArray;
    }
} 
```
**[1.4] Group Anagrams [link](https://leetcode.com/problems/group-anagrams/)**

```java
class Solution {
    public List<List<String>> groupAnagrams(String[] strs) {
        if (strs.length == 0) return new ArrayList();
        Map<String, List> ans = new HashMap<String, List>();
        for (String s : strs) {
            char[] ca = s.toCharArray();
            Arrays.sort(ca);
            String key = String.valueOf(ca);
            if (!ans.containsKey(key)) ans.put(key, new ArrayList());
            ans.get(key).add(s);
        }
        return new ArrayList(ans.values());
    }
} 
```