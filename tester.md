## **Command `cat`**
1. **No Arguments**
  - Output:
```
{
    @cameronhaghighat ➜ ~ $ ls
  
}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $
}
```
  - Explanation:
    After using `cat` without any arguments, the terminal moves to an empty, new line. The command is waiting for an argument to be given. This is not an error.

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

}
```
  - Absolute Path:
```
{
    @cameronhaghighat ➜ ~ $ 
}
```
  - Explanation:
    After using `cat` to the path to a file /workspaces/lecture1/Hello.java, the terminal prints all of the contents of the file Hello.java. This is not an error.

