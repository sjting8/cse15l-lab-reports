# **Lab Report 4**
By: Sean Ting

## Step 1
Log into ieng6

![Image](LogIn.png)

**Keys Pressed:** ```<up><enter>```
ssh command is used to log into a remote server (ieng6). ```ssh cs15lwi23aum@ieng6.ucsd.edu``` was the most recent command in the terminal so the up arrow copied it into the current command line and enter entered it into the terminal. This did not prompt me for a password since I set it up to automatically logged me in.

## Step 2
Clone your fork of the repository from your Github account

![Image](git clone lab7.png)

**Keys Pressed:** ```git clone <ctrl-V><enter>```
I copied the SSH key to clone the repository from the Github website to my clipboard. I then went to my terminal, typed "git clone" and then pressed ctrl-V to paste the SSH key of the forked repository and pressed enter to complete the cloning the repository.

## Step 3
Run the tests, demonstrating that they fail
![Image](git clone lab7.png)

**Keys Pressed:** ```cd lab7 <enter>```

Compile and run Junit Tests
![Image](TestFail.png)


**Keys pressed:** ```<up><up><up><up><up><enter>, <up><up><up><up><up><enter>```

The ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` command was 5 commands up in the search history, so I used up arrow to access it and enter to reinput it. Then the ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` command was 5 up in the history, so I accessed and ran it in the same way.
  
The first javac command compiles files with junit and the second java command runs the junit tests.
  
## Step 4
Edit the code file to fix the failing test

*Enter nano command (nano `<enter>`)*

This opens up the nano window
  
`<Ctrl-R ListExamples.java>`

This reads the ListExamples.java file.

![Image](ListExamplesRead.png)

Use arrow keys to find in the code and change the first occurrence of index1+=1; (the most bottom one) to index2+=1;
  
`<Ctrl-O ListExamples.java>` and then `<y>` to overwrite. This replaces the old file with the new edited one.
  
`<Ctrl-X>` to exit nano.
 
## Step 5
Run the tests, demonstrating that they now succeed

![Image](TestPass.png)

**Keys Pressed:** `<up><up><enter>`

Accesses and runs the JUnit test command.

Should now show that all the test pasts.

## Step 6
Commit and push the resulting change to your Github account (you can pick any commit message!)

![Image](CommitPush.png)


**Keys Pressed:** ```git commit -a Bug Fixed <esc> :wq```
```git push```

I used the command "git commit -a" to commit all changes made to the directory. "Bug Fixed" was the message to the commit and pressed escape and typed ":wq" to save the changes. Finally, I used the command '''git push''' to push all changes to the repository. 
