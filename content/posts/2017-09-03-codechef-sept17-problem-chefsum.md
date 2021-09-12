+++
title = "CodeChef SEPT17   Problem: CHEFSUM"
slug = "2017-09-03-codechef-sept17-problem-chefsum"
published = 2017-09-03T22:52:00.003000+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Problem: Little
Chef and Sums</span>**</span>  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">  
</span>**</span>  
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
  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Output </span>**</span>  
  
For each test case, output a single line containing the answer.  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Constraints
:**</span></span>  
  

-   **1** ≤ **T** ≤ **10**
-   **1** ≤ **N, A\[i\]** ≤ **10<sup>5</sup>**

**<sup><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">**Subtask\ :**</span></span></sup>**  
  

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

     

### <span style="color: red;"> </span>

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
style="font-family: &quot;verdana&quot; , sans-serif;">Solutions
:</span>**</span>**

<span style="background-color: #6aa84f;"><span
style="color: #cccccc;"><span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: black;">// will update
soon</span></span></span></span></span>**<span
style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">
</span>**</span>**

  

### <span style="color: red;"> </span>

  
**<sup><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">** **</span></span></sup>**  

<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">** **</span></span>  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;"> </span>**</span>  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"></span>**</span>
