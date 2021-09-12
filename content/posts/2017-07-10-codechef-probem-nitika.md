+++
title = "Codechef Probem : NITIKA"
slug = "2017-07-10-codechef-probem-nitika"
published = 2017-07-10T12:24:00.001000+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Problem
:**</span></span> Link: (
[https://www.codechef.com/JULY17/problems/NITIKA
)](https://www.codechef.com/JULY17/problems/NITIKA)  
  
<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Nitika
was once reading a history book and wanted to analyze it. So she asked
her brother to create a list of names of the various famous
personalities in the book. Her brother gave Nitika the list. Nitika was
furious when she saw the list. The names of the people were not properly
formatted. She doesn't like this and would like to properly format
it.</span>  
<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">
</span><span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">A name can
have at most three parts: first name, middle name and last name. It will
have at least one part. The last name is always present. The rules of
formatting a name are very simple: </span>  

-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">**Only**
    the first letter of each part of the name should be capital.</span>
-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">All the
    parts of the name except the last part should be represented by only
    two characters. The first character should be the first letter of
    the part and should be capitalized. The second character should be
    ".".</span>

<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">
</span><span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Let us look
at some examples of formatting according to these rules:</span>  
<span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;"></span>  

-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">gandhi
    -> Gandhi </span>
-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">mahatma
    gandhI -> M. Gandhi </span>
-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Mohndas
    KaramChand ganDhi -> M. K. Gandhi.</span>

  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Input
:</span>**</span>  
  
<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">The
first line of the input contains an integer **T** denoting the number of
test cases.</span>  
<span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;"></span><span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">The only
line of each test case contains the space separated parts of the
name.</span>  
  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Output
:</span>**</span>  
  
<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">For
each case, output the properly formatted name.</span>  
  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Constraint
:</span>**</span>  
  

-   <span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">1
    ≤ **T** ≤ 100</span>
-   <span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">2
    ≤ Length of each part of the name ≤ 10</span>
-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Each
    part of the name contains the letters from lower and upper case
    English alphabets (i.e. from 'a' to 'z', or 'A' to 'Z')</span>

  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Subtask
:</span>**</span>  
  
<span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">**Subtask #1
(40 points)**</span>  

-   <span
    style="font-family: &quot;trebuchet ms&quot; , sans-serif;">There is
    exactly one part in the name.</span>

<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">
</span><span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">**Subtask #2
(60 points)**</span>  
<span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Original
constraints</span>  
  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Example
:</span>**</span>  
  

    Input:
    3
    gandhi
    mahatma gandhI
    Mohndas KaramChand gandhi

    Output:
    Gandhi 
    M. Gandhi 
    M. K. Gandhi 

     

     

  
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------  
  
**<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">Solution</span></span>** <span
style="color: #999999;">*(in C++)*</span> :  
  
  

    #include <iostream>
    #include <string>
    #include <cctype>
    using namespace std;
    int main()
    {
        int t;
        cin >> t;
        cin.ignore();
        while (t--) {
            string s;

            getline(cin, s);

            int x = 0;
            for (int i = 0; i < s.length(); i++) {

                if (s[i] == ' ') {

                    s[x] = toupper(s[x]);
                    x++;
                    s[x] = '.';
                    x++;

                    while (s[x] != ' ') {
                        s.erase(x, 1);
                    }
                    i = x;

                    x++;
                }
            }

            s[x] = toupper(s[x]);
            x++;

            for (int k = x; k < s.length(); k++) {
                s[k] = tolower(s[k]);
            }

            cout << s << endl;
        }
        return 0;
    }
