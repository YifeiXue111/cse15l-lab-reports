# Lab Report1
1. Example of using the command with no arguments
```
[user@sahara ~]$ ls  
lecture1  
```
The working directory was /home when the command was run.  
ls lists the files in the current working directory, and lecture1 is the only file in the working directory, so lecture1 is shown.  
This output is not an error.  

```
[user@sahara ~]$ cat

```
The working directory was /home when the command was run.  
The command cat will read contents from the file given by the path. Since there's no path provided, it does not return anything.  
This output is not an error. 
```
[user@sahara ~]$ cd
[user@sahara ~]$
```
The working directory was /home when the command was run.  
The command cd with no argument will change the working directory to the home directory. In this case since the current directory is already home directory, nothing is changed.
This output is not an error. 
  
  
  
2.  Example of using the command with a path to a directory as an argument[user@sahara ~]$ cat lecture1/Hello.java
```
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




3.  Example of using the command with a path to a file as an argument
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
