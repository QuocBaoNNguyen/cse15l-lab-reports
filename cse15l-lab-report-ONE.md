# CSE 15L Lab Report 1 

## `cd` Command
<br/>
NO ARGUMENTS

### Input/Output


```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```

**Working Directory:** `/home`
 <br/>
 <br/>
**Explanation:** The following output occurred because of the fact that `cd` stands for change directory, however, since there was no argument, the command changed the directory to the home directory. This is true because when I change the directory to `/lecture1` and use the `cd` command with no argument, the directory is changed to the home directory.
<br/>
<br/>
This output is NOT an error
<br/>
***
DIRECTORY AS ARGUMENT

### Input/Output

```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```

**Working Directory:** `home`
<br/>
<br/>
**Explanation:** This time, there was a directory provided. As a result, Java took us to the given directory with the `cd` command. This can be seen as the resulting line in ther terminal has `/lecture1` inbetween the brackets to indicate to us that we are now working in the directory of `lecture1`.
<br/>
<br/>
This output is NOT an error
<br/>
***
FILE AS ARGUMENT

### Input/Output

```
[user@sahara ~/lecture1]$ cd Hello.class
bash: cd: Hello.class: Not a directory
```

**Working Directory:** `lecture1`
<br/>
<br/>
**Explanation:** With a file as the argument, Java indicates to us that it is specifically only wants directories as arguments and nothing else when using the `cd` command. Since we gave it a file, it rejected the command and stated that `Hello.class: Not a directory`.
<br/>
<br/>
This out is an error because we did not provide the `cd` command with the correct form of argument; directories.
<br/>
***
## `ls` Command
NO ARGUMENT

### Input/Output

```
[user@sahara ~]$ ls
lecture1
```

**Working Directory:** `home`
<br/>
<br/>
**Explanation:** The `ls` command lists out all the folders and files from the argument provided. Since there was no argument provided, I'm assuming Java just provided all the files and folders in the home directory, which is `lecture1` as it is the only one in that certain path. If there was another folder/file in the home path, it would have included it in the list alongside `lecture1`.
<br/>
<br/>
This is NOT an error
<br/>
***
DIRECTORY AS ARGUMENT

### Input/Output

```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```
**Working Directory:** `home`
<br/>
<br/>
**Explanation:** Now that we have provided the `ls` command with a directory, it can now take that given directory and return us all the files and folders in it. In this case, it gave us all the files/folders in the `lecture1` directory. This is how the ls command was intended to be utilized.
<br/>
<br/>
This is NOT an error
<br/>
***

FILE AS ARGUMENT

### Input/Output

```
[user@sahara ~]$ ls Hello.java
ls: cannot access 'Hello.java': No such file or directory
```
**Working Directory:** `home`
<br/>
<br/>
**Explanation:** In the command, we are trying to get Java to list out all the files and folders in `Hello.java`. However, we get the result that it cannot acces `Hello.java`. This is because there are not files or directories inside this file. As a result, we get an error from providing a file instead of a path.
<br/>
<br/>
This is an error because `Hello.java` is a file, not a directory/path for Java to list whats inside of it. Notice how when we used a directory as an arguement it went well. This is because it was a folder with many more files/folders in it. With the files, this is not the case and there is nothing else to open.
<br/>
***

## `cat` Command
NO ARGUMENT

### Input/Output

```
[user@sahara ~]$ cat

```
**Working Directory:** `home`
<br/>
<br/>
**Explanation:** As we can see, the output gives us nothing. This is because with no argument, we give Java nothing to concatenate. As a result, it returns blank.
<br/>
<br/>
This is an error because Java was expecting an argument of a file to concatenate, however, it got nothing so it did not perform the command as it wanted to.
<br/>
***

DIRECTORY AS ARGUMENT

### Input/Output

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
**Working Directory:** `home`
<br/>
<br/>
**Explanation:** In the result, Java tells us that `cat` is a directory. It tells us this because it expects an argument that is a file, not a directory. As a result, the cat command doesn't run as it was intended to and simply says `cat: lecture1: Is a directory`. This is due to the fact that your cannot concatenate a folder; it is a path.

<br/>
<br/>
This is an error because Java cannot concatenate a directory. It needs the argument to be a file, something that is actually concatenatable.
<br/>

***

FILE AS ARGUMENT

### Input/Output

```
[user@sahara ~/lecture1]$ cat README
To use this program:

javac Hello.java
java Hello messages/en-us.txt
```
**Working Directory:** `lecture1`
<br/>
<br/>
**Explanation:** This is a more appropiate use of the command. Here we are in the `lecture1` directory because there are actually files here for us to access. After running the command, Java concatenates whats in the file of the argument, which in this case is `README`(it provided the first line of the file).
<br/>
<br/>
This is NOT an error
<br/>
***





