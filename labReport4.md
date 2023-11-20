** Step 4: Log into ieng6 **

![step 4](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/46c01894-1108-4edb-a998-1b546dcd4913)

Keys pressed: ssh cs15lfa23hw@ieng6.uscd.edu ```<Enter>```. I had to type in the ssh command along with my course-specific account and then clicked enter 
in order to ssh into my account. 

** Step 5: Clone your fork of the repository from your Github account (using the SSH URL) **

![step 5](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/8ea95401-0d5f-4fe2-80f2-143982d1eb08)

Keys pressed: ```Ctrl-C```, typed ```git clone```, ```Ctrl-V```, ```Enter```. I first had to use ```Ctrl-C``` to copy the SSH URL from my Github account.
I then typed the git clone commnad to be able to clone the repository. I then used ```Ctrl-V``` to paste the command and clicked ```Enter``` to run it.

** Step 6: Run the tests, demonstrating that they fail **

![step 6](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/29ab0f71-d207-4e7d-9fb8-b08676fbb3c1)

Keys pressed: Typed cd lab7, typed ```bash``` test.sh. I first had to cd into lab7 to be able to run the tests. Next I had to use the bash command to run the 
tests in test.sh.

** Step 7: Edit the code file to fix the failing test **

![step 7 part 1](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/699c72de-1a1f-414d-be5c-dd85cdbdaf09)

Keys pressed: Typed ```vim ListExamples.j```, ```<tab>```, and ```<Enter>```. I first typed ```vim``` to enter editing mode, I then began typing out ListExamples.java 
but stopped at the j and clicked ```tab``` to autocomplete the rest of the name. I then clicked ```Enter``` to run the command.

![step 7 part 2](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/6b918d22-49b9-4646-9b05-241cfd574c48)

Keys pressed: ```4k```, ```2L```, ```x```, ```i```, ```2```, ```<esc>``` ```:wq```, ```<Enter>```. I first used ```4k``` to move my cursor up 4 spaces to the line that contains the varaible
name that we are trying to change. I next used ```2L``` to move the cursor to the left 2 spaces to get to th 1 in index1. Next I clicked ```x``` to delete the 1 that
my cursor was currently on. I then clicked ```i``` to enter insert mode, after this I typed a ```2``` to insert a 2 there. Next, I clicked ```<esc>``` to exit insert mode.
I then typed ```:wq``` and clicked ```<Enter>``` to save and exit.

**Step 8: Run the tests, demonstrating that they now succeed **

![part 8](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/0a44e021-1284-43cc-9f98-f1f08f8c88fd)

Keys presssed: ```<up> <up> <Enter>```. I clicked ```<up>``` two times because the bash test.sh command which runs the tests was two spaces up in my history. I then clicked ```<Enter>```
to run the command.

**Step 9: Commit and push the resulting change to your Github account **

![part 9](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/a30c7123-f846-49f1-bfeb-3f3b73eb2bf9)

Keys pressed: Typed ``` git add ListExamples.j ``` ```<tab>```, ```<Enter>```, Typed ```git commit -m "updated"```, ```<Enter>```, typed ```git push```, ```<Enter>```.

I typed ``` git add ListExamples.j ``` and later clicked ```<tab>``` and ```<Enter>``` to autocomplete the name of the file. This stages the file to be a part of the next 
commit. I next typed ```git commit -m "updated"``` and clicked ```<Enter>``` to create a commit for my updated file. Finally, I typed ```git push``` and ```<Enter>```
to push (copy) all of the commits to my GitHub account. 





