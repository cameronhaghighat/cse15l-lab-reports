# **Lab Report 1**
---
## **Command `cd`**
1. **No Arguments**
  - Output:
   ```
{
    @cameronhaghighat ➜ /workspaces/lecture1 (main) $ cd
    @cameronhaghighat ➜ ~ $
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ /workspaces/lecture1 (main) $
}
```
  - Explanation:
    After using `cd` without any arguments, the working directory changed from /workspaces/lecture1 to the home directory (~). The home         directory is the default directory. This is not an error, it is a standard behavior.

2. **Path to a Directory**
  - Output:
   ```
{
    @cameronhaghighat ➜ ~ $ cd /workspaces/lecture1
    @cameronhaghighat ➜ /workspaces/lecture1 (main) $ 
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $ 
}
```
  - Explanation:
    After using `cd` to the path directory /workspaces/lecture1, the working directory changed to /workspaces/lecture1. This is not an          error, it is a standard behavior.

3. **Path to a File**
  - Output:
   ```
{
    @cameronhaghighat ➜ ~ $ cd /workspaces/lecture1/Hello.java
    bash: cd: /workspaces/lecture1/Hello.java: Not a directory
    @cameronhaghighat ➜ ~ $ 
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $ 
}
```
  - Explanation:
    An error was produced after using `cd` to the path to a file /workspaces/lecture1 because the `cd` command was looking for a directory,     not a file.

## **Command `ls`**
1. **No Arguments**
  - Output:
   ```
{
    @cameronhaghighat ➜ /workspaces/lecture1 (main) $ ls
    Hello.class  Hello.java  README  messages
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ /workspaces/lecture1 (main) $
}
```
  - Explanation:
    After using `ls` without any arguments, the terminal lists all the contents within the current directory. This is not an error, it is       standard behavior.

2. **Path to a Directory**
  - Output:
   ```
{
    @cameronhaghighat ➜ ~ $ ls /workspaces/lecture1
    Hello.class  Hello.java  README  messages
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $ 
}
```
  - Explanation:
    After using `ls` to the path directory /workspaces/lecture1, the terminal lists all of the contents of the /lecture1 directory. This is     not an error, this is standard behavior.

    
3. **Path to a File**
  - Output:
   ```
{
    @cameronhaghighat ➜ ~ $ ls /workspaces/lecture1/Hello.java
    /workspaces/lecture1/Hello.java
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $ 
}
```
  - Explanation:
    After using `ls` to the path to a file /workspaces/lecture1/Hello.java, the terminal displays the path to the file. This is not an          error.

## **Command `cat`**
1. **No Arguments**
  - Output:
```
{
    @cameronhaghighat ➜ ~ $ cat
   
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ /workspaces/lecture1 (main) $
}
```
  - Explanation:
    After using `cat` without any arguments, the terminal moves to an empty, new line. The command is waiting for an argument to be given.      This is not an error.

2. **Path to a Directory**
  - Output:
```
{
    @cameronhaghighat ➜ ~ $ cat /workspaces/lecture1
    cat: /workspaces/lecture1: Is a directory
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $ 
}
```
  - Explanation:
    This produced an error because the command argument was incorrect. It is looking for a list of files, not a directory.

    
3. **Path to a File**
  - Output:
```
{
    @cameronhaghighat ➜ ~ $ cat /workspaces/lecture1/Hello.java
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
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $

}
```
  - Explanation:
    After using `cat` to the path to a file /workspaces/lecture1/Hello.java, the terminal prints all of the contents of the file         
    Hello.java. This is not an error.

