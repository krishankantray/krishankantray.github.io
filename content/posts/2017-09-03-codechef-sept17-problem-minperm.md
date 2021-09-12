+++
title = "CodeChef SEPT17  Problem: MINPERM"
slug = "2017-09-03-codechef-sept17-problem-minperm"
published = 2017-09-03T23:01:00+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Problem:Minimum
Good Permutation</span>**</span>  
  
A permutation of length **n** is an array of size **n** consisting of
**n** **distinct** integers in the range **\[1, n\]**. For example, (3,
2, 4, 1) is a permutation of length 4, but (3, 3, 1, 4) and (2, 3, 4, 5)
are not, as (3, 3, 1, 4) contains duplicate elements, and (2, 3, 4, 5)
contains elements not in range \[1,4\].  
A permutation **p** of length **n** is *good* if and only if for any
**1** ≤ **i** ≤ **n**, **p<sub>i</sub>** ≠ **i**.  
Please find the **lexicographically** smallest *good* permutation
**p**.  
**Definition for "lexicographically smaller**":  
For two permutations **p** and **q**, we say that **p** is
lexicographically smaller than **q** if and only if there exists a index
**1** ≤ **l** ≤ **n** such that:  

-   For any **1** ≤ **i** &lt; **l**, **p<sub>i</sub>** =
    **q<sub>i</sub>**. Note that if **l** = **1**, this constraint means
    nothing.
-   and, **p<sub>l</sub>** &lt; **q<sub>l</sub>**.

For example, (2, 3, 1, 4) &lt; (2, 3, 4, 1) &lt; (3, 4, 1, 2). The
lexicographically smallest permutation is, of course, (1, 2, ...,
**n**), though this one is not *good*.  
  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Input </span>**</span>  
First line of the input contains an integer **T** denoting number of
test cases.  
For each test case, the only line contains an integer **n**.  
  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Output </span>**</span>  
For each test case, output the lexicographically smallest *good*
permutation of length **n**. It's guaranteed that this permutation
exists  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Constraints
:**</span></span>  
  

-   **1** ≤ **T** ≤ **10**
-   **2** ≤ **n** ≤ **10<sup>5</sup>**

<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">**Subtask :**</span></span>

-   **Subtask #1 (17 points)**: **2** ≤ **n** ≤ **9**
-   **Subtask #2 (83 points)**: Original Constraints

### <span style="color: red;">Example</span>

    Input:
    4
    2
    3
    5
    6

    Output:
    2 1
    2 3 1
    2 1 4 5 3
    2 1 4 3 6 5

### <span style="color: red;"> </span>

  

### <span style="color: red;">Explanation</span>

**Example case 1.** The only *good* permutation of length 2 is (2, 1).  
**Example case 2. **Consider all permutations of length 3, they are(in
lexicographically order):  

-   p = (1, 2, 3), it's not good since p\[1\] = 1, p\[2\] = 2 and p\[3\]
    = 3;
-   p = (1, 3, 2), it's not good since p\[1\] = 1;
-   p = (2, 1, 3), it's not good since p\[3\] = 3;
-   p = (2, 3, 1), it's good since p\[1\] ≠ 1, p\[2\] ≠ 2 and p\[3\] ≠
    3;
-   p = (3, 1, 2), it's good since p\[1\] ≠ 1, p\[2\] ≠ 2 and p\[3\] ≠
    3;
-   p = (3, 2, 1), it's not good since p\[2\] = 2.

Thus the minimum good one is (2, 3, 1).  
**Example case 3.** Consider two good permutations for third test case:
p=(2, 1, 4, 5, 3) and q=(2, 4, 1, 5, 3), then p &lt; q. You can check
lexicographically condition as follows. Find the first index where the
entries of two permutations are different, and compare those entries.
For example, in this case, the first position where the entries differ
is index 2. You can see that p\[2\] &lt; q\[2\], as 1 &lt; 4, so p is
lexicographically smaller than q.  
  
  
**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Solutions
:</span>**</span>**  
  
  
  

###   <span style="color: red;"> </span>

    #include<iostream>
    using namespace std;
    int main()
    {
        int t;
        cin>>t;
        while(t--)
        {
            int n,temp;
            cin>>n;
            int arr[n];
            for(int i=0; i<n; i++)
                arr[i]=i+1;
            for(int i=1; i<n; i+=2)
            {
                if(arr[i] == i+1)
                {
                    temp = arr[i];
                    arr[i]=arr[i-1];
                    arr[i-1]=temp;
                }
            }
             for(int i=1; i<n; i++)
            {
                if(arr[i] == i+1)
                {
                    temp = arr[i];
                    arr[i]=arr[i-1];
                    arr[i-1]=temp;
                }
            } 
            for(int i=0 ;i<n;i++)
                cout<<arr[i]<<" ";
            cout<<endl;
        }
        return 0;
    } 

**<sup> </sup>**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">** **</span></span>  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;"> </span>**</span>  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"></span>**</span>
