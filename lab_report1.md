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
