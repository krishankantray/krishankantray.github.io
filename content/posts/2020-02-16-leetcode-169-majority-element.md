+++
title = "LeetCode: 169 Majority Element"
slug = "2020-02-16-leetcode-169-majority-element"
published = 2020-02-16T11:36:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
## LEETCODE : 169. Majority Element

[Link](https://leetcode.com/problems/majority-element/)

**Problem Description :**

Given an array of size n, find the majority element. The majority element is
the element that appears more than ⌊ n/2 ⌋ times.  
  
You may assume that the array is non-empty and the majority element
always exist in the array.

For example:  
**Example 1:**  

```
Input: [3,2,3]
Output: 3 
```
     
**Example 2:**  

```
Input: [2,2,1,1,1,2,2]
Output: 2
```
**Explaination :**

There is pretty easy way to solve it by using count of every element and then returning the element which has count greater than n/2 .

But this solution comes with a cost of O(n) time and O(n) space.

There is a better solution which can do the job in O(n) time and O(1) space.
Atleast we are saving some of the space.
How does our space efficient algorithm works ?

Basically, what we do is that we go on cancelling those elements which has a
counter element present, a counter element is an element whose value is
different from the current element. In other words, we can say that, we
cancel every element corresponding to every other uncancelled element
whose value is different.

In C++ we can write it as below :

```cpp

class Solution {
public:
    int majorityElement(vector<int>& nums) {
        
        int val=nums[0];
        int count=1;
        
        for(int i=1; i<nums.size(); i++){
            if(count==0){
                val=nums[i];
                
            }
            count += nums[i]==val?1:-1 ;
        }
        return val; 
    }
};
```