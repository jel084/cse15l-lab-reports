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
  ![Image](failureinducing.png)
  b. running the input that doesn't induce a failure
  
    ![Image](notfail1.png)
    ![Image](notfail2.png)
4. Before and After Code Change
   a. Before Code Change
 ````
    static void reverseInPlace(int[] arr) {
      for(int i = 0; i < arr.length/2; i += 1) {
      arr[i] = arr[arr.length - i - 1];
      }
    }
````
   b. After Code Change
````
   static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int firstHalf = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - 1 - i] = firstHalf;
    }
 ````
 dj


