+++
title = " A Simple C program to convert DECIMAL to BINARY"
slug = "2017-01-23-a-simple-c-program-to-convert-decimal-to-binary"
published = 2017-01-23T20:21:00.002000+05:30
author = "Krishankant Ray"
tags = []
+++
<u>**<span style="font-family: &quot;verdana&quot; , sans-serif;"><span
style="color: #0070c0; font-size: 14pt;">A Simple C program to convert
DECIMAL to BINARY</span></span>**</u>

  

  

  

<span
style="font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>1<span style="mso-spacerun: yes;"> 
</span><span style="color: #00a000;">#include&lt;iostream></span></span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>2<span style="mso-spacerun: yes;"> 
</span></span><span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">#include&lt;stdio.h></span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>3<span style="mso-spacerun: yes;"> 
</span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">using
namespace </span><span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">std</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>4<span style="mso-spacerun: yes;"> 
</span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">int
</span>**<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">main</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">()</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>5<span style="mso-spacerun: yes;"> 
</span></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">{</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>6<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">int
</span>**<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">,
</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">100</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\]
;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>7<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">int
</span>**<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">0</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">,</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">j</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>8<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">cout</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">&lt;&lt;</span><span
style="color: blue; font-family: &quot;courier new&quot;; font-size: 12.0pt;">"Enter
the decimal number ---><span style="mso-spacerun: yes;">  </span>"
</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;"><span
style="mso-spacerun: yes;"> </span>9<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">cin</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">&gt;&gt;</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">10<span
style="mso-spacerun: yes;">      </span></span><span
style="color: #bebee6; font-family: &quot;courier new&quot;; font-size: 12.0pt;">//
using while loop to store in arr\[\]</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">11<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">while</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">(
(</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">/</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">2</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">)
&gt;=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">1</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">)</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">12<span
style="mso-spacerun: yes;">      </span></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">{</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">13<span
style="mso-spacerun: yes;">          </span>arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">++\]=
(</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">%</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">2</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">);</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">14<span
style="mso-spacerun: yes;">          </span>n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">=</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">/</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">2</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">15<span
style="mso-spacerun: yes;">      </span></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">}</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">16<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">if</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">(</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">==</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">3</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">)</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">17<span
style="mso-spacerun: yes;">      </span></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">{</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">18<span
style="mso-spacerun: yes;">          </span>arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">++\]=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">1</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">19<span
style="mso-spacerun: yes;">          </span>arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\]=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">1</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">20<span
style="mso-spacerun: yes;">      </span></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">}</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">21<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">else
if</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">(</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">==</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">2</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">)</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">22<span
style="mso-spacerun: yes;">          </span>arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\]=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">0</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">23<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">else
if</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">(</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">n</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">==</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">1</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">)</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">24<span
style="mso-spacerun: yes;">          </span>arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\]=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">1</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">25<span
style="mso-spacerun: yes;">  </span></span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">26<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">cout</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">&lt;&lt;</span>**<span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">endl
</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">27<span
style="mso-spacerun: yes;">      </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">for</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">(</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">j</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">=</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">i</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">j</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">&gt;=</span><span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">0</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">j</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">--)</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">28<span
style="mso-spacerun: yes;">          </span></span>**<span
style="color: #00a000; font-family: &quot;courier new&quot;; font-size: 12.0pt;">cout</span>**<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">&lt;&lt;</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">arr</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\[</span><span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">j</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">\];</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">29<span
style="mso-spacerun: yes;">  </span></span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt;">30<span
style="mso-spacerun: yes;">  </span></span>**<span
style="color: #0000a0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">return
</span>**<span
style="color: #f000f0; font-family: &quot;courier new&quot;; font-size: 12.0pt;">0</span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt;">;</span>

<span
style="color: black; font-family: &quot;courier new&quot;; font-size: 12.0pt; line-height: 107%;">31<span
style="mso-spacerun: yes;">  </span></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt; line-height: 107%;">}</span>  
  
  
<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt; line-height: 107%;"></span>  
<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt; line-height: 107%;">**<u><span
style="color: #0070c0; font-family: &quot;berlin sans fb demi&quot; , &quot;sans-serif&quot;; font-size: 14.0pt; line-height: 107%;">OUTPUT</span></u>**
</span>  
<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt; line-height: 107%;"></span>  
<span
style="color: red; font-family: &quot;courier new&quot;; font-size: 12.0pt; line-height: 107%;"><span
style="color: magenta;"><u>**<span
style="font-family: &quot;berlin sans fb demi&quot; , &quot;sans-serif&quot;; font-size: 14pt; line-height: 107%;"></span>**</u></span>**<span
style="color: #0070c0; font-family: &quot;berlin sans fb demi&quot; , &quot;sans-serif&quot;; font-size: 14.0pt; line-height: 107%;"></span>**<u>**<span
style="color: #0070c0; font-family: &quot;berlin sans fb demi&quot; , &quot;sans-serif&quot;; font-size: 14.0pt; line-height: 107%;"></span><span
style="color: #0070c0; font-family: &quot;berlin sans fb demi&quot; , &quot;sans-serif&quot;; font-size: 14.0pt; line-height: 107%;"></span>**</u>
</span>

[![](../images/thumbnails/2017-01-23-a-simple-c-program-to-convert-decimal-to-binary-Capture.JPG)](../images/2017-01-23-a-simple-c-program-to-convert-decimal-to-binary-Capture.JPG)

<span style="mso-no-proof: yes;"></span><span
style="color: red; font-family: &quot;courier new&quot;; font-size: 8.0pt;"></span>
