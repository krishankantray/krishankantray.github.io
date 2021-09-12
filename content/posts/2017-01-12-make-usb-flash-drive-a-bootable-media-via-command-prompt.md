+++
title = "Make USB flash drive a bootable media via Command Prompt"
slug = "2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt"
published = 2017-01-12T20:01:00.001000+05:30
author = "Krishankant Ray"
tags = []
+++
## <span style="background-color: #444444;"><span style="color: white;">**Follow the following steps :-**</span></span>

---------------------------------------------------------------------------------------------------------------  
Step I :  Open command prompt as administrator  
                 
     
[![](../images/thumbnails/2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt-step1.jpg)](../images/2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt-step1.jpg)  
Step II: Type "**diskpart**" and hit enter  
Step III: Type "**list disk**" and then press enter.  
Step III: Check the disk number of you USB drive. ( in example it is  1
)  

[![](../images/thumbnails/2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt-Step2.jpg)](../images/2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt-Step2.jpg)

Step IV: Now, type "**select disk 1**" and then hit enter ( remember
here 1 is the disk number)  
Step V: \`Now type "**clean**" and hit enter.  
Step VI: Type "**create partition primary**" and hit enter.  
Step VII: Type "**select partition 1**" and hit enter. ( here 1 is not
the disk number, whatever is your  
                 disk number you have to write 1).  
Step VIII: Type "**format fs=ntfs quick**" and then hit enter.  
Step IX: Type "**active**" and hit enter.  
Step X: Now, type "**exit**" or just close the command prompt.  
Step XI: Just copy the files from Windows OS DVD to your USB flash
drive.  

[![](../images/thumbnails/2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt-step3.jpg)](../images/2017-01-12-make-usb-flash-drive-a-bootable-media-via-command-prompt-step3.jpg)

Step XII: Restart your computer and set your boot menu to boot via
USB.  
Step XIII: Thats all, you are done, your can install windows OS to your
computer.
