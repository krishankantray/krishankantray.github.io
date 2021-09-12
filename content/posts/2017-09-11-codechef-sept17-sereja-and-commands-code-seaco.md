+++
title = "CodeChef SEPT17 Sereja and Commands (code: SEACO) "
slug = "2017-09-11-codechef-sept17-sereja-and-commands-code-seaco"
published = 2017-09-11T20:15:00.003000+05:30
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
style="color: black;">https://www.codechef.com/SEPT17/problems/SEACO</span></span></span>  
  
Sereja has an array **A** consisting of **n** integers. Initially, all
the elements of array are zero.  
Sereja writes down **m** commands on a piece of a paper. The commands
are enumerated from **1** to **m**. These commands can be of the
following two types of commands:  

-   **l r (l ≤ l ≤ r ≤ n)** — Increase all elements of the array by one,
    whose indices belongs to the range **\[l, r\]**
-   **l r (1 ≤ l ≤ r ≤ m)** — Execute all the commands whose indices are
    in the range **\[l, r\]**. It's guaranteed that **r** is strictly
    less than the enumeration/number of the current command.

Can you please help Sereja in executing all the commands written on this
piece of paper.  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Input </span>**</span>  
The first line of the input contains an integer **T** denoting the
number of test cases. The description of **T** test cases follows.  
The first line contains integers **n** and **m**. Next **m** lines
contain Sereja's commands in the format, described in statement: **t**,
**l**, **r**, where **t** - number of type (1 or 2).  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: black;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Output </span>**</span></span></span></span>For each
test case on different lines print an array **a**, after executing all
the commands. The numbers have to be separated by spaces. As the numbers
can be quite large, print them modulo       **10<sup>9</sup> + 7**.  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Constraints
:**</span></span>  
  

-   **1** ≤ **T** ≤ **3**
-   **1** ≤ **n, m** ≤ **10<sup>5</sup>**

<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">**Subtask :**</span></span>

   

-   Subtask #**1** (20 points): 1 ≤ **n, m** ≤ 10
-   Subtask #**2** (30 points): 1 ≤ **n, m** ≤ 1000
-   Subtask #**3** (50 points): original constraints

### <span style="color: red;">Example</span>

    Input:

    3
    5 5
    1 1 2
    1 4 5
    2 1 2
    2 1 3
    2 3 4
    1 2
    1 1 1
    1 1 1
    10 10
    1 1 10
    2 1 1
    2 1 2
    2 1 3
    2 1 4
    2 1 5
    2 1 6
    2 1 7
    2 1 8
    2 1 9

    Output:

    7 7 0 7 7
    2
    512 512 512 512 512 512 512 512 512 512

### <span style="color: red;">Explanation</span>

**Example case 1.**.  
After the first command, the resulting array is \[1 1 0 0 0\], after
second \[1 1 0 1 1\].  
On third command, we repeat the 1'st and the 2'nd command, so that
resulting array is \[2 2 0 2 2\].  
After fourth command, the array will looks like \[4 4 0 4 4\].  
Last command will apply 3'rd and 4'th commands, which by themselves will
apply 1'st, 2'nd, 1'st, 2'nd, 3'rd(1'st, 2'nd), so resulting arrays is
\[7 7 0 7 7\].  
  
**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Solutions
:</span>**</span>**  
  

        #include<iostream>
        #include<vector>
         
        using namespace std;
         
        void incr(int a[], int i, int j)
        {
            for(;i<=j;i++)
                a[i]++;
        }
         
        void comm(int a[],int c[][3], int l, int r)
        {
            for(int i=l; i<=r;i++)
            {
                if(c[i][0]==1)
                    incr(a,c[i][1]-1, c[i][2]-1);
                else
                    comm(a,c,c[i][1]-1, c[i][2]-1);
            }
        }
        int main()
        {
            int t;
            cin>>t;
            while(t--)
            {
                int n,m,temp;
                cin>>n>>m;
                int a[n] ;
                fill_n(a,n,0);
                
                int c[m][3];
                for(int i=0; i<m; i++)
                {
                    cin>>c[i][0];
                    cin>>c[i][1];
                    cin>>c[i][2];
                }
                
                comm(a,c, 0, m-1);
                
                for(int i=0; i<n; i++)
                {
                    cout<<a[i]<<" ";
                }
                cout<<endl;
                    
                
            }
            
                
            return 0;
        }
