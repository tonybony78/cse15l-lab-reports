# Week 1 Lab Tutorial 
Howdy, future 15L students and TAs/tutors who read this and decide whether the quality of this post is even worth showing to those students. 
In this post, I will be demonstrating how to set up your CSE account, install Virtual Studio Code, remotely connect to CSE servers, and try some basic terminal commands, so that you have a successful course in 15L.

## Setting Up Your Account
First, access this [link](https://sdacs.ucsd.edu/~icc/index.php) and input your UCSD username and Student ID to get to the next page.
It should look like this.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064716040023584797/image.png)

Click on your CSE-specific username, as designated by the blue arrow in my picture, and access the next page.
This page will appear identical to the previous one, however in this one, you will be able to set the password for your CSE account. To do so, click on the blue highlighted "change your password" in the top section, as shown in the previous image.
You may have to input your UCSD username and ID once more and after you do so, you will come across this page. 

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064722923056803932/image.png)

Be **CAUTIOUS** at this step, as mistakes commonly happen here (I may or may not have also made the same mistake).
Under the Current Password prompt, input your UCSD account password, and under New Password and Confirm Password, input any complex (mix capital letters, symbols, numbers) password of your choice and keep it in between 12-30 characters.
**DO NOT CLICK ANYTHING OR PRESS ENTER JUST YET**
Before doing anything, make sure to change the "Change MyTritonLink password?" input to "No" and change the "Change course-specific account passwords?" to "Yes."
Finally, click on the "Confirm Password" box and click the ENTER key on your keyboard.
If every step was followed correctly, you should arrive at a page that says "Success!" and confirms your password change.

## Installing Visual Studio Code
To install Visual Studio Code (VSCode), go to their [website](https://code.visualstudio.com/), find the right version for your operating system (Windows, macOS, Linux), and download it on your computer. At the center of the page, there should be a large Download button for Windows, alongside a dropdown menu that includes other versions for different operating systems. 
Once you have installed the program, open it and you will see a screen similar to this (may look different depending on system or settings of choice). 

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064728748114587758/image.png)

## Remote Connection
Before taking any of these steps, if you have Windows, you must first install Git for Windows, which is necessary for what we will do later on. It can be found on this [link](https://gitforwindows.org/), just click the Download button and install it onto your computer. Upon installation, you might run into numerous steps that ask for a number of options for the program. The only one you should worry about is this.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064734246431899668/image.png).

This option should appear after clicking Next two or three times, but ensure you choose VSCode as the default editor, as shown in the screen.
Before, when I was following the main 15L guide, I had trouble getting Git Bash to appear in VSCode, but when I deleted and reinstalled Git and chose this option, it finally appeared properly.
Afterwards, open up VSCode and click the Ctrl + ' keys to open up your terminal. Next, click the Ctrl + Shift + P keys to open up VSCode's Command Palette. Enter "-Select Default Profile" and click on Git Bash. It should look a little something like this.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064740257351860294/image.png)

In your terminal window, click the + option on the right side and you have now created a Git Bash terminal. Your terminal should appear similar to this.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064743387036651600/image.png)

If you notice, I have created several bash terminals already and in the dropdown menu next to the +, there are different choices of terminals.

Now, open a Git Bash terminal using the previous steps and input "ssh ______" Replace the underline with your CSE account, which you can find in the first step where you set up your account. It should follow the format of **cs15lwi23__@ieng6.ucsd.edu**. 

Because you are inputting this command for the first time ever, you should receive a message that asks if you are sure you want to continue connecting. If this is the first time, go ahead and input "yes," but if it is not, you may have a security concern.

After inputting "yes," the terminal will ask for your password, which you established earlier in Step 1. At this point, your terminal should look similar to this. 

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064749418580037692/image.png)

Input your password and the terminal should spit out a lot of lines, which will look something like this.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064751083685171211/image.png)

You have now connected to the CSE Basement computers!

## Testing Commands
From this point, you can now test some basic terminal commands to manuever through and see the contents of the computer you are connected to.
Some commands you can try out yourself are:
- cd
- ls
- ls -lat
- ls -a
- cat /home/linux/ieng6/cs15lwi23/public/hello.txt
- cat /home/linux/ieng6/cs15lwi23/cs15lwi23awo/perl5
- pwd

In this image, you can see some of these commands I have tried on my own terminal.

![Image](https://cdn.discordapp.com/attachments/1064716019156930640/1064754488050733126/image.png)

If you want to exit or end your terminal connection, just input "exit" or click the Ctrl + D keys.

Congratulations! You have made it all the way here and I wish you the best of luck for the rest of your CS career. You will need it.
