# Week 2 Lab Report
## Part 1
Here are the screenshots of my code and the use of /add-message.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1074914702586548354/image.png)

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1069813019321835530/image.png)

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1069817235666911282/image.png)

In the third image above, the method *handleRequest* is called, as it takes an URI argument of value *url*, which in this case, is *http://localhost:6969/add-message?s=Hello World!*. As the method is called, it checks the path, which is *add-message*, then splits the query by "*=*" into a String array *parameters*. Because the first parameter before *=* is an s, it checks if an int variable *count* is 0, as that means the parameter after *=* is the first message to be added. In this image, the value of the first message is "*Hello World!*. This message is added to a String variable *msg*, which is meant to be updated each time a new message is added. Finally, count increments by 1 and the message *msg* is returned.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1069817351790399508/image.png)

In the image above, *handleRequest* is called once more, with a different URI argument, this one being *http://localhost:6969/add-message?s=I%27m%20so%20tired%20of%20this%20world.*. *msg* already has its first item, which means that this new parameter after *=*, "I'm so tired of this world." is added after a string indentation, placing it into a new line. Count is incremented once more, making its value 2, and lastly, the updated *msg* is returned.

## Part 2
For this section, I will be focusing the *reverseInPlace* method from our lab, as shown below.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1069828993722888242/image.png)

Failure-Inducing Input:
```
int[] input2 = {25, 75, 125};
ArrayExamples.reverseInPlace(input2);
assertArrayEquals(new int[]{125, 75, 25}, input2);
```
Non-Failure-Inducing Input:
```
int[] input1 = { 3 };
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{ 3 }, input1);
```
Symptom:

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1069830909886468127/image.png)

Bug:

Before - 
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

After -
```
static void reverseInPlace(int[] arr) {
    int[] arrCopy = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arrCopy[arrCopy.length - i - 1];
    }
  }
```

Fix Reasoning:

The bug that occurs in the before code is that the reverseInPlace method is able to reverse the first half of the data set, but once it gets to the second half, it reverses the first half once more, due to a lack of values to change to. This can be seen in the line:
```
arr[i] = arr[arr.length - i - 1];
```
However, by making a copy of the input array and overwriting the original array's values with those from the copy, as shown in the lines below, there is no complication in overwriting any of the values.
```
int[] arrCopy = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arrCopy[arrCopy.length - i - 1];
    }
```

## Part 3
After completing the past two labs, I can confidently say that I have learned how to diagnose bugs and symptoms in my code much better than I did before. By absorbing the articles from the Week 3 Readings, especially Regehr's well-articulated step-by-step article, I have learned new approaches as well as a new mindset for encountering issues in my programs. Additionally, I learned how to manuever through JUnit and utilize it to my advantage for testing my code.
