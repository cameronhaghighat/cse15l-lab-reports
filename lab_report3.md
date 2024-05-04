# Lab Report 3

## Part 1

### A Failure-Inducing Input for the Buggy Program

```
@Test
public void FailureInducingInputTest() {
    int[] input1 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3, 2, 1}, input1);
}

```

### An Input That Doesn't Induce a Failure

```
@Test
public void SuccessfulInputTests() {
  int[] input1 = { 1 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 1 }, input1);
}

```

### The Symptom

//Add Image Here

### The Bug Before and After

Before:

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }

```

After: 

```
static void reverseInPlace(int[] arr) {
    int[] temp = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      temp[i] = arr[i];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = temp[arr.length - i - 1];
    }
  }

```

### Why the Fixes are True

The bug in reverseInPlace has to do with assigning updated values back to the array. For example, the last index in an array would take the value of the first, but the first index has the value of the last from the first iteration of the loop. In order to get around this, I created a temporary array to hold the values of the array and then looped through the temporary array backwards and assigned those values to the original array.


## Part 2 `grep`

Source: https://phoenixnap.com/kb/grep-command-linux-unix-examples

### The `-i` Command-Line Option

This command-line option ignores differences between lowercase and uppercase letters. This may be useful if we do not care about case sensitivity.

Examples:

```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -i "Is it still possible to work there?" plos/journal.pbio.0020214.txt  
        “Is it still possible to work there?” The best response to the first question is, “Why
```
```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -i "IS IT STILL POSSIBLE TO WORK THERE?" plos/journal.pbio.0020214.txt
        “Is it still possible to work there?” The best response to the first question is, “Why
```
### The `-c` Command-Line Option

This command-line option counts how many lines match the search pattern. It can be useful if we are looking for the frequency of a search pattern.)

Examples:

```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -c "Is it still possible to work there?" plos/journal.pbio.0020214.txt  
1
```
```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -c "This shouldn't be in the text." plos/journal.pbio.0020214.txt  
0
```

### The `-x` Command-Line Option

This command-line option looks to match whole lines which can be helpful for case sensitive searches. For example, if we are looking for file paths that we store in a directory.

Examples:

```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -x "        The contribution of the international community cannot be the sole decisive factor in" plos/journal.pbio.0020
214.txt  
        The contribution of the international community cannot be the sole decisive factor in
```
```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -x "       Edit  The contribution of the international community cannot be the sole decisive factor in" plos/journal.pbio
.0020214.txt
```

### The `-w` Command-Line Option

This command-line options matches only whole words. It can be helpful if we want the search results to only the exact terms specified.

Examples:

```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -w "Is it still possible to work there?" plos/journal.pbio.0020214.txt
        “Is it still possible to work there?” The best response to the first question is, “Why
```
```
(base) MacBook-Pro-83:technical cameronhaghighat$ grep -w "Is it still possible to work ther" plos/journal.pbio.0020214.txt
```


