+++
title = "HackerRank(greedy): Minimum Absolute Difference in an Array"
slug = "2017-10-22-hackerrank-greedy-minimum-absolute-difference-in-an-array"
published = 2017-10-22T16:15:00.001000+05:30
author = "Krishankant Ray"
tags = []
+++

**Problem:**

Consider an array of integers, A = a0, a1, a2....an-1. We define the [absolute
difference](https://en.wikipedia.org/wiki/Absolute_difference) between
two elements, ai and aj  
(where ai not equal to aj ), to be the [absolute value](https://en.wikipedia.org/wiki/Absolute_value)
of ai-aj.

Given an array of n integers, find and print the minimum absolute difference between any two elements in the array.  

**Input Format**

The first line contains a single integer denoting  (the number of integers).  
The second line contains space-separated integers describing the respective values of a0, a1....an-1 .

**Constraints**
- 2 <= n <= 10^5
- -10^9 <= ai <= 10^9

**Output Format**

Print the minimum absolute difference between any two elements in the array.

**Sample Input 0**
```
3
3 -7 0
```

**Sample Output 0**

```
3
```
 
  
**Solutions:**
Note: Simple O(n^2) solution won't work because of
time constraints. So, use this below O(N logN) solution which uses
sorting the array first, then uses O(N) to compare adjacent
differences.
  
***
```cpp

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <climits>
using namespace std;

int main() {
    int n;
    long long min = INT_MAX;
    cin>>n;
    vector<long long>arr(n);
    for(int i=0; i<n; i++)
    cin>>arr[i];
    sort(arr.begin(), arr.end());
    for(int i=0;i<n-1;i++)
    if(min>abs(arr[i]-arr[i+1]))
    min=abs(arr[i]-arr[i+1]);
    cout<<min;
    return 0;
}

```