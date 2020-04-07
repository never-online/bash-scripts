# info1211-bashscripts

Scripts

1.	Write a Bash script called postal that asks the user to enter the following pieces of information, one at a time: their first name, their last name, their home street address, their city of residence, their province, and their postal code. The script should then write out all the information in the format of a Canadian mailing address. Here is an example of what the script might show as output:
John Smith		 first and last name
123 Main Street	 street address
Vancouver  BC		 city and province
V5K 1R6		 postal code (letter, digit, letter, space, digit, letter, space)

2.	Write a Bash script called arithmetic that asks the user to enter two numbers (a and b). The script should then write out the numbers’ sum (a+b), their difference (a-b), their product (a*b) and their quotient (a/b). You do not have to do any error-checking, and you do not need to ask the user which operation to perform; the script should do all four calculations each time the script is executed.

3.	Write a Bash script called hello that uses command line arguments to allow the user to put two strings after the command name, when the script is being executed. These strings should represent a first and last name. The script should then write out a greeting to the user that includes the first and last name. Here is an example of how the script might work (the first line represents what the user types to launch the script):
[user@HAL] hello John Smith		 you type the script name followed by first and last name
Hey John Smith, nice to see you	 script writes out the greeting

To do this, you will need to use the variables $1 and $2 in your code. Remember that in a script, variables of this type represent arguments that are typed on the command line after the command’s name, when the script is launched.

4.	Write a Bash script called testmark that allows a user to enter a test score and what the test was out of. The script should then calculate and show the percentage derived from the score and the score’s maximum. After this, the script should write out “Pass” if the percentage is greater than or equal to 50, and “Fail” if the percentage is less than 50. Also, the script should write “Invalid” if the percentage is either greater than 100 or less than zero. Hint: you should use if…elif… to do this.

5.	Write a Bash script called options that shows a menu of three options to the user. The user will choose one of the options, and the script should then do the action corresponding to the option. The three options are:
a.	Count the number of words in a file, whose name will be given by the user.
b.	Display the current date and time.
c.	Display the list of users who are currently logged on to the computer (hal).
To do this, you will need to use the case instruction. For each option, you will need to determine which Linux instructions should be performed to provide the appropriate result. Note: if the user chooses an invalid option, the script should display an error message.

6.	Write a Bash script called nowseconds that calculates the number of seconds elapsed today:
Number of seconds elapsed today: 23532 seconds.
To do this, you will have to determine the hour, minute and second of the time of day that the script is being executed. To access the hour number of the current time, you can use date '+%H' (and similarly for Minutes and Seconds). Remember that you can assign the result of a Linux command to a variable if you enclose the command in backquotes. Here is an example:
hours=`date '+%H'`
This will determine the current hour, and assign this number to hours. After you do this for minutes and seconds as well, you can use a formula to compute the total number of seconds.

7.	Write a Bash script called runnable which asks the user to enter a file name, and then checks to see if the file has execute permission. The script should then display whether or not this is so. If the name given does not correspond to an existing file, the script should show an error message. After the script has done this for one file, it should allow the user to do this again. The script should loop until the user no longer wants to continue.

I suggest you do this without using a loop first. To do the checking for just one file, you will need to use if…elif in combination with the file condition codes that determine if a file exists and if it has execute permission. After you have this working correctly, enclose your code with a while or until loop that will allow the user to choose whether to repeat the script.

8.	Write a Bash script called canedit that displays the names of the files in the current directory that have write permission (permission being for the file owner). For example, output from the script might look like:
Writable files:
makelist
nowseconds
toggle
To do this, you should use a for loop that loops through all the files in the directory. For example:
for filename in * ; do
done
The asterisk is the wildcard meaning “the list of all files in the directory”. The for loop therefore repeats as many times as there are files in the directory, and each time it loops, the variable called filename takes on the value of the next file in the directory. Within the loop, you can use an if instruction to check the “write” permission for filename. If the permission is enabled, the script can simply write out the value of filename.
