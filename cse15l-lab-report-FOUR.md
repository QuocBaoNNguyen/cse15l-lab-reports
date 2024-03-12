# CS15L Lab Report 4
## Step 4
**Screenshot**

<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/c87c18a4-ee96-4240-898c-551f9835c2f2)

<br/>

**Keys Pressed**

<br/>

`ssh qun008@ieng6.ucsd.edu`, `<enter>`

<br/>

**Summary**

<br/>

I typed out `ssh qun008@ieng6.ucsd.edu` and then pressed `<enter>` to log into my ieng6 and complete step 4.

<br/>

## Step 5

**Screenshot**

<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/8f39987b-782f-416b-b286-7137acf4b535)

<br/>

**Keys Pressed**

<br/>

`git clone git@github.com:QuocBaoNNguyen/lab7.git`, `<enter>`

<br/>

**Summary**

<br/>

After setting up the SSH key in my GitHub account, I typed out 
`git clone` and `git@github.com:QuocBaoNNguyen/lab7.git`(from my fork) then pressed `<enter>`. This cloned the forked repository.

<br/>

## Step 6
**Screenshot**
<br/>
![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/8317f078-2700-4c7f-b81f-b619b9d87a9e)


<br/>

**Keys Pressed**

<br/>

`cd lab7`, `<enter>`

<br/>

`<Ctrl+V>`, `<enter>`

<br/>

`<Ctrl+V`, `<enter>`

<br/>

**Summary**

<br/>

By typing out `cd lab7`, `<enter>`, I changed my working directory to `lab7`. With `javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar ListExamplesTests.java`, `<enter>`, I compiled the `ListExamplesTests` file. Lastly, `java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore ListExamplesTests`, `<enter>`, ran the file `ListExamplesTests.java` and gave me the results of the test.

<br/>

## Step 7
**Screenshot**
<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/6f043cd9-9307-4428-8758-7a6baf14c0f0)

<br/>


![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/66dba0f9-1b4b-4750-b493-e905fae3ec7f)

<br/>

**Keys Pressed**

<br/>

`vim ListExamples.java`, `<enter>`

<br/>

`<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<down>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` `<right>` 

<br/>

`i` `<backspace>` `2` `<esc>`

<br/>

`:wq` `<enter>`

<br>

**Summary**

<br/>

I used `vim ListExamples.java`, `<enter>` to open `ListExamples.java` in `vim`. Then, the 43 `<down>`s and 12 `<right>`s are to place my cursor at the desired position at where I want to make my changes. The `i` `<backspace>` `2` `<esc>` are to switch into "insert mode" in `vim`, delete the `1` and replace it with a `2` and `<esc>` is to exit out of "insert mode". Lastly, `:wq` `<enter>` saves the changes and quits `vim`.

<br/>

## Step 8

**Screenshot**

<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/4bc9b3dc-77fa-4671-8b6b-8e3b06a96c17)


<br/>

 **Keys Pressed**

<br/>

`javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar ListExamplesTests.java`, `<enter>`

<br/>

`java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore ListExamplesTests`, `<enter>`

<br/>

**Summary**

<br/>

With `javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar ListExamplesTests.java`, `<enter>`, I recompiled the `ListExamplesTests` file. Then, `java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore ListExamplesTests`, `<enter>`, ran the file `ListExamplesTests.java` and gave me the results of the test.

<br/>

## Step 9
**Screenshot**

<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/f63d0302-1800-4b75-93a0-19b1306c9ebc)

<br/>

**Keys Pressed**

<br/>

`git add .`, `<enter>`

<br/>

`git commit -m "ListExamples Fixed"`, `<enter>`

<br/>

`git push`, `<enter>`

<br/>

**Summary**

<br/>

This, `git add .`, `<enter>`, stages all changes in the working directory and also it's subdirectories (because of the `.`) for the next commit. What is staging? Staging means to mark the files and all changes within them as ready to be included in the next commit. Then, `git commit -m "ListExamples Fixed"`, `<enter>`, commits the staged changes(from the previous command) to the local repository. Notice the `-m`, this allows for a commit message to be included! Lastly, is the `git push`, `<enter>`. This command pushes the committed changes from the local repository to a remote repository.










