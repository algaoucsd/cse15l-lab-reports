# CSE 15L Lab 1 Tutorial: 

## Installing VSCode and Git Bash: 
 >This tutorial assumes you are using a Chromium based browser.
 
 1. Go to this link : [https://code.visualstudio.com/](https://code.visualstudio.com/)
 2. Hit the download button
 3. Next look in the bottom left and click something that looks like this:
 
![image](https://user-images.githubusercontent.com/122490362/211927169-90e6b3bb-197b-4e24-8f03-2cfe448a9444.png)

 4. You can now install VSCode through this installer
 5. Go to this link: [https://git-scm.com/downloads](https://git-scm.com/downloads)
 6. Click the link with your relevant OS (Windows, Mac, or Linux)
 7. Follow the instructions on the page for Mac/Linux, or choose the 32-bit or 64-bit (depends on your system) Standalone Installer if you are using Windows
 
## Connecting to the ENGR Server:

1. Open VSCode
2. Look at the top right and open the Terminal menu, it should look something like this

![image](https://user-images.githubusercontent.com/122490362/211928318-cc1d49af-e923-4512-a88e-753eb5ef876c.png)

3. Click New Terminal
4. In your new terminal type: `ssh CS15LAccount@ieng.ucsd.edu` (replace 'CS15LAccount' with your CS15L account name)
6. It should then ask for your password, enter your password
7. If you don't know your password, follow this guide: [https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit)
8. If you see a message like this, you'll know you've connected:

![image](https://user-images.githubusercontent.com/122490362/211930465-746a7a7e-4d07-4623-b848-0200ea8f25f0.png)

## Trying out Commands:

List of Commands:
```
cd <directory> # replace directory with the path (relative or absolute) to the directory
cd ~
ls 
ls -a
ls -lat
ls <directory> # replace directory with the path (relative or absolute) to the directory
cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
cat /home/linux/ieng6/cs15lwi23/public/hello.txt
```

Above is a list of commands, here will detail a couple of these commands and what they should look like after running.
To use a command, just type them into the terminal and hit enter.

The `ls` and `ls -a` command should look like this:

![image](https://user-images.githubusercontent.com/122490362/211931591-fba9b68f-60cd-48f0-aa3b-1e2794e7f53a.png)

Notice how they are different, that's becuase the `-a` stands or "all", and shows "hidden" files as well.

For the cp command, you should get something like this:

![image](https://user-images.githubusercontent.com/122490362/211931321-ec745c7a-949c-41c0-a5fd-7faad4c88e6a.png)

The cp stands for copy, and it copies a file from the first location, into the second. Notice the "No such file or directory"? That's because there isn't a file called hello.txt in that folder. Use cd and ls to navigate to that directory to see for yourself.

Feel free to try out any other commands on your own!

