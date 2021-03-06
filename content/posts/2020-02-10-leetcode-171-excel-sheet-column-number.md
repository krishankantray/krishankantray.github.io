+++
title = "LEETCODE : 171. Excel Sheet Column Number"
slug = "2020-02-10-leetcode-171-excel-sheet-column-number"
published = 2020-02-10T00:25:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
## <span style="font-family: &quot;verdana&quot; , sans-serif;">LEETCODE : 171. Excel Sheet Column Number</span>

[Link](https://leetcode.com/problems/excel-sheet-column-number)

  

**Problem Description :**

Given a column title as appear in an Excel sheet, return its corresponding
column number.
  
For example:
```

        A -> 1
        B -> 2
        C -> 3
        ...
        Z -> 26
        AA -> 27
        AB -> 28 
        ...
```
  
**Example 1:**

    Input: "A"
    Output: 1 

     

**Example 2:** 

    Input: "AB"
    Output: 28

**Example 3:**
  

    Input: "ZY"
    Output: 701 

***

**Explaination :**

Initially it looks like a hard problem but when we get to know the logic behind it then it seems to be a really easy problem.

The observation needed here is that, the column title value represents a
number of base 26. And all we need to do is to convert that base 26
number to base 10 number.

To convert the base to base 10, we need to do what we usually do for binary
or octal converstions.

*For example :*  

```  

BAD

B=2
A=1
D=4
 
2x(26)^2 + 1x(26) + 4x(26)^0 
= 1352
+ 26 + 4
=
1382

```

**In C++ we can write it as below :**

```cpp


    class Solution {
    public:
        int titleToNumber(string s) {
            int ans =0;
            long pwr=1;
            reverse(s.begin(), s.end()) ;
            for(auto c:s){
                ans+=(pwr*(c-'A' +1));
                pwr=pwr*26;
            }
            return ans;
        }
    };
```