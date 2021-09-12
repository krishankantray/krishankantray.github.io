+++
title = "CodeChef (AUG17 LunchTime) : Mathison and pangrams - MATPAN"
slug = "2017-08-30-codechef-aug17-lunchtime-mathison-and-pangrams-matpan"
published = 2017-08-30T21:10:00+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Problem: Mathison
and pangrams</span>**</span>  
  
Mathison recently inherited an ancient papyrus that contained some text.
Unfortunately, the text was not a **pangram**. Now, Mathison has a
particular liking for holoalphabetic strings and the text bothers him.
The good news is that Mathison can buy letters from the local store in
order to turn his text into a pangram.  
However, each letter has a price and Mathison is not very rich. Can you
help Mathison find the cheapest way to obtain a pangram?  
  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Input </span>**</span>  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">  
</span>**</span>The first line of the input file will contain one
integer, **T**, representing the number of tests.  
  
Each test will be formed from two lines. The first one contains **26**
space-separated integers, representing the prices of all letters. The
second will contain Mathison's initial text (a string of **N** lowercase
letters).  
  
<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Output </span>**</span>  
  
The output file will contain **T** lines, one for each test. Each line
will contain the answer for the corresponding test.  
  
<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">**Constraints
:**</span></span>  
  

-   1 ≤ **T** ≤ 10
-   1 ≤ **N** ≤ 50,000
-   All prices are natural numbers between 1 and 1,000,000 (i.e.
    10<sup>6</sup>).
-   A pangram is a string that contains every letter of the Latin
    alphabet at least once.
-   All purchased letters are added to the end of the string

  

<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">**Subtask :**</span></span>

<u>**Subtask #1**</u> (30 points):  

-   **N** = 1

<u>**Subtask #2**</u> (70 points):  

-   Original constraints

  

  

### <span style="color: red;">Example</span>

    Input:
    2
    1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26
    abcdefghijklmopqrstuvwz
    1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26
    thequickbrownfoxjumpsoverthelazydog

    Output:
    63
    0 

     

     

### <span style="color: red;">Explanation</span>

First test There are three letters missing from the original string: n
(price 14), x (price 24), and y (price 25). Therefore the answer is 14 +
24 + 25 = **63**. 

Second test No letter is missing so there is no point in buying
something. The answer is **0.**

**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Solutions
:</span>**</span>**

    *
    https://www.codechef.com/problems/MATPAN
     */
    #include <iostream>
    #include <vector>
    using namespace std;
    int main()
    {
        int t;
        cin >> t;
        while (t--) {
            char x = 'a';
            vector<char> alpha;
            vector<int> cost(26);
            for (int i = 1; i <= 25; i++) {
                alpha.push_back(x);
                x = x + 1;
            }
            alpha.push_back(x);
            //-----------------------------------
            for (int i = 0; i < 26; i++)
                cin >> cost[i];
            string s;
            cin >> s;
            for (int i = 0; i < s.length(); i++) {
                for (int j = 0; j < 26; j++)
                    if (s[i] == alpha[j] && alpha[j] != '0')
                        alpha[j] = '0';
            }
            int sum = 0;
            for (int i = 0; i < 26; i++) {
                if (alpha[i] != '0')
                    sum += cost[i];
            }
            cout << sum << endl;
        }

        return 0;
    }

**<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;"> </span>**</span> **
