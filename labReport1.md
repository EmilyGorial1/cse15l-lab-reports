**1) cd with no arguments, cd with path to directory as argument, cd with path to file as argument**

cd commands

```
[user@sahara ~]$ cd
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd Hello.class
bash: cd: Hello.class: Not a directory
```
For cd with no arguments, the working dirctory is just /home. There is no output because we did not give cd a directory to change to. For this reason there is no change or output. If however, the working directory was lecture1, then cd with no arguments would take us back to the home directory.

For cd with a path to a directory, the working directory is now /home/lecture1. There is no output, however we now see that 'lecture1' has been added behind the tilde symbol, indicating that we are now in the lecture1 folder.

For cd with a path to a file, the working directory is also /home/lecture1. Our output produces an error because the command cd tells the computer to change directory, yet we passed in 'Hello.class', which is not a directory. For this reason, we get an error for our output.


**2) ls with no arguments, ls with path to directory as argument, ls with path to file as argument**

ls commands

   ```
   [user@sahara ~]$ ls
   lecture1 
   [user@sahara ~]$ ls lecture1
   Hello.class  Hello.java  messages  README
   [user@sahara ~]$ ls lecture1/Hello.java
   lecture1/Hello.java
   ```
 For ls with no argument, the working directory is /home. The output is lecture1 because this is the file/folder 
 contained within our working directory (/home). If there were any other files or folders in our working directory, they would also be 
 displayed here.

 For ls with a path to a directory, the working directory is /home, as this is the working directory when the command was run. The output 
 lists the files/folders contained in the lecture1 folder because the ls command's job is to list files and folders from the given path 
 (lecture 1).

 For ls with a path to a file, the working directory is /home. The output is lecture1/Hello.java because ls is meant 
 to print the contents of a directory. When you pass in a file, there are no files/folders contained within the file- a file is not a 
 directory. So, for this reason, the ls command does not work as it is intended to.


**3) cat with no arguments, cat with path to directory as argument, cat with path to file as argument**

cat commands

```
[user@sahara ~]$ cat
^C
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$ cat lecture1/Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
```
For cat with no command, the working directory is /home. For this command, no output is produced because the cat command is typicaly used to print the contents of a file given by the path, yet there is no path (argument) given, and for this reason nothing can be printed. Additionally, after typing cat with no argument and clicking enter, the cursor simply moves down an waits for an argument. For this reason, we cannot move on to type more commands until you press ctrl + C.

For cat with a path to a directory, the working directory is /home. For this command our output is an error. The cat command prints the content of a file, lecture1 is a directory, and for this reason, the cat command is not used in the way it was intended to be used.

For cat with a path to a file, the working directory is /home. For this command, the output is the contents of the Hello.java file printed. This is expected, as we know the cat command is used to print the contents of a file.

