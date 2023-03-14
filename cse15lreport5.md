# Lab 7 Report w/ Bash Script:


## Step 4: Logging into ieng6:
![image](https://user-images.githubusercontent.com/122490362/221730943-72c948c4-3e4a-4fa3-a283-6629af7e3ead.png)
```
Keys:<Up><Enter>
```
The `<Up>` key brought up the ssh command, which was the last command used locally, and after hitting `<Enter>`, I was logged into ieng6.

## Bash Script: comp.sh
```
CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"

git clone git@github.com:algaoucsd/lab7.git
cd lab7/
javac -cp $CPATH *.java
java -cp $CPATH org.junit.runner.JUnitCore ListExamplesTests
```
## Steps 5-6:

![image](https://user-images.githubusercontent.com/122490362/224881280-4b5c62e7-fc18-4098-918e-15c40b718dcc.png)

```
Keys:bash c<Tab><Enter>
```
I run the above bash script to clone the git repository, then compile and run the failing tests. 

## Step 7: Editing the Code
![image](https://user-images.githubusercontent.com/122490362/221734719-bd037680-6ed9-4d79-b13d-5161ead43f24.png)

```
Keys: cd l<tab><Enter> vim List<Tab><Enter> i <Right><Backspace> 2 <Esc> <Shift>+: wq <Enter>
```
I first cd into the lab7 folder so I can then proceed to edit the code. The vim command is to open up vim so I can edit the code and fix the bug. Everything after it, and before the `<Esc>` is to move my cursor over and turn `index1` into `index2`. The rest is to save the edits and exit vim to go back to the console.

## Bash Script: finish.sh

```
CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"

cd lab7/
javac -cp $CPATH *.java
java -cp $CPATH org.junit.runner.JUnitCore ListExamplesTests
git add ListExamples.java
git commit -m "Fixed"
git push
```


## Steps 8-9:
![image](https://user-images.githubusercontent.com/122490362/224882777-3814d59a-51a7-4943-b776-339ef8522330.png)

```
cd ..<Enter> bash f<Tab><Enter>
```

First I cd out of the lab7 folder so I can run the second bash script. Then I run the bash script to recompile and run the now correct tests. Then it adds the edited code to the commit, commits, then pushes the commit.
