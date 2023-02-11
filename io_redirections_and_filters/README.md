<p align=center >
<img width = 60% src = "https://linuxhint.com/wp-content/uploads/2021/08/Input-Output-Redirection-in-Ubuntu.jpg" </>
  
  # <p align=center >`Shell, I/O Redirections and filters`</p>
## <p align=center> `Project's obejectives` </p>
Be able to explain:
- What do the commands head, tail, find, wc, sort, uniq, grep, tr do
- How to redirect standard output to a file
- How to get standard input from a file instead of the keyboard
- How to send the output from one program to the input of another program
- How to combine commands and filters with redirections
- What are special characters
- Understand what do the white spaces, single quotes, double quotes, backslash, comment, pipe, command separator, tilde and how and when to use them
- How to display a line of text
- How to concatenate files and print on the standard output
- How to reverse a string
- How to remove sections from each line of files
- What is the /etc/passwd file and what is its format
- What is the /etc/shadow file and what is its format
## <p align=center >`Resources`</p>
Read or watch:
- [Shell, I/O Redirection](https://intranet.hbtn.io/rltoken/dJRc-mwT3vNw7SCWZNlGcg)
- [Special Characters](https://intranet.hbtn.io/rltoken/k2EzFVxAXrpfJMvl8-1ukQ)

## <p align=center>`Tasks`</p>
### <p align=center>`0. Hello World`</p>
Write a script that prints “Hello, World”, followed by a new line to the standard output.

-------------------------------------------------------------------
### <p align=center>`1. Confused smiley`</p>

Write a script that displays a confused smiley "(Ôo)'.

-------------------------------------------------------------------
### <p align=center>`2. Let's display a file`</p>
Display the content of the /etc/passwd file.

Example:
```bash
$ ./2-hellofile
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico
_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false
_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false
_installassistant:*:25:25:Install Assistant:/var/empty:/usr/bin/false
_lp:*:26:26:Printing Services:/var/spool/cups:/usr/bin/false
_postfix:*:27:27:Postfix Mail Server:/var/spool/postfix:/usr/bin/false
_scsd:*:31:31:Service Configuration Service:/var/empty:/usr/bin/false
_ces:*:32:32:Certificate Enrollment Service:/var/empty:/usr/bin/false
_mcxalr:*:54:54:MCX AppLaunch:/var/empty:/usr/bin/false
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false
$
```
-------------------------------------------------------------------
### <p align=center>`3. What about 2?`</p>
Display the content of /etc/passwd and /etc/hosts

Example:
```bash
$ ./3-twofiles
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting. Do not change this entry.
##
127.0.0.1   localhost
255.255.255.255 broadcasthost
::1 localhost
$
```
-------------------------------------------------------------------
### <p align=center>`4. Last lines of a file`</p>
Display the last 10 lines of /etc/passwd

Example:
```bash
$ ./4-lastlines
_assetcache:*:235:235:Asset Cache Service:/var/empty:/usr/bin/false
_coremediaiod:*:236:236:Core Media IO Daemon:/var/empty:/usr/bin/false
_launchservicesd:*:239:239:_launchservicesd:/var/empty:/usr/bin/false
_iconservices:*:240:240:IconServices:/var/empty:/usr/bin/false
_distnote:*:241:241:DistNote:/var/empty:/usr/bin/false
_nsurlsessiond:*:242:242:NSURLSession Daemon:/var/db/nsurlsessiond:/usr/bin/false
_nsurlstoraged:*:243:243:NSURLStorage Daemon:/var/empty:/usr/bin/false
_displaypolicyd:*:244:244:Display Policy Daemon:/var/empty:/usr/bin/false
_astris:*:245:245:Astris Services:/var/db/astris:/usr/bin/false
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false
```
-------------------------------------------------------------------
### <p align=center>`5. I'd prefer the first ones actually`</p>
Display the first 10 lines of /etc/passwd

Example:
```bash
$ ./5-firstlines
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
$
```
-------------------------------------------------------------------
### <p align=center>`6. Line #2`</p>
Write a script that displays the third line of the file iacta.

The file iacta will be in the working directory
-------------------------------------------------------------------
### <p align=center>`7. It is a good file that cuts iron without making a noise`</p>

Write a shell script that creates a file named exactly `\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)` containing the text `Best School` ending by a new line.

-------------------------------------------------------------------
### <p align=center>`8. Save current state of directory`</p>
Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.

-------------------------------------------------------------------
### <p align=center>`9. Duplicate last line`</p>
Write a script that duplicates the last line of the file iacta

- The file iacta will be in the working directory
-------------------------------------------------------------------
### <p align=center>`10. No more javascript`</p>
Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.

-------------------------------------------------------------------
### <p align=center>`11. Don't just count your directories, make your directories count`</p>
Write a script that counts the number of directories and sub-directories in the current directory.

- The current and parent directories should not be taken into account
- Hidden directories should be counted
-------------------------------------------------------------------
### <p align=center>`12. What’s new`</p>
Create a script that displays the 10 newest files in the current directory.

Requirements:

- One file per line
- Sorted from the newest to the oldest
-------------------------------------------------------------------
### <p align=center>`13. Being unique is better than being perfect`</p>
Create a script that takes a list of words as input and prints only words that appear exactly once.

- Input format: One line, one word
- Output format: One line, one word
- Words should be sorted
-------------------------------------------------------------------
### <p align=center>`14. It must be in that file`</p>
Display lines containing the pattern “root” from the file /etc/passwd

-------------------------------------------------------------------
### <p align=center>`15. Count that word`</p>
Display the number of lines that contain the pattern “bin” in the file /etc/passwd

-------------------------------------------------------------------
### <p align=center>`16. What's next?`</p>
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.

-------------------------------------------------------------------
### <p align=center>`17. I hate bins`</p>
Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.

-------------------------------------------------------------------
### <p align=center>`18. Letters only please`</p>
Display all lines of the file /etc/ssh/sshd_config starting with a letter.

- include capital letters as well
-------------------------------------------------------------------
### <p align=center>`19. A to Z`</p>
Replace all characters A and c from input to Z and e respectively.

-------------------------------------------------------------------
### <p align=center>`20. Without C, you would live in hiago`</p>
Create a script that removes all letters c and C from input.

-------------------------------------------------------------------
### <p align=center>`21. esreveR`</p>
Write a script that reverse its input.

-------------------------------------------------------------------
### <p align=center>`22. DJ Cut Killer`</p>
Write a script that displays all users and their home directories, sorted by users.

- Based on the the /etc/passwd file
-------------------------------------------------------------------
### <p align=center>`23. Empty casks make the most noise`</p>
Write a command that finds all empty files and directories in the current directory and all sub-directories.

- Only the names of the files and directories should be displayed (not the entire path)
- Hidden files should be listed
- One file name per line
- The listing should end with a new line
- You are not allowed to use basename, grep, egrep, fgrep or rgrep
-------------------------------------------------------------------
### <p align=center>`24. A gif is worth ten thousand words`</p>
Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.

- Hidden files should be listed
- Only regular files (not directories) should be listed
- The names of the files should be displayed without their extensions
- The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)
- One file name per line
- The listing should end with a new line
- You are not allowed to use basename, grep, egrep, fgrep or rgrep
-------------------------------------------------------------------
### <p align=center>`25. Acrostic`</p>
An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval. Read more.

Create a script that decodes acrostics that use the first letter of each line.

- The ‘decoded’ message has to end with a new line
- You are not allowed to use grep, egrep, fgrep or rgrep
-------------------------------------------------------------------
### <p align=center>`26. The biggest fan`</p>
Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.

- Order by number of requests, most active host or IP at the top
- You are not allowed to use grep, egrep, fgrep or rgrep
-------------------------------------------------------------------



## <p align=right>`Score: 100/100`</p>

-------------------------------------------------------------------
