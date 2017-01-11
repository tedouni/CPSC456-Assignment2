Tayseer Edouni | taedouni@gmail.com

Part II implemented correctly.

Was developed on Ubuntu 14.04.
run as "python binder.py /bin/ls /bin/pwd"


Extra Credit:
None

Part I:
 Try opening the file using the 7-zip program.
 What happens?  Are you able to extract and run the worm.bat file inside the archive?

A:When opening the archive I only see the worm.bat file in the archive (not the gif).
I was able to extrct and run the worm.bat file however it does not work on the virtual machine because it was
coded to user Mike and there is no user Mike on this virtual machine (which works out good so that it does not hang the virtual machine).




 Repeat the above steps, but this time rename the file to result.gif extension.Try opening the file. What happens?

A:When the file result is changed to result.gif you can open the gif but the worm won't run. However if you then change the extension
to .7z (at the and of the filename but keep .gif in filename) the file can still be opened with internet explorer on the system to view the gif
but you can also right click on the file and open archive using 7z and are able to run the worm.




 Explain what is happening. Do some research in order to find out what the above copy
command does. In your explanation be sure to explain the role of each argument in the
above command. Also, be sure to explain how Windows handles files which leads to the
above behavior. Include the answers to these questions in the README file you submit.

A: The /B flag of the copy command treats the files as binary. It copies them byte for byte instead of
the default /a flag (text mode) which treats them as lines of text and copies until it reaches the EOF character.
In our case worm.7z and fileName.gif files are the source files and are copied byte for byte to the  result file
(which is the destination).

http://superuser.com/questions/453245/what-exactly-happens-when-you-use-the-copy-b-command
https://en.wikipedia.org/wiki/Copy_(command)


How can this technique be used for hiding malicious codes?

A: This technique can be useful for transporting malware from one system to another.
If malware is hidden within a gif image, a security ignorant individual may fall victim to the malware.
A popular method in the early 2000s was for attackers to hide malware in a file that looked like an mp3 file of a
popular song and was shared on p2p applications such as Kazaa. When trying to e-mail myself the result.7z file, gmail (my fullerton e-mail)
blocked the attachment however it allowed the result.gif file. By default windows hides the extension of files so attackers may use this
to exploit novice computer users.

How robust is this technique in terms of avoiding detection by anti-virus tools? You may
need to do some research.

A: Anti-Virus tools tend to compare signatures. If this is a targeted attack then it can possibly avoid detection (if the payload/malware is custom written for the target). But if this is a well
known malware/virus that already exist in database of anti-virus tools then it is not a good technique to avoid detection.
