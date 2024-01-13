# CSE 15L Lab Report 1 

## cd Command
<br/>
NO ARGUMENTS

### Input/Output


```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```

**Working Directory:** home
 <br/>
 <br/>
**Explanation:** The following output occurred because of the fact that cd stands for change directory, however, since there was no argument, there was no directory to change to. Thus, the code essentially did nothing as it had no directory to take us to.
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

**Working Directory:** home
<br/>
<br/>
**Explanation:** This time, there was a directory provided. As a result, Java took us to the given directory with the cd command. This can be seen as the resulting line in ther terminal has "/lecture1" inbetween the brackets to indicate to us that we are now working in the directory of lecture1.
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

**Working Directory:** lecture1
<br/>
<br/>
**Explanation:** With a file as the argument, Java indicates to us that it is specifically only wants directories as arguments and nothing else when using the cd command. Since we gave it a file, it rejected the command and stated that "Hello.class: Not a directory".
<br/>
<br/>
This out is an error because we did not provide the cd command with the correct form of argument; directories.
<br/>
***
## ls Command
NO ARGUMENT

### Input/Output

```
[user@sahara ~]$ ls
lecture1
```

**Working Directory:** home
<br/>
<br/>
**Explanation:** The ls command lists out all the folders and files from the argument provided. Since there was no argument provided, I'm assuming Java just provided all the files and folders in the home directory, which is lecture1 as it is the only one in that certain path. If there was another folder/file in the home path, it would have included it in the list alongside lecture1.
<br/>
<br/>
This is NOT an error
<br/>
***
DIRECTORY AS ARGUMENT




