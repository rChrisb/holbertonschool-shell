![image](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-sysadmin_devops/205/image.jpg)
# <p align=center >`Shell, basics`</p>
## <p align=center> `Project's obejectives` </p>
Be able to explain:
- What does RTFM mean?
- What is a Shebang
- What is the shell
- What is the difference between a terminal and a shell
- What is the shell prompt
- How to use the history (the basics)
- What do the commands or built-ins cd, pwd, ls do
- How to navigate the filesystem
- What are the . and .. directories
- What is the working directory, how to print it and how to change it
- What is the root directory
- What is the home directory, and how to go there
- What is the difference between the root directory and the home directory of the user root
- What are the characteristics of hidden files and how to list them
- What does the command cd - do
- What do the commands ls, less, file do
- How do you use options and arguments with commands
- Understand the ls long format and how to display it
- A Guided Tour
- What does the ln command do
- What do you find in the most common/important directories
- What is a symbolic link
- What is a hard link
- What is the difference between a hard link and a symbolic link
- What do the commands cp, mv, rm, mkdir do
- What are wildcards and how do they work
- How to use wildcards
- What do type, which, help, man commands do
- What are the different kinds of commands
- What is an alias
- When do you use the command help instead of man
- How to read a man page
- What are man page sections
- What are the section numbers for User commands, System calls and Library functions
- Common shortcuts for Bash
- What does LTS mean?
## <p align=center >`Resources`</p>
Read or watch:
- [What Is “The Shell”?](https://intranet.hbtn.io/rltoken/aygkrwOyI_yLtXHF1Yj0QQ)
- [Navigation](https://intranet.hbtn.io/rltoken/fMDkg3TKjANJSPTROMQSpA)
- [Looking Around](https://intranet.hbtn.io/rltoken/isPTWCOgTjeLaonZg8Rl5g)
- [A Guided Tour](https://intranet.hbtn.io/rltoken/GznRkhU3QTWAWwDeZ-k9Pw)
- [Manipulating Files](https://intranet.hbtn.io/rltoken/GA2UvOhDOjwa-NtbazvlCQ)
- [Working With Commands](https://intranet.hbtn.io/rltoken/ylGnKaanTSp3jIpXme9krg)
- [Reading Man pages](https://intranet.hbtn.io/rltoken/52aXMywgSkXV07rFrX8eWw)
- [Keyboard shortcuts for Bash](https://intranet.hbtn.io/rltoken/XXe2AD3TVWvNFwSP5_-YWQ)
- [LTS](https://wiki.ubuntu.com/LTS)
- [Shebang](https://intranet.hbtn.io/rltoken/_pJ5Fl2TaZVzW3jJy_mwKA)

## <p align=center>`Tasks`</p>
### <p align=center>`0. Where am I?`</p>
Write a script that prints the absolute path name of the current working directory.
Example:
```bash
$ ./0-current_working_directory
/0x00-shell_basics
$
```
--------------------------------------------------
### <p align=center>`1. What’s in there?`</p>
Display the contents list of your current directory.
```bash
Example:

$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```
--------------------------------------------------
### <p align=center>`2. There is no place like home`</p>
Write a script that changes the working directory to the user’s home directory.

- You are not allowed to use any shell variables
--------------------------------------------------
### <p align=center>`3. The long format`</p>
Display current directory contents in a long format

Example:
```bash
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$
```
--------------------------------------------------
### <p align=center>`4. Hidden files`</p>
Display current directory contents, including hidden files (starting with .). Use the long format.

Example:
```bash
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
```
--------------------------------------------------
### <p align=center>`5. I love numbers`</p>
Display current directory contents.

- Long format
- with user and group IDs displayed numerically
- And hidden files (starting with .)
Example:
```bash
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$
```
--------------------------------------------------
### <p align=center>`6. Welcome`</p>
Create a script that creates a directory named my_first_directory in the /tmp/ directory.
```bash
Example:

$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```
--------------------------------------------------
### <p align=center>`7. Betty in my first directory`</p>
Move the file betty from /tmp/ to /tmp/my_first_directory.

Example:
```bash
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```
--------------------------------------------------
### <p align=center>`8. Bye bye Betty`</p>
Delete the file betty.

- The file betty is in /tmp/my_first_directory
Example:
```bash
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```
--------------------------------------------------
### <p align=center>`9. Bye bye My first directory`</p>
Delete the directory my_first_directory that is in the /tmp directory.

Example:
```bash
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```
--------------------------------------------------
### <p align=center>`10. Back to the future`</p>

--------------------------------------------------
### <p align=center>`11. Lists`</p>

--------------------------------------------------
### <p align=center>`12. File type`</p>

--------------------------------------------------
### <p align=center>`13. We are symbols, and inhabit symbols`</p>

--------------------------------------------------
### <p align=center>`14. Copy HTML files`</p>

--------------------------------------------------
### <p align=center>`15. Let’s move`</p>

--------------------------------------------------
### <p align=center>`16. Clean Emacs`</p>

--------------------------------------------------
### <p align=center>`17. Tree`</p>

--------------------------------------------------






## <p align=right>`Score: 100/100`</p>
