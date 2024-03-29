<p align=center >
  <img src = "http://2.bp.blogspot.com/-TfLl-0Uus0E/VvFlb4YrV1I/AAAAAAAABmo/Zg1CfFww2eI0T0DpMv-wKzNFNsLaAOFeA/s1600/permissions-01.png" />
</p>

# <p align=center >`Shell, permissions`</p>
## <p align=center> `Project's obejectives` </p>
Be able to explain:
- What do the commands chmod, sudo, su, chown, chgrp do
- Linux file permissions
- How to represent each of the three sets of permissions (owner, group, and other) as a single digit
- How to change permissions, owner and group of a file
- Why can’t a normal user chown a file
- How to run a command with root privileges
- How to change user ID or become superuser

- How to create a user
- How to create a group
- How to print real and effective user and group IDs
- How to print the groups a user is in
- How to print the effective userid

## <p align=center >`Resources`</p>
Read or watch:
- [Permissions](https://intranet.hbtn.io/rltoken/UL7cEzRpzknNKTQ-3-zH2w)

## <p align=center>`Tasks`</p>
### <p align=center>`0. My name is Betty`</p>
Create a script that switches the current user to the user betty.

- You should use exactly 8 characters for your command (+1 character for the new line)
- You can assume that the user betty will exist when we will run your script
-------------------------------------------------
### <p align=center>`1. Who am I`</p>
Write a script that prints the effective username of the current user.

-----------------------------------------------
### <p align=center>`2. Groups`</p>
Write a script that prints all the groups the current user is part of.

-----------------------------------------------
### <p align=center>`3. New owner`</p>
Write a script that changes the owner of the file hello to the user betty

-----------------------------------------------
### <p align=center>`4. Empty!`</p>
Write a script that creates an empty file called hello.

-----------------------------------------------
### <p align=center>`5. Execute`</p>
Write a script that adds execute permission to the owner of the file hello.

- The file hello will be in the working directory
-----------------------------------------------
### <p align=center>`6. Multiple permissions`</p>
Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

- The file hello will be in the working directory
-----------------------------------------------
### <p align=center>`7. Everybody!`</p>
Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

- The file hello will be in the working directory
- You are not allowed to use commas for this script
-----------------------------------------------
### <p align=center>`8. James Bond`</p>
Write a script that sets the permission to the file hello as follows:

- Owner: no permission at all
- Group: no permission at all
- Other users: all the permissions
-----------------------------------------------
### <p align=center>`9. John Doe`</p>
Write a script that sets the mode of the file hello to this:
```
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
```
- The file hello will be in the working directory
- You are not allowed to use commas for this script

-----------------------------------------------
### <p align=center>`10. Look in the mirror`</p>
Write a script that sets the mode of the file hello the same as olleh’s mode.

- The file hello will be in the working directory
- The file olleh will be in the working directory
-----------------------------------------------
### <p align=center>`11. Directories`</p>
Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.

-----------------------------------------------
### <p align=center>`12. More directories`</p>
Create a script that creates a directory called my_dir with permissions 751 in the working directory

-----------------------------------------------
### <p align=center>`13. Change group`</p>
Write a script that changes the group owner to school for the file hello

- The file hello will be in the working directory
-----------------------------------------------
### <p align=center>`14. Owner and group`</p>
Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.

-----------------------------------------------
### <p align=center>`15. Symbolic links`</p>
Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.

- The file _hello is in the working directory
- The file _hello is a symbolic link
-----------------------------------------------
### <p align=center>`16. If only`</p>
Write a script that changes the owner of the file hello to vincent only if it is owned by the user guillaume.

- The file hello will be in the working directory
-----------------------------------------------
## <p align=right>`Score: 100/100`</p>
