# LeetCode ProblemSet [click here](https://leetcode.com/problemset/all/) () {...}

## Table of Contents

1. [Array](#array)


## Array

**[1.1] Two Sum [link](https://leetcode.com/problems/two-sum/)**

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

**[1.2] Find the Array Concatenation Value [link](https://leetcode.com/problems/find-the-array-concatenation-value/)**

```java
class Solution {
    public long findTheArrayConcVal(int[] nums) {
        long ConcatValue=0;
        int i=0,j=nums.length-1;
        while(i<=j) 
        {
            if(i == j)
            {
                ConcatValue += nums[i];
                break;
            } 
            int first=nums[i];
            int last=nums[j];
            String ConcatString = Integer.toString(first) + Integer.toString(last);
            ConcatValue += Long.parseLong(ConcatString);
            i++;
            j--;
        }
        return ConcatValue;         
    }
}
```
