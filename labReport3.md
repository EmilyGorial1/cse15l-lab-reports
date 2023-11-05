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
}```

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
}```

3.) Screenshots of the symptom as the output of running the tests for each input above

![Image](https://github.com/EmilyGorial1/cse15l-lab-reports/blob/main/testReverseInPlace-%20failure%20inducing%20input.png)

![Image](testReverseInPlace- failure inducing input.png)

![Image](testReverseInPlace- input that does not induce failure part 1.png)

![Image](testReverseInPlace- input that does not induce failure part 2.png)


