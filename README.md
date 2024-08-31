<h1>Part I: Git basics<h1>

<h2>2. Creating a project</h2>
<h3>1) Create a “Hello, World!” page</h3>
I started with an empty directory and added an empty subdirectory called work and then created a hello.html file in it. <a href="screenshots/2.1.png">Screenshot 2.1</a>
<h3>2) Create a repository</h3>
So there is a directory that contains one file. Ran git init to create a Git repository from this directory. <a href="screenshots/2.2.png)">Screenshot 2.2</a>
<h3>3) Add the page to the repository</h3>
Now let's add the “Hello, World” page to the repository. <a href="screenshots/2.3.png)">Screenshot 2.3</a>

<h2>3. Checking the status of the repository</h2>
<h3>1) Check the status of the repository</h3>
Use the git status command, to check the current state of the repository. <a href="screenshots/3.1.png)">Screenshot 3.1</a>

<h2>4. Making changes</h2>
<h3>1)Checking the status</h3>
Check the working directory’s status. <a href="screenshots/4.1.png)">Screenshot 4.1</a> The first important aspect here is that Git knows hello.html file has been changed, but these changes are not yet committed to the repository.

<h2>5. Staging the changes</h2>
<h3>1)Adding changes</h3>
Now command Git to stage changes. Check the status. <a href="screenshots/5.1.png)">Screenshot 5.1</a> Changes to the hello.html have been staged. This means that Git knows about the change, but it is not permanent in the repository. The next commit will include the changes staged.

<h2>6. Staging and committing</h2>
I edited three files (a.html, b.html and c.html). After that, you need to commit all the changes so that the changes in a.html and b.html are a single commit <a href="screenshots/6.1.png)">Screenshot 6.1</a>, and the changes in c.html are not logically related to the first two files and are made in a separate commit. <a href="screenshots/6.2.png)">Screenshot 6.2</a>

<h2>7. Committing the changes</h2>
<h3>1) Committing changes. Checking the status</h3>
Let us commit now and check the status. <a href="screenshots/7.1.png)">Screenshot 7.1</a> The working directory is clean, you can continue working.

<h2>8. Changes, not files</h2>
<h3>1) First Change: Adding default page tags</h3>
Change the "Hello, World" page so that it contained default tags <html> and <body>. <a href="screenshots/8.1.png)">Screenshot 8.1</a>
<h3>2) Add this change</h3>
Now add this change to the Git staging. <a href="screenshots/8.2.png)">Screenshot 8.2</a>
<h3>3) Second change: Add the HTML headers</h3>
Now add the HTML headers (<head> section) to the "Hello, World" page. <a href="screenshots/8.3.png)">Screenshot 8.3</a>
<h3>4) Check the current status</h3>
<a href="screenshots/8.4.png)">Screenshot 8.4</a>
<h3>5) Commit
Commit the staged changes, then check the status one more time. <a href="screenshots/8.5.png)">Screenshot 8.5</a> The status command suggests that hello.html still has unrecorded changes, but the staging area is already clear.
<h3>6) Adding the second change</h3>
Add the second change to the staging area, after that run the git status command. <a href="screenshots/8.6.png)">Screenshot 8.6</a>
<h3>7) Commit the second change</h3>
<a href="screenshots/8.7.png)">Screenshot 8.7 </a>

<h2>9. History</h2>
Getting a list of changes made is a function of the git log command.
