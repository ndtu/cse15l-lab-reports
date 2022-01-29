# **Lab Report #1**

Part 1: Installing VScode: 
To begin with, start by downloading and installing visual studio code. To do so, click on this link:  https://code.visualstudio.com/
Follow the instructions that correspond with your major operating systems. Once installed, open VSC and your page should look like this:
![image](https://user-images.githubusercontent.com/77379218/149480135-48e50113-7783-4717-844f-c45394f3f98b.png)

Part 2: Remotely Connecting:
After installing visual studio code, install a program called OpenSSH and read through the instructions. It will allow you to connect with other computers.
The link to installing OpenSSH is here: https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse
Then, look up your account here and change your password: https://sdacs.ucsd.edu/~icc/index.php
After that, open a new terminal in visual studio code and enter this: ssh cs15lwi22zz@ieng6.ucsd.edu. However, the two "zz" are the letters in your account.
Then press yes and enter your new password. You should get this: 

![image](https://user-images.githubusercontent.com/77379218/149487077-8bf832ef-f6c7-441f-adca-6780afb3095a.png)

Part 3: Run Some Commands:
Try running some commands. Here are a few commands that you can run: 
![image](https://user-images.githubusercontent.com/77379218/149595060-684ed030-ae05-4c60-a600-d9ec4ebb6777.png)

Part 4: Moving Files over SSH with scp:
Now, on visual studio code, create a whereAmI.java file with this content:
![image](https://user-images.githubusercontent.com/77379218/149595809-d76d0939-471f-4587-b83e-c8fb984b2a56.png)
Then, use this scp command in order to move a file to SSH. SCP command:
![image](https://user-images.githubusercontent.com/77379218/149594932-8ae32d61-9747-4d7f-8005-821b7017a4d8.png)


Part 5: SSH keys:
Now, there is a way to shorten the process of logging in and copying files to a remote server with SSH and SCP, and it is with SSH keys
In your terminal, run ssh-keygen. Your set up should look like this: 
![image](https://user-images.githubusercontent.com/77379218/149594265-4eeb6bc6-c72d-48a6-a5ce-dec101875110.png)

Part 6: Making Remote Running Even More Pleasant:
Now, try to use what you have learned in order to make an local edit to the whereAmI.java file in the most efficient way, and then run it in the remote server.
This is a hint:
![image](https://user-images.githubusercontent.com/77379218/149596019-12a62d00-19d8-431e-9e09-3cc8215f3ec9.png)
Adding quotations at the end of a command to run it in the remote server.
Now, in order to make it run in the most efficient way, first, enter this in your terminal: ssh cs15lwi22aov@ieng6.ucsd.edu "ls"
Enter your password and run it on your remote server. Now, try running multiple commands in a single line in order to make a local edit to WhereAmI.java, and
 then copying it to the remote server and running it. Doing this allows you to only enter your password a single time and not every time you wished to make an edit, and 
 by creating multiple commands on a single line allows you to making a local edit to your file, copy it to the remote server and run it at the same time. The commands are: 
 scp WhereAmI.java; ssh cse15lwizz@ieng.ucsd.edu;(zz are the letters in your course-specific account) javac WhereAmI.java; java WhereAmI. Make sure to put these commands all in a single line and to use semi colons to space the commands out.
