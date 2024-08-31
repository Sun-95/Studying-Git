<h1>Part I: Git basics<h1>
<h2>2. Creating a project</h2>
<h3>1) Create a “Hello, World!” page</h3>
<p>I started with an empty directory and added an empty subdirectory called work and then created a hello.html file in it. <a href="screenshots/2.1.png">Screenshot 2.1</a></p>

<h3>2) Create a repository</h3>
<p>So there is a directory that contains one file. Ran git init to create a Git repository from this directory. <a href="screenshots/2.2.png)">Screenshot 2.2</a></p>

<h3>3) Add the page to the repository</h3>
<p>Now let's add the “Hello, World” page to the repository. <a href="screenshots/2.3.png)">Screenshot 2.3</a></p>

<h2>3. Checking the status of the repository</h2>
<h3>1) Check the status of the repository</h3>
<p>Use the git status command, to check the current state of the repository.<a href="screenshots/3.1.png)">Screenshot 3.1</a></p>

<h2>4. Making changes</h2>
Goals
Learn to monitor the working directory’s state.
01Changing the “Hello, World” page
Let's add some HTML-tags to our greeting. Change the file contents to:

File: hello.html
<h1>Hello, World!</h1>
02Checking the status
Check the working directory’s status.

Run
git status
You will see:

Result
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   hello.html

no changes added to commit (use "git add" and/or "git commit -a")
The first important aspect here is that Git knows hello.html file has been changed, but these changes are not yet committed to the repository.

Another aspect is that the status message hints about what to do next. If you want to add these changes to the repository, use git add. To undo the changes use git checkout.
