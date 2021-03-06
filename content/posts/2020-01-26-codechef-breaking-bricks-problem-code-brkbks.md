+++
title = "CodeChef : Breaking Bricks ||  Problem Code: BRKBKS"
slug = "2020-01-26-codechef-breaking-bricks-problem-code-brkbks"
published = 2020-01-26T01:14:00+05:30
author = "Krishankant Ray"
tags = []
+++
CodeChef : <https://www.codechef.com/JAN20B/problems/BRKBKS>  
  
  
**Problem:** 
For her next karate demonstration, Ada will break some bricks.  
  
Ada stacked three bricks on top of each other. Initially, their widths
(from top to bottom) are W1,W2,W3.  
  
Ada's strength is S. Whenever she hits a stack of bricks, consider the
largest k≥0 such that the sum of widths of the topmost k bricks does not
exceed S; the topmost k bricks break and are removed from the stack.
Before each hit, Ada may also decide to reverse the current stack of
bricks, with no cost.  
  
Find the minimum number of hits Ada needs in order to break all bricks
if she performs the reversals optimally. You are not required to
minimise the number of reversals.</span>  

**Input**

- The first line of the input contains a single integer T denoting the number of test cases. The description of T test cases follows.

-   The first and only line of each test case contains four space-separated integers S, W1, W2 and W3.

**Output**

For each test case, print a single line containing one integer ― the minimum
required number of hits.

**Constraints**

-   1≤T≤64
-   1≤S≤8
-   1≤Wi≤2
    for each valid i
-   1≤Wi≤2
    for each valid i  
     
It is guaranteed that Ada can break all bricks
  
  

**Example**

Input : 
```
3
3 1 2 2
2 1 1 1
3 2 2 1
```
Output :
```

2
2
2
    
```


**Example Explanation :**

Example case 1: Ada can reverse the stack and then hit it two times.
Before the first hit, the widths of bricks in the stack (from top to
bottom) are (2,2,1). After the first hit, the topmost brick breaks and
the stack becomes (2,1). The second hit breaks both remaining bricks.  
  
In this particular case, it is also possible to hit the stack two times
without reversing. Before the first hit, it is (1,2,2). The first hit
breaks the two bricks at the top (so the stack becomes (2)) and the
second hit breaks the last brick.  
  

**Solution :**

This looks like a bit trivial problem of super easy category.And the logic is also too simple. All we need to do is that just think it in three parts, when Ada has enough strength to break all three blocks at a single hit, or in two hits or in three hits. There is no more than three hits needed
because we know that the number of blocks in fixed to three. 


Here is the C++ code for the problem :  

```cpp
#include <bits/stdc++.h>


using namespace std;

int main() {

  int t;

  cin >> t;

  int s;

  vector < int > w(3);

  while (t--) {

    cin >> s >> w[0] >> w[1] >> w[2];

    if (s >= 6) {

      cout << 1 << endl;

      continue;

    }

    if (w[0] + w[1] + w[2] <= s) {

      cout << 1 << endl;

    } else if ((w[0] + w[1] <= s) || (w[1] + w[2] <= s))

    {

      cout << 2 << endl;

    } else cout << 3 << endl;

  }

  return 0;

}
```
