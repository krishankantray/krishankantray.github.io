+++
title = "Kadane's Algorithm"
slug = "2020-04-03-kadanes-algorithm"
published = 2020-04-03T06:16:00+05:30
author = "Krishankant Ray"
tags = []
+++
## <span style="color: red;"><span style="font-size: x-large;"><span style="font-family: Verdana, sans-serif;">Kadane's Algorithm</span></span></span>

  
  
TL;DR  
  

-   This algorithm is used to find maximum sum sub-array from a given
    array. 
-   Its has O(n) time complexity and O(1) space complexity.  
-   It works irrespective of whether the elements are positive or
    negative, whether sorted or unsorted. 
-   Its DP approach
-   Its brute force approach takes O(n^2) as it calculates all possible
    sub-array and then return maximum out of them. 

  
  
Since brute force approach is very obvious and easy to implement, so, I
am not discussing it here.  
  

#### Lets directly jump to Kadane's Algorithm : 

  
Its uses two variables one stores local maximum ( <span
style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum
</span></span>) and other stores global maximum ( <span
style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">global\_maximum</span>
</span>) .  
Initialise , <span style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum
= 0 </span></span>and <span style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">global\_maximum</span>
= -Infinity </span>  
  

  
We start iteration from the first element, and for each element we check
following condition before updating the <span
style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum</span></span>
:  

-   if  <span style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum
    &lt; 0</span> </span>,  then <span style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum
    = arr\[i\]</span></span> ,  this is because if <span
    style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum
    </span></span>is negative value then adding it with current value
    will result into lower value.  
    Otherwise, if<span style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">
    local\_maximum >=0 </span></span>then <span
    style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum=
    local\_maximum + arr\[i\]</span></span> .

Now, we got <span style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">local\_maximum
</span></span>till current element, its time to compare it with <span
style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">global\_maximum</span>
</span>. 

 

-   If <span style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">global\_maximum
    &lt; local\_maximum</span></span> then  <span
    style="color: #e69138;"><span
    style="font-family: &quot;Courier New&quot;, Courier, monospace;">global
    maximum = local\_maximum</span></span>              

 

 Thats it, now after whole iteration is finished the our answer is the
value of <span style="color: #e69138;"><span
style="font-family: &quot;Courier New&quot;, Courier, monospace;">global\_maximum</span></span>. 

  

  

 

#### Now, its time to code it out : 

Language used : `JavaScript`

```js

    var maxSubArray = function(nums) {
        var local_maximum=0;
        
        return nums
            .reduce( (global_maximum,current_element)=>{
            
            if(local_maximum <0 ) {
                local_maximum = current_element ;
            }
            else
                local_maximum = local_maximum + current_element ;
            
            global_maximum =  Math.max(global_maximum,local_maximum);
            
            return global_maximum ;
            
        }, -Infinity);
    };
```
  

  

Please read about reduce function in JS if you don't already know about
it.
