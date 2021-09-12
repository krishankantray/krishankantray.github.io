+++
title = "TCS-Codevita 2017 Round-1  Problem-A"
slug = "2017-09-26-tcs-codevita-2017-round-1-problem-a"
published = 2017-09-26T19:39:00.001000+05:30
author = "Krishankant Ray"
tags = []
+++
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Problem :
</span></span>**Mountain peak sequence  
  
Consider the first three natural numbers 1, 2, 3. These can be arranged
in the following ways: 2, 3, 1 and 1, 3, 2. Inboth of  
these arrangements, the numbers increase to a certain point and then
decrease. A sequence with this property is called a  
"mountain peak sequence".  
Given an integer N, write a program to find the remainder of mountain
peak arrangements that can be obtained by rearranging  
the numbers 1, 2, ...., N.  
  
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Input
Format:</span></span>**  
  
One line containing the integer N  
  
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Output
Format:</span></span>**  
  
An integer m, giving the remainder of the number of mountain peak
arrangements that could be obtained from 1, 2, ...., N is  
divide by Mod  
  
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Constraints</span></span>**:  
  
Mod = 109+7  
N ≤ 109  
  
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Example
1</span></span>**  
  
Input  
3  
Output  
2  
Explanation  
There are two such arrangements: 1, 3, 2 and 2, 3, 1  
  
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Example
2</span></span>**  
  
Input  
4  
Output  
6  
Explanation  
The six arrangements are (1, 2, 4, 3), (1,3,4,2), (1,4,3,2), (2,3,4,1),
(2,4,3,1), (3,4,2,1)  
  
  
**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Note:</span></span>**  
  
Please do not use package and namespace in your code. For object
oriented languages your code should be written in one  
class.  
Note:  
Participants submitting solutions in C language should not use functions
from &lt;conio.h> / &lt;process.h> as these files do not  
exist in gcc  
Note:  
For C and C++, return type of main() function should be int.  
<span style="font-size: xx-small;">© 2017 Tata Consultancy Services
Limited. All Rights Reserved.</span>  
  
<span style="font-size: xx-small;"> </span>**<span
style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Solution:</span></span>**  
  

    /*
     * CODEvita  2017 problem-A
     * Author: krishankantray
     */
    #include<iostream>
    #include<algorithm>
    #include<vector>
    using namespace std;
    int min(int a,int b)
    {
        return a>b?a:b ;
    }
    int bino(int  n,int  r,int p)
    {
        vector<int>C(r+1,0);
        C[0]=1;
        for(int i=1;i<=n;i++ )
        {
            for(int j=min(i,r);j>0;j--)
                C[j]=(C[j] + C[j-1])%p;

        }
        return C[r];
    }
    int main()
    {
        int N,m=0;
        int mod;
        mod= 1000000007;
        cin>>N;
        for(int i=1;i<N-1;i++)
            m+=bino(N-1,i,mod);
        cout<<(m%mod);
        return 0;
    }
