## Lab Report 4

To start things off, first I log into *ieng6* by typing

``` ssh cs15lwi23awoieng6.ucsd.edu ```

![img](https://cdn.discordapp.com/attachments/1064716019156930640/1084954193984487544/image.png)

``` git clone <Ctrl+V> -> (git@github.com:tonybony78/lab7.git) <enter> ```

The link is copied from my repository on GitHub and pasted to complete the first step.

``` cd l<tab> ``` -> autocompletes to "lab7/" ``` <enter> ```
  
``` <Ctrl + V> -> (javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java) <enter> ```
 
The command is copied from Week 3 on the CSE 15L website and compiles all the .java files in the current directory.

``` <Ctrl + V> -> (java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore) <space> 
"Lis"<tab> ```-> autocompletes to "ListExamples." ``` <space> "java" <enter> ``` 
```
 
This command runs the ListExamples.java file.
 
![image](https://user-images.githubusercontent.com/114378343/221395003-3019516e-c4aa-4435-864b-31e87c7a018a.png)
  
``` "nano Lis<tab>" ``` -> autocompletes to "ListExamples." ``` <space> "java" <enter> ```
  
By performing these commands, I am able to edit the text inside ListExamples.java and fix the error.

 `<down>` 42 times, `<right>` 12 times.
   
 `<backspace>` "2"
   
 With the commands in the two previous lines, I manuever to the erroneous line, replacing the 9th occurence of "index1" with "index2".
 The reason it caused an error before was because the loop should have been incrementing index2, rather than index1.

 ![image](https://cdn.discordapp.com/attachments/1064716019156930640/1079283154852008006/image.png)
  
 `<Ctrl + O> <enter> <Ctrl + X>`
   
 Afterwards, I save the changes in the file with its original name and exit nano.
   
 `<up>` 7 times, `<enter>`
   
 The ```"javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java" ```was 7 lines up in the search history, so I scrolled back and entered it to compile the example files once more.
   
 `<up>` 6 times, `<enter>`
   
  The ``` "java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests" ``` was 6 lines up in the search history, so I went back and entered it to run the test file again.
   
 ![image](https://user-images.githubusercontent.com/114378343/221395740-118bf178-8820-498d-b1ec-f422e888ed39.png)

 ``` "git add Lis<tab>" ```-> autocompletes to "ListExamples." ``` <space> "java" <enter> ```
   
 ``` "git commit -m "Updated"" <enter> ```
   
``` "git push" <enter> ```
  
  Because the tests passed completely after the text change, I add the ``` ListExamples.java ``` change to staging, commit the change, and push it to my repository.
  
  ![img](https://cdn.discordapp.com/attachments/1064716019156930640/1079290181586268270/image.png)
   
