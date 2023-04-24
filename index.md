# Lab Report 2
## Part 1

## Part 2
* Failure inducing input for the buggy program
```
@Test
public void testReverseInPlace2()
{
int input1[] ={12,9,6,3};
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{3,6,9,12}, input 1);
}
```
* An input that doesn't induce a failure
```
@Test
public void testReverseInPlace2()
{
int input1[]={ 3 };
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{ 3 }, input 1);
}
```
* The symptom
> Input 1 Screenshot : ![Image](https://github.com/vesalcido/cse-15l-lab-report2/blob/main/Screen%20Shot%202023-04-23%20at%208.11.09%20PM.png)
> Input 2 Screenshot : ![Image](https://github.com/vesalcido/cse-15l-lab-report2/blob/main/Screen%20Shot%202023-04-23%20at%208.13.23%20PM.png)

* The bug(before and after)
```
static void reverseInPlace(int[] arr)
{
for(int i = 0; i < arr.length; i +=1)
{
arr[i]= arr[arr.length - i -1 ];
}
}
```
```
static void reverseInPlace(int[] arr)
{
for(int i = 0; i < arr.length/2; i+=1)
{
int temp = arr[i];
arr[i]= arr[arr.length - i -1 ];
arr[arr.length - i - 1] = temp;
}
}
```


## Part 3
In week 3 of lab I was surprised to learn that even the simplest difference of an operator can make your whole program have a bug. By having this knowledge, working with a group to debug these given programs gave a better insight on how teamwork helps fix these problems by each person focusing on fixing a part of the program. I also liked learning about writing our own tests and how they can help us better understand how to test each part of our code and still be able to collaborate with our group to each make our own test for our partners to try out in the lab.
