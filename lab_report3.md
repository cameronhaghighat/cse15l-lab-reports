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


