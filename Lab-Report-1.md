# ***CSE 15L lab report***   
Name: William Share

***cd***
---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/ee2bf43e-e1c2-460a-b925-2c31d175cb8c)

The working directory when the command was run was `/home/lecture1/messages` as seen when `pwd` was run.

I got this output because when you run `cd` with no arguments, we return to the home directory (default directory).

This output is not an error. When `cd` is used without an argument it should return to the home directory.

---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/f4833983-a6d8-451c-931e-45d0c427cfe7)

The working directory when the command was run was `/home` as seen when `pwd` was run.

When using `cd` with a folder (directory) as an argument, the working directory changes to that directory.

This output is not an error because when `cd` is used with a folder as an argument it switches into that. It changes its directory to the specified argument when it is a folder.

---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/623d1fda-b2b5-42df-b877-0caae3bba611)

The working directory when the command was run was `/home/lecture1/messages` as seen when `pwd` was run.

When using `cd` with a file such as a text file as an argument, the working directory cannot change and gives us an error as it is trying to change its directory to a text file.

This output is an error because `cd` cannot be used to change its directory to a file, thus giving us this error. It is supposed to be used with a directory like a folder.




***ls***
---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/2495cfdb-70a7-473a-a3d7-a6feebbd6fe4)

The working directory when the command was run was `/home` as seen when `pwd` was run.

When using `ls` with no arguments, it lists the directories and files and in this case all the directories and files in the home directory (because we are in the home directory). Becaues the only directory is `lecture1` it lists `lecture1`.

This output is not an error because there is only one directory and no files to list, that being `lecture1` (directory).

---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/20653a35-0b45-4c76-b0d9-6f1c0e55751e)

The working directory when the command was run was `/home` as seen when `pwd` was run.

When using `ls` with a directory, it lists all of the contents (directories and files) that are within the directory. In this case it lists all of the contents inside the `lecture1` directory.

This output is not an error because it is listing all of the contents inside the argument (directory).

---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/ce34b966-c7ef-4691-b8e4-d3edb6a4dfc4)

The working directory when the command was run was `/home/lecture1/messages` as seen when `pwd` was run.

When using `ls` with a file such as the `en-us.txt` flie, it returns the `en-us.txt` file because it cannot show the files and directories of a directory as the `en-us.txt` file is not a directory.

This output is not really an error because the `ls` command lists all of the files and directories within a specified directory. However, when the argument is a file, it will just display the file name because it cannot list the files and directories within a file (contains no files/directories).


***cat***
---
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/18451e2c-b816-4009-bf0d-2e8d7f719c2e)

The working directory when the command was run was `/home` as seen when `pwd` was run.

When using `cat` with no argument(s), you will be able to continue typing into the terminal where it will reiterate to you what the input you typed. When I press `ctrl + c` I can exit.

This output is not really an error because `cat` is used to list the contents of a file. However, when there is no file for it to list (no file is given as an argument) it cannot list anything which causes it to reiterate the input given to the terminal and will read from the terminal because it has no files to read.

---

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/4eb606c2-6593-45ad-b66e-d9e3110f92af)

The working directory when the command was run was `/home` as seen when `pwd` was run.

When using `cat` with a directory (lecture1), we see that it tells us that `lecture1` is a directory. This happens because `cat` is used to display the contents of a file. However, when `cat` is used with a directory, it lets the user know that they are trying to list the contents of a directory not a file.

This output is an error because `cat` is supposed to be used with files, but when used with directories, the terminal is letting the user know that `cat` cannot be used on a directory by telling the user that the argument (the directory) is a directory which implies it is not a file.

---

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/cbbc0bc9-325d-49a1-b582-5bddcb48ce74)

The working directory when the command was run was `/home/lecture1/messages` as seen when `pwd` was run.

When using `cat` with a file (en-us.txt), we see that it displays the contents of the file. In this case it is "Hello World!" because that is inside the `en-us.txt` file.

This is not an error because this is the function of `cat`. `cat` is used to display the contents of the argument when it is a file.



