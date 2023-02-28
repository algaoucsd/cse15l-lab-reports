# Lab 7 Report:

## Step 4: Logging into ieng6:
![image](https://user-images.githubusercontent.com/122490362/221730943-72c948c4-3e4a-4fa3-a283-6629af7e3ead.png)
```
Keys:<Up><Enter>
```
The `<Up>` key brought up the ssh command, which was the last command used locally, and after hitting `<Enter>`, I was logged into ieng6.

## Step 5: Cloning the Repository:
![image](https://user-images.githubusercontent.com/122490362/221732380-91fa6dc4-41bf-4d46-822b-a9ff868a345e.png)
```
Keys:git clone <Ctrl>+<Shift>+V <Enter>
```
I typed out the beginning of git clone then pasted what I copied from the SSH section of the clone on github.

## Step 6: Running Failing Tests
![image](https://user-images.githubusercontent.com/122490362/221733540-c3063759-0581-4b98-a145-eb968a1e29de.png)
```
Keys: cd la <Tab>, <Up><Up><Up><Up><Up><Up><Up><Up><Up><Up><Enter>, <Up><Up><Up><Up><Up><Up><Up><Up><Up><Up><Enter>
```
The first command cds me into the lab7 folder generated off of the git clone. Then, i hit the `<Up>` 10 times and hit `<Enter>` to execute the compile command `javac -cp ".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar" *.java` , then to actually run the tests I did the same thing to run the command `java -cp ".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar" org.junit .runner.JUnitCore ListExamplesTests`.

## Step 7: Editing the Code
![image](https://user-images.githubusercontent.com/122490362/221734719-bd037680-6ed9-4d79-b13d-5161ead43f24.png)

```
Keys: vim List<Tab><Enter> i <Right><Backspace> 2 <Esc> <Shift>+: wq <Enter>
```
The vim command is to open up vim so I can edit the code and fix the bug. Everything after it, and before the `<Esc>` is to move my cursor over and turn `index1` into `index2`. The rest is to save the edits and exit vim to go back to the console.

## Step 8: Running Passing Tests
![image](https://user-images.githubusercontent.com/122490362/221739456-eb954324-1f4d-47ef-9bd2-a515e631abb2.png)
```
Keys:<Up><Up><Up><Enter>, <Up><Up><Up><Enter>
```
Like Step 6, the `<Up>` keys are to run the same commands in the same order. But this time, it's significantly less key presses because we used the commands in Step 6.

## Step 9: Commit and Push
![image](https://user-images.githubusercontent.com/122490362/221741430-7b36d6e7-4967-42e4-9975-b26a9dfe7da6.png)

```
git add List<Tab>.j<Tab><Enter>, git commit -m "Fixed" <Enter>, git push <Enter>
```
The first command is to add the edited file `ListExamples.java` to the files needed to commit changes. The tabs were to autocomplete the file names. Then I just commited the added files with the message "Fixed" and then pushing the commited changes.
