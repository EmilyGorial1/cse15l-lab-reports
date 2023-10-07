**1) cd with no arguments, cd with path to directory as argument, cd with path to file as argument**

cd commands

```
[user@sahara ~]$ cd
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd Hello.class
bash: cd: Hello.class: Not a directory
```
For cd with no arguments, the working dirctory is just /home. There is no output because we did not give cd a directory to change to. For this reason there is no change or output.

For cd lecture1, the working directory is now /home/lecture1. There is no output, however we now see that 'lecture1' has been added behind the tilde symbol, indicating that we are now in the lecture1 folder.

For cd Hello.class, the working directory is also /home/lecture1. Our output produces an error because the command cd tells the computer to change directory, yet we passed in 'Hello.class', which is not a directory. For this reason, we get an error for our output.


**2) ls with no arguments, ls with path to directory as argument, ls with path to file as argument**

ls commands

   ```
   [user@sahara ~]$ ls
   lecture1  'running cd commands.PNG'
   [user@sahara ~]$ ls lecture1
   Hello.class  Hello.java  messages  README
   [user@sahara ~]$ ls Hello.class
   ls: cannot access 'Hello.class': No such file or directory
   ```


**3) cat with no arguments, cat with path to directory as argument, cat with path to file as argument**

cat commands

```
[user@sahara ~]$ cat
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

