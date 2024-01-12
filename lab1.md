# Lab Report1
1. **Examples of using the command with no arguments**  
-**Example1**
   ```
   [user@sahara ~]$ ls
   lecture1
   ```
   The working directory was /home when the command was run.  
   The command ls lists the files in the current working directory, and lecture1 is the only file in the working directory, so lecture1 is shown.  
   This output is not an error.
-**Example2**
   ```
   [user@sahara ~]$ cat
   ```
   The working directory was /home when the command was run.  
   The command cat will read contents from the file given by the path. Since there's no path provided, it does not return anything.  
   This output is not an error.   
-**Example3**
   ```
   [user@sahara ~]$ cd
   ```
   The working directory was /home when the command was run.  
   The command cd with no argument will change the working directory to the home directory. In this case since the current directory is already home directory, nothing is changed.  
   This output is not an error.        
2.  **Examples of using the command with a path to a directory as an argument**  
**Example1**  
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
The working directory was /home when the command was run.  
The command cd will change the working directory to the given directory. So starting from the next command the working directory is lecture1 instead of /home.  
This output is not an error.   
**Example2**  
```
[user@sahara ~]$ ls lecture1/messages
en-us.txt  es-mx.txt  zh-cn.txt
```
The working directory was /home when the command was run.  
The command ls lists  the files in the given path. There are three files in the folder messages, so the names of the three files are listed in the output.  
This output is not an error.  
**Example3**  
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
The working directory was /home when the command was run.  
The command cat will read contents from the file given by the path, but in this case a directory is given instead of a file, so an error message is shown.  
This output is an error because the argument should be a file instead of a directory.   
3.  **Examples of using the command with a path to a file as an argument**   
**Example1**  
```
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
}
```
The working directory was /home when the command was run.  
The command cat will read contents from the file given by the path, so the output includes the contents in the file Hello.java.  
This output is not an error.  
**Example2**   
```
[user@sahara ~]$ cd lecture1/Hello.java 
bash: cd: lecture1/Hello.java: Not a directory
```
The working directory was /home when the command was run.  
The command cd will change the working directory to the given directory. In this case a file instead of a directory is given, so the output is an error message.  
This output is an error because the argument should be a directory instead of a file.  
**Example3**    
```
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java
```
The working directory was /home when the command was run.  
The command ls lists  the files in the given path, the given path is a file, so the file itself is the output.  
This output is not an error.  
