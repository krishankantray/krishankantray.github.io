+++
title = "Codechef - Courses in an university - Problem Code: UNICOURS"
slug = "2017-09-14-codechef-courses-in-an-university-problem-code-unicours"
published = 2017-09-14T23:39:00.001000+05:30
author = "Krishankant Ray"
tags = []
+++
### <span style="color: red;">Problem</span>

  
There are **n** courses in a university being offered. These courses are
numbered from 1 to **n** in the increasing order of their difficulty.
For each course, you can have some courses as prerequisites. The
prerequisite courses for a course should be of lower difficulty than it.
You are given an array **a** of size **n**, where **a**<sub>i</sub>
denotes that there should be at least **a**<sub>i</sub> prerequisite
courses for i-th course.  
The university wants to estimate the efficiency of the allocation of
prerequisites of courses by maximizing the number of courses that are
not prerequisites for any other course. Find out what's the maximum such
number of courses possible. It is guaranteed that **a**<sub>i</sub> &lt;
i, thus making sure that it is possible to allocate the prerequisites
for each of the course.  

### <span style="color: red;">Input</span>

The first line of the input contains an integer **T** denoting the
number of test cases. The description of **T** test cases follows.  
The first line of each test case contains an integer **n**.  
The second line of each test case contains **n** space separated
integers denoting array **a**.  

### <span style="color: red;">Output</span>

For each test case, output a single line containing an integer
corresponding to the maximum number of possible courses which are not
prerequisite for any other course.  

### <span style="color: red;">Constraints</span>

-   **1** ≤ **T** ≤ **10**
-   1 ≤ **n** ≤ 10<sup>5</sup>
-   0 ≤ **a**<sub>i</sub> &lt; i

### <span style="color: red;">Subtasks</span>

-   **Subtask #1** (40 points) : 1 ≤ **n** ≤ 100
-   **Subtask #2** (60 points) : original constraints

### <span style="color: red;">Example</span>

    Input:
    2
    3
    0 1 1
    3
    0 1 2

    Output:
    2
    1 

     

     

### <span style="color: red;">Solution :</span>

### <span style="color: red;"> </span>

###  

    #include<iostream>
    #include<climits>
    using namespace std;
    int main()
    {
        int t;
        cin>>t;
        while(t--)
        {
            int n,max=INT_MIN;
            cin>>n;
            int A[n];
            for(int i=0; i<n; i++)
            {
                cin>>A[i];
                if(A[i]>max)
                    max=A[i];
            }
            
            cout<<(n-max)<<endl;
        }  
        return 0;
    }

### <span style="color: red;"></span>
