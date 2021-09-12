+++
title = "CodeChef SEPT17 Chef and Pick Digit (code: CHEFPDIG)"
slug = "2017-09-11-codechef-sept17-chef-and-pick-digit-code-chefpdig"
published = 2017-09-11T20:07:00+05:30
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
style="color: black;">https://www.codechef.com/SEPT17/problems/CHEFPDIG</span></span></span>  
  
Chef likes to play with big numbers. Today, he has a big positive
integer **N**. He can select any two digits from this number (the digits
can be same but their positions should be different) and orders them in
any one of the two possible ways. For each of these ways, he creates a
two digit number from it (might contain leading zeros). Then, he will
pick a character corresponding to the ASCII value equal to this number,
i.e. the number 65 corresponds to 'A', 66 to 'B' and so on till 90 for
'Z'. Chef is only interested in finding which of the characters in the
range 'A' to 'Z' can possibly be picked this way. <span
style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Input </span>**</span>  
The first line of the input contains an integer **T** denoting the
number of test cases.  
The first line of the input contains an integer **N**.  
  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: black;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Output </span>**</span>  
</span></span></span>For each test case, output a string containing
characters Chef can pick **in sorted order** If the resulting size of
string is zero, you should output a new line.  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Constraints
:**</span></span>  
  
  

-   **1** ≤ **T** ≤ **10**
-   **1** ≤ **N** ≤ **10<sup>100000</sup>**

<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">**Subtask :**</span></span>

   

-   *Subtask #1 (40 points)* **N** ≤ **10<sup>10</sup>**
-   *Subtask #2 (60 points)* **Original Constraints**

### <span style="color: red;">Example</span>

    Input:
    4
    65
    566
    11
    1623455078

    Output:

    A
    AB

    ACDFGHIJKLNPQRSTUVW

### <span style="color: red;">Explanation</span>

  
**Example case 1.** Chef can pick digits **6** and **5** and create
integers 56 and 65. The integer 65 corresponds to 'A'.  
**Example case 2.** Chef can pick digits **6** and **5** and create
**'A'** as it equals **65**. He can pick 6 and 6 (they are picked from
position 2 and position 3, respectively) to create 'B' too. Hence answer
is "AB".  
**Example case 3.** It's not possible to create any character from 'A'
to 'Z'. Hence, we just print a new line.  
  
**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Solutions
:</span>**</span>**  
  

    #include<iostream>
    #include<vector>
    #include<algorithm>
    #include<iterator>
    using namespace std;
     
    int main()
    {
        int t;
        cin>>t;
        while(t--)
        {
            long long unsigned int n,x;
            cin>>n;
            x=n;
            vector<int>nums;
            vector<char>alpha;
            while(x !=0)
            {
                int a = x%10;
                nums.push_back(a);
                x /=10;
            }
            
            int p = nums.size();
            for(int i=0; i<p; i++)
            {
                for(int j=0; j<p ;j++)
                {
                    if(j != i)
                    {
                        int b = 10*nums[i] + nums[j];
                        char c = b;
                        if(b>=65 && b<=90)
                            alpha.push_back(c);
                        b= 10*nums[j] + nums[i];
                        c= b;
                        if(b>=65 && b<=90)
                            alpha.push_back(c);
                    }
                }
            }
            
            sort(alpha.begin(), alpha.end());
            vector<char>::iterator it;
            it = unique(alpha.begin(), alpha.end());
            alpha.resize(distance(alpha.begin(), it));
        for(int i=0; i<alpha.size(); i++)
            cout<<alpha[i];
            cout<<endl;
        }
        
        
        
        return 0;
    }

**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"> </span>**</span>**
