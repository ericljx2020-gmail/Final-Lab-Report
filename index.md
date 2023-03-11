# Lab Report 5
---
This is the report about how to make a grade.sh autograder using the skill we learned in this quarter comprehensively.

1. First make a fork of the repository contain the starter code for grade.sh
<img width="1509" alt="image" src="https://user-images.githubusercontent.com/68884486/224475808-6a6a5a73-4455-4a28-b3e1-fec4deec698c.png">

2. Copy the link over here to use git clone command to clone into github repository.
<img width="1511" alt="image" src="https://user-images.githubusercontent.com/68884486/224475908-5edb2fe1-25f9-40a8-984e-7274659d4088.png">

3. Run command `git clone git@github.com:ericljx2020-gmail/list-examples-grader.git` to clone into the repository

4. We can see that we have a grade.sh file in the working directory. We now have to open it in vscode to modify the file.

5. First, we need to handle the case that if the file does not exist in the student-submission. What we do is that we use a if statement to check if file
exist using `-e` statement. If the file exists in the correct directory, we print "FILE FOUND" and proceed. Else if the file exists but not in correct
directory, we put "FILE NOT IN CORRECT DIRECTORY" to the terminal. The corresponding code is shown below:
<img width="960" alt="image" src="https://user-images.githubusercontent.com/68884486/224476269-bcff0ff3-84e5-44cb-a42c-a0ce84a6fff6.png">

6. After dealing with whether the file exist or not, now we need to checki if the java file can be compile successfully or it has any compile error. If so
what is the specific error in it. This will involves a command we learnt in lab report 3 -- `grep` and its extension of `grep -q`. This argument ignore the
output of grep and return a single exit status of whether the pattern is found in error.log file. The implementation of this step is shown in the image below.
<img width="635" alt="image" src="https://user-images.githubusercontent.com/68884486/224476590-6075b260-54ac-435a-a468-4f12b331724c.png">

7. After running this file for all examples given in the lab task, we see that all of them are running well.
