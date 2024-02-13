# Lab Report 3- Bugs and Commands
## Part 1- Bug with `reversed` method
Failure Inducing Input:
<br/>
```
@Test
  public void testReversed() {
    int[] input1 = {1,2,3,4};
    assertArrayEquals(new int[] {4,3,2,1}, ArrayExamples.reversed(input1));
  }
```
<br/>
Non-Failure Inducing Input:
<br/>

```
@Test
  public void testReversed2() {
    int[] input1 = { 0, 0, 0, 0 };
    assertArrayEquals(new int[] { 0, 0, 0, 0 }, ArrayExamples.reversed(input1));
  }
```

<br/>
Symptom: The method will only return an array full of zeros the size of the inputted array.
<br/>

![Image](image(1).png)

<br/>

The Bug: The issue with the method is that it directly changes the inputted array instead of working on a dummy array.

<br/>
Before:
<br/>

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for (int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

<br/>

After:

<br/>

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for (int i = 0; i < arr.length; i++) {
        newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```

<br/>

This slight, yet, important change fixed the code because of 2 things. First, the for loop no longer directly changes the `arr` array (our inputted array). Instead, it changes out dummy array, `newArray` as it should. Second, it returns `newArray` instead of `arr`.

<br/>

# Part 2- Research on `grep`

1. grep -i



