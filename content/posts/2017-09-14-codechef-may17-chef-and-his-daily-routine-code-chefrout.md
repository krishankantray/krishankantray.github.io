+++
title = "Codechef MAY17 chef and his daily routine    ( code: CHEFROUT )"
slug = "2017-09-14-codechef-may17-chef-and-his-daily-routine-code-chefrout"
published = 2017-09-14T18:01:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
### <span style="color: red;">Problem </span>: <https://www.codechef.com/problems/CHEFROUT>

Chef's daily routine is very simple. He starts his day with cooking
food, then he eats the food and finally proceeds for sleeping thus
ending his day. Chef carries a robot as his personal assistant whose job
is to log the activities of Chef at various instants during the day.
**Today** it recorded activities that Chef was doing at N different
instants. These instances are recorded in chronological order (in
increasing order of time). This log is provided to you in form of a
string **s** of length N, consisting of characters 'C', 'E' and 'S'. If
**s**\[i\] = 'C', then it means that at the i-th instant Chef was
cooking, 'E' denoting he was eating and 'S' means he was sleeping.  
You have to tell whether the record log made by the robot could possibly
be correct or not.  
  

### <span style="color: red;">Input</span>

The first line of the input contains an integer **T** denoting the
number of test cases. The description of **T** test cases follows.  
The only line of each test case contains string **s**.  

### <span style="color: red;">Output</span>

For each test case, output a single line containing "yes" or "no"
(without quotes) accordingly.  

### <span style="color: red;">Constraints</span>

-   1 ≤ **T** ≤ 20
-   1 ≤ N ≤ 10<sup>5</sup>

### <span style="color: red;">Subtasks</span>

-   **Subtask #1** (40 points) : 1 ≤ N ≤ 100
-   **Subtask #2** (60 points) : original constraints

### <span style="color: red;">Example</span>

    Input:
    5
    CES
    CS
    CCC
    SC
    ECCC

    Output:
    yes
    yes
    yes
    no
    no

### <span style="color: red;">Explanation</span>

**Example case 1.** "CES" can correspond to a possible record of
activities of Chef. He starts the day with cooking, then eating and then
sleeping.  
**Example case 2.** "CS" can also correspond to a possible record of
activities of Chef. He starts the day with cooking, then eating and then
sleeping. Robot recorded his cooking and sleeping in order. He might not
have recorded his eating activity.  
**Example case 4.** "SC" can not correspond to Chef's activities. Here
it means that Chef slept first, then he cooked the food, which is
impossible for Chef to do on some particular day.  
  

### <span style="color: red;">Solution </span>:

###  

    #include <iostream>
    using namespace std;
    int main()
    {
        int t;
        cin >> t;
        while (t--) {
            string s;
            cin >> s;
            bool flag = true;
            for (int i = 1; i < s.length(); i++)
                if (s[i] < s[i - 1]) {
                    flag = false;
                    break;
                }

            if (flag == true)
                cout << "yes" << endl;
            else
                cout << "no" << endl;
        }
        return 0;
    }

### 

###
