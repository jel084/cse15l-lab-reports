# **Lab 2**
Tutorial on loggining into ieng6

## **Part 2** Choosing one of the bugs from lab 3.

1. failure-inducing input for the buggy program

```
@Test
  public void testReversedagain(){
    int[] = input1 = {1,2,3,4,5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int [] {5,4,3,2,1}, input1_;
  }
````
2. input that doesn't induce a failure
````
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
````
3. symptoms of running the test
  a. running the failure-inducing input
  
  b. running the input that doesn't induce a failure
