# Lab Report 2
## Part 1
* Screenshot 1: ![Image]()
* The method in my code that is being called would be my handleRequest method, which takes in my message that I want added into the website and returns it the way I want it to look like.
* The relevant arguments to my handleRequest method would be my url argument, which is taking in the url that we want to reach, and the relevant values of any relevant fields of the class would be my combined variable and my String[ ] input that update continuously depending on each input used.
* The values of the relevant fields of the class changed from this specific request was by my combined variable combining the phrase I wanted in the url and returning it in the server used.

* Screenshot 2: ![Image]()
* The method in my code that is being called would be my handleRequest method, which takes in my message that I want added into the website and returns it the way I want it to look like.
* The relevant arguments to my handleRequest method would be my url argument, which is taking in the url that we want to reach, and the relevant values of any relevant fields of the class would be my combined variable and my Sting[ ] input that update continuously depending on each input used.
* The values of the relevant fields of the class changed from this specific request was by my combined variable combining the phrase I wanted in the url and returning it in the server used.

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
* Input 1 Screenshot : ![Image]()
* Input 2 Screenshot : ![Image]()

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
