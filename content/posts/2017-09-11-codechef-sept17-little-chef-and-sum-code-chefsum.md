+++
title = "CodeChef SEPT17 Little Chef and Sum ( code: CHEFSUM)"
slug = "2017-09-11-codechef-sept17-little-chef-and-sum-code-chefsum"
published = 2017-09-11T19:59:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Problem: Little
Chef and Sum </span>**</span>  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">  
</span>**</span><span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: black;">https://www.codechef.com/SEPT17/problems/CHEFSUM</span></span></span>  
  
Our little chef is fond of doing additions/sums in his free time. Today,
he has an array **A** consisting of **N** positive integers and he will
compute prefix and suffix sums over this array.  
He first defines two functions **prefixSum(i)** and **suffixSum(i)** for
the array as follows. The function **prefixSum(i)** denotes the sum of
first **i** numbers of the array. Similarly, he defines **suffixSum(i)**
as the sum of last **N - i + 1** numbers of the array.  
Little Chef is interested in finding the minimum index **i** for which
the value **prefixSum(i) + suffixSum(i)** is the minimum. In other
words, first you should minimize the value of **prefixSum(i) +
suffixSum(i)**, and then find the least index **i** for which this value
is attained.  
Since, he is very busy preparing the dishes for the guests, can you help
him solve this problem?  
  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Input </span>**</span>  
The first line of the input contains an integer **T** denoting the
number of test cases.  
The first line of each test case contains a single integer **N**
denoting the number of integers in the array **A**.  
The second line contains **N** space-separated integers
**A<sub>1</sub>**, **A<sub>2</sub>**, ..., **A<sub>N</sub>** denoting
the array **A**.  
  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: black;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Output </span>**</span>  
</span></span></span>For each test case, output a single line containing
the answer.  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Constraints
:**</span></span>  
  
  

-   **1** ≤ **T** ≤ **10**
-   **1** ≤ **N, A\[i\]** ≤ **10<sup>5</sup>**

<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">**Subtask :**</span></span>

  **<sup>  
</sup>**

-   **Subtask #1 : (20 points)** **1 ≤ N ≤ 100**
-   **Subtask #2 : (80 points)** Original constraints

### <span style="color: red;">Example</span>

    Input:
    2
    3
    1 2 3
    4
    2 1 3 1

    Output:

 

    1
    2

     

     

### <span style="color: red;">Explanation</span>

**Example case 1.** Let's calculate prefixSum(i) + suffixSum(i) for all
indexes **i** in the sample case.  

    prefixSum(1) + suffixSum(1) = 1 + 6 = 7
    prefixSum(2) + suffixSum(2) = 3 + 5 = 8
    prefixSum(3) + suffixSum(3) = 6 + 3 = 9

The minimum value of the function is 7, which is attained at index 1, so
the answer would be 1.  
**Example case 2.** Let's calculate prefixSum(i) + suffixSum(i) for all
indexes **i** in the sample case.  

    prefixSum(1) + suffixSum(1) = 2 + 7 = 9
    prefixSum(2) + suffixSum(2) = 3 + 5 = 8
    prefixSum(3) + suffixSum(3) = 6 + 4 = 10
    prefixSum(4) + suffixSum(4) = 7 + 1 = 8

The minimum value of the function is 8, which is achieved for indices 2
and 4. The minimum of these two indices 2, 4 is index 2. Hence, the
answer will be 2.  
  
**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Solutions :<span
style="background-color: #6aa84f;"><span style="color: #cccccc;"><span
style="color: #999999;"><span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"></span></span></span></span></span></span>**</span>**  
**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="background-color: #6aa84f;"><span style="color: #cccccc;"><span
style="color: #999999;"><span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: black;"></span></span></span></span></span></span> </span>**</span>**  

     #include <iostream>
    #include <climits>
    using namespace std;
    int main()
    {
        int t;
        cin >> t;
        while (t--) {
            int N, sum = 0, pos = INT_MAX;
            int small = INT_MAX;
            cin >> N;
            int arr[N];
            for (int i = 0; i < N; i++) {
                cin >> arr[i];
                if (arr[i] < small) {
                    small = arr[i];
                    pos = i;
                }
            }
            cout << pos + 1 << endl;
        }
        return 0;
    }

  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"></span>**</span>  
  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"> </span>**</span>
