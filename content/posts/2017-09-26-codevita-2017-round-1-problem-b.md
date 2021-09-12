+++
title = "CodeVita 2017 Round-1 Problem-B"
slug = "2017-09-26-codevita-2017-round-1-problem-b"
published = 2017-09-26T19:47:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;"><span
style="color: red;">**Problem :**</span> Concatenating
primes</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
If you like numbers, you may have been fascinated by prime numbers.
Sometimes we obtain by concatenating two primes. For  
example, concatenating 2 and 3, we obtain the prime 23. The aim is to
find all such distinct "concatenated primes" that could  
be obtained by concatenating primes ≤ a given integer N.  
 </span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;"><span
style="color: red;">**Input Format:**</span>  
 </span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">Integer
N</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
<span style="color: red;">**Output
Format:**</span></span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
M, the number of distinct primes that could be obtained by concatenating
two primes ≤ N</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
<span
style="color: red;">**Constraints:**</span></span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
N ≤ 70</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
Example 1</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
Input  
10  
Output  
4</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
Explanations</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
The primes ≤ 10 are 2, 3, 5, 7. These can be used to form the following
concatenated numbers: 22, 23, 25, 27, 32, 33, 35, 37,  
52, 53, 55, 57, 72, 73, 75, 77. Of these, there are four primes: 23 37
53 and 73. Hence the output is 4.</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
Example 2  
Input  
20  
Output  
17</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
**<span
style="color: red;">Explanation</span>**</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
The prime numbers up to 20 are 2 3 5 7 11 13 17 and 19.  
Concatenating these two at a time in all possible ways, we get the
following numbers:  
22 23 25 27 211 213 217 219  
32 33 35 37 311 313 317 319  
52 53 55 57 511 513 517 519  
72 73 75 77 711 713 717 719  
112 113 115 117 1111 1113 1117 1119  
132 133 135 137 1311 1313 1317 1319  
172 173 175 177 1711 1713 1717 1719  
192 193 195 197 1911 1913 1917 1919  
We have the following 17 primes numbers in this list: 23 37 53 73 113
137 173 193 197 211 311 313 317 719 1117 1319  
1913 Hence the output would be 17.</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
Note:</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-family: inherit;"><span style="color: black;">  
Please do not use package and namespace in your code. For object
oriented languages your code should be written in one  
class.  
Note:  
Participants submitting solutions in C language should not use functions
from &lt;conio.h> / &lt;process.h> as these files do not  
exist in gcc  
Note:  
For C and C++, return type of main() function should be int.  
A B C D E F</span></span></span>**<span
style="font-family: Verdana,sans-serif;"></span>**</span>  
<span style="color: red;">**<span
style="font-family: Verdana,sans-serif;"> </span>**</span>  
  
<span style="color: red;">**<span
style="font-family: Verdana,sans-serif;">Solution:</span>**</span>  
<span style="color: red;">**<span
style="font-family: Verdana,sans-serif;">  
</span>**</span>  

    #include<iostream>
    #include<vector>
    #include<cmath>
    #include<set>

    using namespace std;
    int checkprime(int x)
    {
        int i=2;
        while(i<=sqrt(x))
        {
            if(x%i==0)
                return 0;
            i++;
        }
        return 1;
    }
    int main()
    {
        int N,temp;
        
        cin>>N;
        vector<int>prime;
        set<int>conc;
        if(N>1)
        {
            for(int i=2;i<=N;i++)
               if(checkprime(i) == 1)
                   prime.push_back(i);
            
            for(int i =0; i<prime.size();i++)
            {
                for(int j=0; j<prime.size();j++)
                {
                    if(int(prime[j]/10)==0)
                    {
                        temp=prime[i]*10+prime[j];
                        if(checkprime(temp)==1)
                        conc.insert(temp);
                    }
                    else if(int(prime[j]/10)!=0 && int(prime[j]/100)==0)
                    {
                        temp=prime[i]*100+prime[j];
                        if(checkprime(temp)==1)
                        conc.insert(temp);
                    }
                }
            }
        }
        
       
        cout<<conc.size();
        
        return 0;
    }

<span style="color: red;">**<span
style="font-family: Verdana,sans-serif;"></span>**</span>
