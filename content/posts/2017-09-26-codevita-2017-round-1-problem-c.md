+++
title = "Codevita 2017 Round-1 Problem-C"
slug = "2017-09-26-codevita-2017-round-1-problem-c"
published = 2017-09-26T20:20:00+05:30
author = "Krishankant Ray"
tags = []
+++
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"></span>**<span
style="font-family: Verdana,sans-serif;">Problem:</span>**</span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-size: x-small;"><span style="color: black;">CodeVita 2017
Round 1 Problem -C</span></span></span></span>  
<span style="color: red;"><span
style="font-family: Verdana,sans-serif;"><span
style="font-size: x-small;"><span style="color: black;">(download from
below ...  if any problem in downloading then
comment) </span></span></span>**<span
style="font-family: Verdana,sans-serif;"> </span>**</span>  
<span style="color: red;">**<span
style="font-family: Verdana,sans-serif;"><http://s000.tinyupload.com/?file_id=52952119059621072275></span>**</span>  
  
<span style="color: red;">**<span
style="font-family: Verdana,sans-serif;">Solution</span>**</span>:  

    /*
     Author: Krishankant Ray
     * CodeVita 2017 Round 1
     */

    #include<iostream>
    #include<vector>

    using namespace std;
    int main()
    {
        int d,k=0;
        string arr;
        cin>>d;
        cin>>arr;
        int n=arr.length();
        char R[n];

        for(int f=0; f<n; )
        {

            R[f]=arr[k++];

            f+=((2*d)-2);
        }
        for(int i=1; i<d-1;i++)
        {
            R[i]=arr[k++];
            for(int j=i; j<n;)
            {

                j+=((2*d)-2-(2*i));
                R[j]=arr[k++];

                j+=((2*i));
                if(j<n)
                R[j]=arr[k++];

            }
        }

        for(int l=d-1; l<n;l+=((2*d)-2))
        {
            R[l]=arr[k++];

        }
        for(int f=0; f<n;f++)
        {
            if(R[f]=='X')
                break;
            else
            cout<<R[f];
        }

        return 0;
    }
