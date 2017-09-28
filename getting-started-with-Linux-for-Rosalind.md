# Intro To Linux and the Rosalind HPC
--------------------------------------
The Linux and the command line may seem like a daunting undertaking initially, but with some practice and these basic commands, you should be able to navigate through Rosalind like a pro!  


**1.  Where Am I?! -- The 'pwd' command**
--------------------------------------
When you first log into Rosalind it will automatically place you in your home directory. The phrase yourUsername should be replaced with your Rosalind username. You can verify this by typing 'pwd', which stands for present working directory on the command prompt as follows:

```
[yourUsername@cubipmlgn01 ~]$ pwd
```
The output should look like this and then give you a new command prompt:
```
/homelink/yourUsername
[yourUsername@cubipmlgn01 ~]$
```


**2.  Changing Directories -- The 'cd' command**
-------------------------------------------------
Your home directory has very limited space and can only be viewed by you the user and nobody else. Therefore this space should never be used to upload data or for sharing files with other members within your project group.  Typically, this should only be used to store very small files that only you the user needs or for installing specific software or storing small reference files.  Instead, let's change directories into your shared project space on Rosalind.  The phrase "yourProject" should be replaced with the exact name of the project you are approved for on Rosalind and remember, Linux is **ALWAYS CASE SENSITIVE!**
```
[yourUsername@cubipmlgn01 ~]$ cd /gpfs/share/yourProject
```
To confirm this, you can use the pwd command from above to ensure you are now in your designated project space:
```
[yourUsername@cubipmlgn01 ~]$ pwd
/gpfs/share/yourProject
[yourUsername@cubipmlgn01 ~]$
```
The 'cd' command can also regonize a very useful shortcut.  If you want to move up one directory/folder you can use **..**  For example if you type in the following:
```
[yourUsername@cubipmlgn01 ~]$ cd ..
```
you will now have moved up one level.  To confirm this, if you type in the pwd command, you should now see the following:
```
[yourUsername@cubipmlgn01 ~]$ pwd
/gpfs/share
[yourUsername@cubipmlgn01 ~]$
```
To change directories back into your project, you can type the following:
```
[yourUsername@cubipmlgn01 ~]$ cd yourProject
```


**3.  Make a new directory (folder) -- The 'mkdir' command**
------------------------------------------------------------
Now that you are in your project directory you have the ability to create new folders, or in Linux we all them directories. Let's make a new folder called 'Rosalind_Demo'.
```
[yourUsername@cubipmlgn01 ~]$ mkdir Rosalind_Demo
[yourUsername@cubipmlgn01 ~]$
```
You have now successfully created a directory called Rosalind_Demo.  You may be wondering how you can tell...well let's move to the next step.  


**4.  List all items in a directory -- The 'ls' command**
----------------------------------------------------------
The ls command is one of your best friends when using the command line.  ls stands for list segements, and any time you call it, it will list all the items in your present working directory.  For example type the following:
```
[yourUsername@cubipmlgn01 ~]$ ls
```
It should return the following (assuming you followed the directions above):
```
Rosalind_Demo
[yourUsername@cubipmlgn01 ~]$
```
If you have other files or directories in this directory it will list those as well.  Additionally ls has multiple options you can add following the ls command.  One of which that is particular useful is **-lh**  This means long format and human readable.  For example, type in the following:
```
[yourUsername@cubipmlgn01 ~]$ ls -lh
```
You should see something similar to the following:
drwx------  2 yourUsername groupOwnership 4.0K Sep 28 14:13 Rosalind_Demo
```
The first chunk of drwx------ tell you the directory or file permissions. The 4.0K tells you the size of the directory(note, this is a little confusing because all directories are 4.0K no matter what is in them) or file (the h in -lh makes it so that the size is humann readable i.e. KB, MG, GB) isteady of in bytes).  The date and time following the size is the date the file/directory was last modified.



The first letter, 'd', indicates that Rosalind_Demo is a directory.  The remaining letters specify which users and groups have access to the directory Rosalind_Demo.  Since you created this directory, by default you also own the directory, therefore, the 'rwx', following the 'd' indicate that you have the ability to read/open Rosalind_Demo (the r), you also have write/modify access (the w), and you have the ability to execute or move into the Rosalind_Demo directory (the x). 
