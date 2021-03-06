+++
author = "Krishankant"
authorTwitter = ""
cover = "/uploads/monotonic-stack.jpg"
date = 2021-10-04T22:05:57Z
description = "A whole range of problems based on monotonic stack"
keywords = []
showfullcontent = false
tags = ["dsa", "algorithm", "next-greatest-element", "stack", "monotonic-stack"]
title = "Monotonic Stack based problems"

+++
# Next Greater Element ( variants )

This problem states that for every index `i` in the given array, we need to find the element to the right of it which is just greater ( not smaller ) than the elment at `i`.

**Entire list** - [https://leetcode.com/tag/monotonic-stack/](https://leetcode.com/tag/monotonic-stack/)

There are two ways to solve this problem  :

* Using stack ( this is most popular one )
* Without using stack

Problems that are based on this concept are :

* Next Greater Element I - [https://leetcode.com/problems/next-greater-element-i/](https://leetcode.com/problems/next-greater-element-i/)
* Next Greater Element II : [https://leetcode.com/problems/next-greater-element-ii/](https://leetcode.com/problems/next-greater-element-ii/)
* Next Greater Element III :  [https://leetcode.com/problems/next-greater-element-iii/](https://leetcode.com/problems/next-greater-element-iii/)
* Largest Rectangle histogram : [https://leetcode.com/problems/largest-rectangle-in-histogram/](https://leetcode.com/problems/largest-rectangle-in-histogram/)
* Maximal Rectangle : [https://leetcode.com/problems/maximal-rectangle/](https://leetcode.com/problems/maximal-rectangle/)

The order of relationship is : `NGE` > `largest rect histogram` > `maximal rectangle`

**Next Greater Element** code using stacks :

```cpp
/*
	INPUT : [1,2,1]
	OUTPUT : [2,-1,-1]
*/
vector<int> nextGreaterElements(vector<int>& nums) {
        int n = nums.size() ;
        vector<int>nge(n);
        stack<int>s ;
        for(int i=n-1; i>=0; i--){
            if(s.empty()){
                nge[i]=-1 ;
            }
            else if(s.top() >= nums[i]){
                nge[i]=s.top() ;
            }
            else if(s.top()<nums[i]){
                while(!s.empty() && s.top()<nums[i]) s.pop() ;
                if(s.empty()) nge[i]=-1 ;
                else nge[i]=s.top() ;
            }
            s.push(nums[i]) ;
        }
        return nge ; 
    }
```

[1130. Minimum Cost Tree From Leaf Values](https://leetcode.com/problems/minimum-cost-tree-from-leaf-values/discuss/339959/One-Pass-O(N)-Time-and-Space)

[907. Sum of Subarray Minimums](https://leetcode.com/problems/sum-of-subarray-minimums/discuss/170750/C++JavaPython-Stack-Solution)

[901. Online Stock Span](https://leetcode.com/problems/online-stock-span/discuss/168311/C++JavaPython-O(1))

[856. Score of Parentheses](https://leetcode.com/problems/score-of-parentheses/discuss/141777/C++JavaPython-O(1)-Space)

[503. Next Greater Element II](https://leetcode.com/problems/next-greater-element-ii/discuss/98270/JavaC++Python-Loop-Twice)

1. Next Greater Element I
2. Largest Rectangle in Histogram
3. Trapping Rain Water