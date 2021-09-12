+++
title = "TCS Code Vita 6 ( problem-B )"
slug = "2017-07-31-tcs-code-vita-6-problem-b"
published = 2017-07-31T21:03:00+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;">**Problem : Concatenating
primes**</span></span>  
  
If you like numbers, you may have been fascinated by prime numbers.
Sometimes we obtain by concatenating two primes. For example,
concatenating 2 and 3, we obtain the prime 23. The aim is to find all
such distinct "concatenated primes" that could be obtained by
concatenating primes ≤ a given integer N.  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;">**  
Input Format:**</span></span>  
  
Integer N  
  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;">**Output
Format**</span></span>:  
  
M, the number of distinct primes that could be obtained by concatenating
two primes ≤ N  
Constraints:  
N ≤ 70  
  
<u>**Example 1**</u>  
<span style="color: yellow;">Input  
10  
Output  
4</span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;">** **</span></span>  
<u><span style="font-family: inherit;">**Explanations**</span></u>  
The primes ≤ 10 are 2, 3, 5, 7. These can be used to form the following
concatenated numbers: 22, 23, 25, 27, 32, 33, 35, 37,  
52, 53, 55, 57, 72, 73, 75, 77. Of these, there are four primes: 23 37
53 and 73. Hence the output is 4.  
  
<u>**Example 2**</u>  
  
<span style="color: yellow;">Input  
20  
Output  
17</span>  
  
<u>**Explanation**</u>  
  
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
137 173 193 197 211 311 313 317 719 1117 1319 1913 .  
Hence the output would be **17**.  
  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;">**Solution:**</span></span>  
  
  

    #include <iostream>
    #include <vector>
    int checkprime(int n)
    {

        for (int i = 2; i < n; i++)
            if (n % i == 0)
                return 0;
        return 1;
    }

    int main()
    {
        int N, temp, count = 0;
        std::vector<int> primes;
        std::cin >> N;
        if (N > 2) { // ----------------------------------------------

            primes.push_back(2);
            primes.push_back(3);

            for (int i = 4; i <= N; i++) {
                if (checkprime(i) == 1)
                    primes.push_back(i);
            }

            for (std::vector<double>::size_type i = 0; i < primes.size(); i++) {
                for (std::vector<double>::size_type j = 0; j < primes.size(); j++) {

                    if (primes[j] < 10)
                        temp = 10 * primes[i] + primes[j];
                    else
                        temp = 100 * primes[i] + primes[j];
                    if (checkprime(temp) == 1) {
                        count++;
                    }
                }

            } //------------------------------------------------------
            std::cout << count << std::endl;
            for (std::vector<double>::size_type i = 0; i < primes.size(); i++)
                std::cout << "  " << primes[i];
        }

        else if (N <= 2)
            std::cout << 0;

        return 0;
    }
