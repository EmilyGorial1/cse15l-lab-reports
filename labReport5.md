**The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is**
Hi, I am having an issue with my script. It seems to say that the submission is not a file when it indeed is. I passed in a student file which I know should receive full credit as the argument to my script so that it can be graded.I am not sure why the script says that it is not a file. Can I please get some help with this? Here is my script and the output that I get from grading the student submission.

![grading script](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/b76101f7-7988-4fbc-801c-6c74c9a4e622)

![lab 5 symptom](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/bc7f538a-7875-486d-a3bf-b469b05e6d9d)


**A response from a TA asking a leading question or suggesting a command to try**

Hello, there, I would recommend looking into your conditional in the if statement that checks if the submission is a file or not. Hope this helps

**Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is**

Ohhh, I think I have found the issue. Within my grading script, I have a conditional that chekcs if the submission is a file or not. While, I thought that my conditional was checking if the submission was not a file, it was actually checking if it was a file (the opposite of what I wanted). So basically, my if statement was checking if the submission is a file, and if it was a file, it would say that it is not a file. This is the opposite of what I want. To negate this, and make it work the way that it is supposed to, I will include an exclamation point before my conditional statment. This way, it will evaluate to true if the submission is indeed not a file, and then display the message, "submission is not a file." Here is a screenshot of my corrected script along with the expected output. Thank you for your help!

![corrected script](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/c6462290-b482-471f-863d-707d62ce3075)

![proper outcome](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/31fc8002-a8df-4936-95b9-238e0c2a6151)

**The file and directory structure needed**

The ``` /lib ``` file in our directory contains the file and directory structure needed. This directory contains ``` hamcrest-core-1.3.jar ``` and ``` junit-4.13.2.jar ``` 
These allow us to run the junit test. grade.sh is the script that tests the student submissions. The student submission I passed in as an argument to my script is 
https://github.com/ucsd-cse15l-f22/list-methods-corrected

![file and directory structure needed](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/1560251c-f98c-42a2-b6e7-67305ef79ff7)

**The contents of the file before fixing the bug**

![grading script](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/2febf36f-ce38-4eaf-8b34-1be39135ea9f)

**The full command line that I ran to trigger the bug**

``` bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-corrected ```

**A description of what to edit to fix the bug**

After looking through my script more carefully, I realized that my conditional in the if statement was actually evaluating to true when it was supposed to be evaluating to false. In the beginning, the conditional basically evaluated to true if the argument passed in was a file, and then it proceeded to display a message that the submission was not a file. This is because I was missing an exclamation point in my conditional statement. I changed the conditional statement from ``` if[[ -e  $files ]] ``` to ``` if[[ ! -e $files ]] ```. This way, it evaluates to true if the submission is not a file, and then displays the message "submission is not a file."

**Reflection**
Something I learned from my lab experience in the second half of the quarter was Vim. I had never previously worked with Vim and honestly never imagined that something like it even existed. Entering the class, I was very unfamiliar with working at the command line as I had only ever done it a handful of times where I was directed on exactly what to do by a teacher. I then became more comfortable with working at the command line as the course progressed, but only within certain bounds. I never imagined that we would be able to edit files from the command line. Vim gave me a whole new appreciation for working in the terminal, as I realized how powerful it is. So much can be done just by working in the terminal. 

