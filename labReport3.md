**Part 1- Bugs**

The bug I have chosen from week 4 is the bug in the reverseInPlace() method

1.) A failure-inducing input as a JUnit test

```public class ArrayTests 
{
  @Test
  public void testReverseInPlace()
  {
    int[] input1 = {1,2};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{2,1}, input1};
   }
}
```

2.) An input that does not induce a failure

```public class ArrayTests 
{
  @Test
  public void testReverseInPlace()
  {
    int[] input1 = {1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1}, input1};
   }
}
```

3.) Screenshots of the symptom as the output of running the tests for each input above

![testReverseInPlace-nf1](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/7f2e25af-fc1e-44e3-83a4-bcf4bf897afa)

![testReverseInPlace-nf2](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/e5cee4b4-b5de-4b31-b495-2ac89029e06d)

![testReverseInPlace-f](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/37e95678-175b-49f6-ba7e-d5a43aae606c)


