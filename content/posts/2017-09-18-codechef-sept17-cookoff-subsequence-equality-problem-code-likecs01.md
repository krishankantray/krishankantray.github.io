+++
title = "Codechef SEPT17 CookOff - Subsequence Equality Problem Code: LIKECS01"
slug = "2017-09-18-codechef-sept17-cookoff-subsequence-equality-problem-code-likecs01"
published = 2017-09-18T00:46:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
### <span style="color: red;">Problem:</span> (Link: <https://www.codechef.com/problems/LIKECS01> )

Chef Tobby is playing a rapid fire with Bhuvan. He gives Bhuvan a string
**S** and each time, Bhuvan has to guess whether there exists **2**
equal [subsequences](https://en.wikipedia.org/wiki/Subsequence) in the
string or not.  
Bhuvan got a perfect score in the game with Chef Tobby. However, Chef
Tobby has now asked Bhuvan to write a program that will do this
automatically given a string **S**. Bhuvan is an intelligent man but he
does not know how to write a code. Can you help him?  
Find two different subsequences such that they are equal in their value,
more formally, find two sequences of indices (a<sub>1</sub>,
a<sub>2</sub>, ..., a<sub>k-1</sub>, a<sub>k</sub>) and (b<sub>1</sub>,
b<sub>2</sub>, ..., b<sub>k-1</sub>, b<sub>k</sub>) such that:  

1.  1≤ a<sub>i</sub>, b<sub>i</sub> ≤ |S|
2.  a<sub>i</sub> &lt; a<sub>i+1</sub> for all valid i
3.  b<sub>i</sub> &lt; b<sub>i+1</sub> for all valid i
4.  S<sub>a<sub>i</sub></sub> = S<sub>b<sub>i</sub></sub> for all valid
    i
5.  there exist at least one i such that a<sub>i</sub> is not equal to
    b<sub>i</sub>

### <span style="color: red;">Input section</span>

The first line contains **T**, the number of test cases.  
Each of the next **T** lines contain one string **S** each.  
**Input will only consist of lowercase english characters**  
  

### <span style="color: red;">Output section</span>

For each test case, output **"yes"** or **"no"** (without quotes) as the
solution to the problem.  

### <span style="color: red;">Input constraints</span>

    1 ≤ T ≤ 1000
    1 ≤ length of S ≤ 100

### <span style="color: red;">Sample Input</span>

    4
    likecs
    venivedivici
    bhuvan
    codechef

### <span style="color: red;">Sample Output</span>

    no
    yes
    no
    yes

### <span style="color: red;">Explanation</span>

In test case **2**, one of the possible equal subsequence is **"vi"**
and **"vi"**. (one at position **{0, 3}** and other at **{4, 7}**,
assuming 0-based indexing).  
In test case **4**, one of the possible equal subsequence is **"ce"**
and **"ce"**. (one at position **{0, 3}** and other at **{4, 6}**,
assuming 0-based indexing).  
  
  

### <span style="color: red;">Solution :</span>

### 

### 

    #include <iostream>
    #include <set>
    using namespace std;
    int main()
    {
        int t;
        cin >> t;
        while (t--) {
            set<char> st;
            string s;
            cin >> s;
            for (int i = 0; i < s.length(); i++)
                st.insert(s[i]);
            if (st.size() == s.length())
                cout << "no" << endl;
            else
                cout << "yes" << endl;
        }

        return 0;
    }
