+++
title = "HackerRank Problem : Reverse and capitalise first alphabet of each word."
slug = "2017-07-06-hackerrank-problem-reverse-and-capitalise-first-alphabet-of-each-word"
published = 2017-07-06T22:36:00.004000+05:30
author = "Krishankant Ray"
tags = []
+++
* *<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Problem : </span>**<span style="color: red;"><span
style="color: black;">(</span></span></span><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;"><span style="color: black;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;"><span style="color: #93c47d;"><span
style="font-size: x-small;">*Link :*</span> </span></span></span><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: #274e13;"><span style="font-size: x-small;">[Click here to
visit this problem on
HackerRank.](https://www.hackerrank.com/contests/codejam/challenges/reverse-words/problem)
</span></span></span></span></span></span><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;"><span style="color: black;"><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: #274e13;"><span style="font-size: x-small;">[<span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">)</span></span>](https://www.hackerrank.com/contests/codejam/challenges/reverse-words/problem)
</span></span></span></span></span>**<span
style="color: red;"></span>**</span>  
<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: red;">  
</span></span><span
style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: #274e13;"></span>**<span style="color: red;">
</span>**</span>*<span style="background-color: #f9cb9c;"> </span>*  
<span
style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Reverse the
words in a string and capitalize the first letter of each reversed word,
preserving the capitalization in the original stri. For eg: "Hello
World" would be transformed to "OlleH DlroW".</span>  
  

<span style="font-family: &quot;verdana&quot; , sans-serif;">**<span
style="color: red;">Input :</span>**</span>

  

<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">The
first line of input would be the number of test cases followed by each
string in a line.</span>  

  

**<span style="color: red;"><span
style="font-family: &quot;verdana&quot; , sans-serif;">Output
:</span></span>**

  
<span style="font-family: &quot;trebuchet ms&quot; , sans-serif;">Output
should be the string with each word reversed and first letter of each
reversed word capitalized. Each output string should be printed to a new
line.</span>  

<table style="height: 123px; width: 403px;">
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><table style="height: 111px; width: 475px;">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
  <span style="color: red;">Sample Input<span style="background-color: white;"><span class="problem-item-gray"></span></span></span></td>
<td><br />
<span style="color: red;"><span class="problem-item-gray">Sample Output</span></span></td>
</tr>
<tr class="even">
<td><pre><code>1
Hello World</code></pre></td>
<td><pre><code>OlleH DlroW</code></pre></td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><br />
</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------  
  
<span style="color: red;">**<span
style="font-family: &quot;verdana&quot; , sans-serif;">Solution :
</span>**</span>*<span style="color: #3d85c6;">( in C++ )</span>*  
  
<span style="font-family: &quot;consolas&quot;;"><span
style="color: magenta;">#include</span> <span
style="color: #996600;">&lt;iostream></span>  
<span style="color: magenta;">#include</span> <span
style="color: #996600;">&lt;string></span>  
<span style="color: magenta;">#include</span> <span
style="color: #996600;">&lt;algorithm></span>  
<span style="color: magenta;">#include</span> <span
style="color: #996600;">&lt;cctype></span>  
<span style="color: green;">using</span> <span
style="color: #9933ff;">namespace</span> <span
style="color: green;">std</span>;  
<span style="color: green;">int</span> <span
style="color: blue;">main</span>()  
{  
    <span style="color: green;">int</span> <span
style="color: blue;">x</span>;  
    cin >&gt; x;  
  
    <span style="color: #9933ff;">for</span> (<span
style="color: green;">int</span> <span
style="color: blue;">i</span> = 0; <span
style="color: green;">i</span> &lt; <span
style="color: blue;">x</span>; i++) {  
        <span style="color: green;">string</span> <span
style="color: blue;">line</span>;  
        getline(cin, line);</span><span
style="font-family: &quot;consolas&quot;;"><span
style="font-family: &quot;consolas&quot;;"><span
style="color: brown;">*  *</span></span></span>  

<span style="font-family: &quot;consolas&quot;;"><span
style="font-family: &quot;consolas&quot;;"><span
style="color: brown;">*                  /\* this is required to*
</span></span></span><span
style="font-family: &quot;consolas&quot;;"><span
style="font-family: &quot;consolas&quot;;"><span
style="color: brown;">*<span
style="font-family: &quot;consolas&quot;;"><span
style="font-family: &quot;consolas&quot;;"><span
style="color: brown;">*eliminate* </span></span></span>trailing
whitespaces created due to  endline character of
cin>&gt; *</span></span></span>

<span style="font-family: &quot;consolas&quot;;"><span
style="font-family: &quot;consolas&quot;;"><span
style="color: brown;">*\*/*</span></span>     </span>

<span style="font-family: &quot;consolas&quot;;">        </span>  
<span style="font-family: &quot;consolas&quot;;">       
getline(cin, line);  
  
        <span
style="color: brown;">*//loop for reversing words*</span>  
        <span style="color: green;">int</span> <span
style="color: blue;">j</span> = 0;  
        <span style="color: #9933ff;">for</span> (<span
style="color: green;">int</span> <span
style="color: blue;">i</span> = 0; <span
style="color: green;">i</span> &lt;= <span
style="color: blue;">line</span>.length(); i++)  
            <span
style="color: #9933ff;">if</span> (line\[i\] == ' ' || line\[i\] == '\\0') {  
  
                reverse(line.begin() + j, line.begin() + i);  
                line\[j\] = toupper(line\[j\]);  
                j = i + 1;  
            }  
  
        cout &lt;&lt; line &lt;&lt; endl;  
    }  
    <span style="color: #9933ff;">return</span> 0;  
}</span>
