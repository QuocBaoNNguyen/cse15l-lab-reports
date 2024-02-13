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

1. `grep -i `

<br/>

1a.

<br/>
```
tonyn@BOOK-PHHA2EB9PA MINGW64 ~/Downloads/docsearch-main/technical/911report
$ grep -i "Gerard" *.txt
chapter-1.txt:    At 9:00, American Airlines Executive Vice President Gerard Arpey learned that communications had been lost with American 77. This was now the second American aircraft in trouble. He ordered all American Airlines flights in the Northeast that had not taken off to remain on the ground. Shortly before 9:10, suspecting that American 77 had been hijacked, American headquarters concluded that the second aircraft to hit the World Trade Center might have been Flight 77. After learning that United Airlines was missing a plane, American Airlines headquarters extended the ground stop nationwide.
chapter-13.2.txt:            55. Gerard Arpey interview (Jan. 8, 2004); Larry Wansley interview (Jan. 8, 2004);

```
<br/>

This command searches all the .txt files in the `/Downloads/docsearch-main/technical/911report` directory for "Gerard" and returns the line that has it. But more specifically, the "-i" part of the command makes it so that it ignores cases. Thus, if I were to use "GERARD" or "gerard" or "geRarD" I would still get the same result. I do this example in the next one. This is helpful if your looking for a certain word and don't care about the capitalization it has in the file.

<br/>

1b.

<br/>

```
tonyn@BOOK-PHHA2EB9PA MINGW64 ~/Downloads/docsearch-main/technical/911report
$ grep -i "GERARD" *.txt
chapter-1.txt:    At 9:00, American Airlines Executive Vice President Gerard Arpey learned that communications had been lost with American 77. This was now the second American aircraft in trouble. He ordered all American Airlines flights in the Northeast that had not taken off to remain on the ground. Shortly before 9:10, suspecting that American 77 had been hijacked, American headquarters concluded that the second aircraft to hit the World Trade Center might have been Flight 77. After learning that United Airlines was missing a plane, American Airlines headquarters extended the ground stop nationwide.
chapter-13.2.txt:            55. Gerard Arpey interview (Jan. 8, 2004); Larry Wansley interview (Jan. 8, 2004);

```

<br/>

This does exactly the same as described in 1a. The only difference is that I used "GERARD" instead of "Gerard". Notice how it still provides me the same lines like I claimed. This is helpful if I know I'm looking for the name "Gerard" but I'm not too sure on the capitalization of the name. 

<br/>

2. `grep -n`

<br/>

2a.

 









