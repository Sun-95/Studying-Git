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
Getting a list of changes made is a function of the git log command. <a href="screenshots/9.0.png)">Screenshot 9.0</a>
<h3>1) One line history</h3>
You have full control over how the log is displayed. The one-line format helps show this. <a href="screenshots/9.1.png)">Screenshot 9.1</a>
<h3>2) Controlling the display of entries</h3>
Here are some other interesting options for viewing history:
<a href="screenshots/9.2.1.png)">Screenshot 9.2.1</a>
<a href="screenshots/9.2.2.png)">Screenshot 9.2.2</a>
<a href="screenshots/9.2.3.png)">Screenshot 9.2.3</a>
<a href="screenshots/9.2.4.png)">Screenshot 9.2.4</a>
<a href="screenshots/9.2.5.png)">Screenshot 9.2.5</a>
<h3>3) Getting fancy</h3>
This is what you should use to view changes made in the last week. I added --author=Svitlana if I want to see only my changes. <a href="screenshots/9.3.png)">Screenshot 9.3</a>
<h3>4) The ultimate format of the log</h3>
The following log format is most appropriate. <a href="screenshots/9.4.1png)">Screenshot 9.4.1</a>
Every time you want to see a log, you'll have to do a lot of typing. Fortunately, there are several Git config options to adjust the default log output format. <a href="screenshots/9.4.2png)">Screenshot 9.4.2</a>

<h2>10. Getting older versions</h2>
<h3>1) Getting hashes of the previous commit</h3>
<a href="screenshots/10.1.1.png)">Screenshot 10.1.1</a>
Check the log data and find the hash of the initial commit. <a href="screenshots/10.1.2.png)">Screenshot 10.1.2</a>
<h3>2) Returning to the latest version in the main branch</h3>
To return to the latest version of our code, we need to switch to the default main branch. We can use the switch command to switch between branches.<a href="screenshots/10.2.png)">Screenshot 10.2</a>

<h2>11. Tagging versions</h2>
<h3>1) Creating a tag for the first version</h3>
<a href="screenshots/11.1.png)">Screenshot 11.1</a>
<h3>2) Tags for previous versions</h3>
Let's tag the version prior to the current version with the name v1-beta. First of all we will check out the previous version. Instead of looking up the hash of the commit, we are going to use the ^ notation, specifically v1^, indicating the commit previous to v1. <a href="screenshots/11.2.1.png)">Screenshot 11.2.1</a>
This is the version with <html> and <body> tags, but without <head>. Let's make it’s the v1-beta version. <a href="screenshots/11.2.2.png)">Screenshot 11.2.2</a>
<h3>3) Check out by the tag name</h3>
Now try to check out between the two tagged versions. <a href="screenshots/11.3.png)">Screenshot 11.3</a>
<h3>4) Viewing tags with the tag command</h3>
You can see the available tags using the git tag command.
<h3>5) Viewing tags in logs</h3>
You can also check for tags in the log. <a href="screenshots/11.5.png)">Screenshot 11.5</a>

<h2>12. Discarding local changes (before staging)</h2>
<h3>1) Change hello.html</h3>
Make changes to the hello.html file in the form of an unwanted comment. 
<h3>2) Check the status</h3>
First of all, check the working directory’s status. <a href="screenshots/12.2.png)">Screenshot 12.2</a> We see that the hello.html file has been modified, but not staged yet.
<h3>3) Undoing the changes in the working directory</h3>
Use the checkout command in order to check out the repository's version of the hello.html file. <a href="screenshots/12.3.png)">Screenshot 12.3</a> The status command shows there were no unstaged changes in the working directory. And the "bad comment" is no longer contained in the file.

<h2>13. Cancel staged changes (before committing)</h2>
<h3>1) Edit file and stage changes</h3>
Make changes to the hello.html file in the form of an unwanted comment. <a href="screenshots/13.1.png)">Screenshot 13.1</a>
<h3>2) Check the status</h3>
Stage the modified file. Check the status of unwanted changes. <a href="screenshots/13.2.png)">Screenshot 13.2</a> Status shows that the change has been staged and is ready to commit.
<h3>3) Reset the staging area</h3>
The reset command resets the staging area to HEAD. This clears the staging area from the changes that we have just staged. <a href="screenshots/13.3.png)">Screenshot 13.3</a> The reset command (default) does not change the working directory. Therefore, the working directory still contains unwanted comments. 
<h3>4) Switch to commit version</h3>
We can use the checkout command to remove unwanted changes from working directory. <a href="screenshots/13.4.png)">Screenshot 13.4</a>







