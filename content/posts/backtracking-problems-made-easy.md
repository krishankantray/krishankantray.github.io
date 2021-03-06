+++
author = "Krishankant"
authorTwitter = ""
cover = ""
date = 2021-09-26T21:15:56Z
description = "A simplified way of solving and understanding backtracking problems."
keywords = []
showfullcontent = false
tags = ["DSA", "backtracking"]
title = "Backtracking problems made easy "

+++
Backtracking problems seems to be one of the tricky part while studying DSA. But once we figure out a pattern in it, then its even easier than array problems.

A general code structure of a backtracking problem solution looks like :
```cpp
    void Backtrack(int start, vector<int>&arr, int &ans)
    {
        //Base case 
    
        for(int i=start; i<arr.size(); i++)
        {
            //include the current element at this position if possible in the ans 
            
            Backtrack(start+1) // here take care whethere to pass start or start+1 dending on the usecase
            
            //backtrack by removing current element 
        }
    }
```
To avoid duplicates in backtracking, we generally sort the array/list, then keep track of the duplicates by `arr[i] == arr[i-1]`.  

Here are some good backtracking problems which makes our understanding about the topic more firm : 

 1.  [Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number)
 2. [Generate Parentheses](https://leetcode.com/problems/generate-parentheses)
 3.  [Sudoku Solver](https://leetcode.com/problems/sudoku-solver)
 4.  [Combination Sum](https://leetcode.com/problems/combination-sum)
 5.  [Combination Sum II](https://leetcode.com/problems/combination-sum-ii)
 6.  [Permutations](https://leetcode.com/problems/permutations)
 7.  [Permutations II](https://leetcode.com/problems/permutations-ii)
 8.  [N-Queens](https://leetcode.com/problems/n-queens)
 9.  [Combinations](https://leetcode.com/problems/combinations)
10.  [Subsets](https://leetcode.com/problems/subsets)
11.  [Subsets II](https://leetcode.com/problems/subsets-ii)
12.  [Restore IP Addresses](https://leetcode.com/problems/restore-ip-addresses)
13.  [Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning)
14.  [Word Break](https://leetcode.com/problems/word-break)
15.  [Combination Sum III](https://leetcode.com/problems/combination-sum-iii)
16.  [Target Sum](https://leetcode.com/problems/target-sum)
17.  [Letter Case Permutation](https://leetcode.com/problems/letter-case-permutation)