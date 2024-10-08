# Part I: Git Basics

## 2. Creating a Project

### 1) Create a “Hello, World!” Page
I started with an empty directory and added an empty subdirectory called `work`, then created a `hello.html` file in it.  
![Screenshot 2.1](./screenshots/2.1.png)

### 2) Create a Repository
So there is a directory that contains one file. I ran `git init` to create a Git repository from this directory.  
![Screenshot 2.2](./screenshots/2.2.png)

### 3) Add the Page to the Repository
Now let's add the “Hello, World!” page to the repository.  
![Screenshot 2.3](./screenshots/2.3.png)

## 3. Checking the Status of the Repository

### 1) Check the Status of the Repository
Use the `git status` command to check the current state of the repository.  
![Screenshot 3.1](./screenshots/3.1.png)

## 4. Making Changes

### 1) Checking the Status
Check the working directory’s status.  
![Screenshot 4.1](./screenshots/4.1.png)  
The first important aspect here is that Git knows the `hello.html` file has been changed, but these changes are not yet committed to the repository.

## 5. Staging the Changes

### 1) Adding Changes
Now command Git to stage changes. Check the status.  
![Screenshot 5.1](./screenshots/5.1.png)  
Changes to the `hello.html` file have been staged. This means that Git knows about the change, but it is not permanent in the repository. The next commit will include the changes staged.

## 6. Staging and Committing

I edited three files (`a.html`, `b.html`, and `c.html`). After that, you need to commit all the changes so that the changes in `a.html` and `b.html` are a single commit.  
![Screenshot 6.1](./screenshots/6.1.png)  
The changes in `c.html` are not logically related to the first two files and are made in a separate commit.  
![Screenshot 6.2](./screenshots/6.2.png)

## 7. Committing the Changes

### 1) Committing Changes. Checking the Status
Let us commit now and check the status.  
![Screenshot 7.1](./screenshots/7.1.png)  
The working directory is clean, and you can continue working.

## 8. Changes, Not Files

### 1) First Change: Adding Default Page Tags
Change the "Hello, World" page so that it contains default tags `<html>` and `<body>`.  
![Screenshot 8.1](./screenshots/8.1.png)

### 2) Add This Change
Now add this change to the Git staging.  
![Screenshot 8.2](./screenshots/8.2.png)

### 3) Second Change: Add the HTML Headers
Now add the HTML headers (`<head>` section) to the "Hello, World" page.  
![Screenshot 8.3](./screenshots/8.3.png)

### 4) Check the Current Status
![Screenshot 8.4](./screenshots/8.4.png)

### 5) Commit
Commit the staged changes, then check the status one more time.  
![Screenshot 8.5](./screenshots/8.5.png)  
The status command suggests that `hello.html` still has unrecorded changes, but the staging area is already clear.

### 6) Adding the Second Change
Add the second change to the staging area, and then run the `git status` command.  
![Screenshot 8.6](./screenshots/8.6.png)

### 7) Commit the Second Change
![Screenshot 8.7](./screenshots/8.7.png)

## 9. History

Getting a list of changes made is a function of the `git log` command.  
![Screenshot 9.0](./screenshots/9.0.png)

### 1) One Line History
You have full control over how the log is displayed. The one-line format helps show this.  
![Screenshot 9.1](./screenshots/9.1.png)

### 2) Controlling the Display of Entries
Here are some other interesting options for viewing history:  
![Screenshot 9.2.1](./screenshots/9.2.1.png)  
![Screenshot 9.2.2](./screenshots/9.2.2.png)  
![Screenshot 9.2.3](./screenshots/9.2.3.png)  
![Screenshot 9.2.4](./screenshots/9.2.4.png)  
![Screenshot 9.2.5](./screenshots/9.2.5.png)

### 3) Getting Fancy
This is what you should use to view changes made in the last week. I added `--author=Svitlana` if I want to see only my changes.  
![Screenshot 9.3](./screenshots/9.3.png)

### 4) The Ultimate Format of the Log
The following log format is most appropriate.  
![Screenshot 9.4.1](./screenshots/9.4.1.png)  
Every time you want to see a log, you'll have to do a lot of typing. Fortunately, there are several Git config options to adjust the default log output format.  
![Screenshot 9.4.2](./screenshots/9.4.2.png)

## 10. Getting Older Versions

### 1) Getting Hashes of the Previous Commit
![Screenshot 10.1.1](./screenshots/10.1.1.png)  
Check the log data and find the hash of the initial commit.  
![Screenshot 10.1.2](./screenshots/10.1.2.png)

### 2) Returning to the Latest Version in the Main Branch
To return to the latest version of our code, we need to switch to the default main branch. We can use the `switch` command to switch between branches.  
![Screenshot 10.2](./screenshots/10.2.png)

## 11. Tagging Versions

### 1) Creating a Tag for the First Version
![Screenshot 11.1](./screenshots/11.1.png)

### 2) Tags for Previous Versions
Let's tag the version prior to the current version with the name `v1-beta`. First of all, we will check out the previous version. Instead of looking up the hash of the commit, we are going to use the `^` notation, specifically `v1^`, indicating the commit previous to `v1`.  
![Screenshot 11.2.1](./screenshots/11.2.1.png)  
This is the version with `<html>` and `<body>` tags, but without `<head>`. Let's make it the `v1-beta` version.  
![Screenshot 11.2.2](./screenshots/11.2.2.png)

### 3) Check Out by the Tag Name
Now try to check out between the two tagged versions.  
![Screenshot 11.3](./screenshots/11.3.png)

### 4) Viewing Tags with the Tag Command
You can see the available tags using the `git tag` command.
![Screenshot 11.4](./screenshots/11.4.png)

### 5) Viewing Tags in Logs
You can also check for tags in the log.  
![Screenshot 11.5](./screenshots/11.5.png)

## 12. Discarding Local Changes (Before Staging)

### 1) Change hello.html
Make changes to the `hello.html` file in the form of an unwanted comment.
![Screenshot 12.1](./screenshots/12.1.png)  

### 2) Check the Status
First of all, check the working directory’s status.  
![Screenshot 12.2](./screenshots/12.2.png)  
We see that the `hello.html` file has been modified, but not staged yet.

### 3) Undoing the Changes in the Working Directory
Use the `checkout` command in order to check out the repository's version of the `hello.html` file.  
![Screenshot 12.3](./screenshots/12.3.png)  
The status command shows there were no unstaged changes in the working directory, and the "bad comment" is no longer contained in the file.

## 13. Cancel Staged Changes (Before Committing)

### 1) Edit File and Stage Changes
Make changes to the `hello.html` file in the form of an unwanted comment.  
![Screenshot 13.1](./screenshots/13.1.png)

### 2) Check the Status
Stage the modified file. Check the status of unwanted changes.  
![Screenshot 13.2](./screenshots/13.2.png)  
The status shows that the change has been staged and is ready to commit.

### 3) Reset the Staging Area
The `reset` command resets the staging area to `HEAD`. This clears the staging area from the changes that we have just staged.  
![Screenshot 13.3](./screenshots/13.3.png)  
The `reset` command (default) does not change the working directory. Therefore, the working directory still contains unwanted comments.

### 4) Switch to Commit Version
We can use the `checkout` command to remove unwanted changes from the working directory.  
![Screenshot 13.4](./screenshots/13.4.png)

## 14. Cancelling Commits

### 1) Edit the File and Make a Commit
Replace `hello.html` with the following file.  
![Screenshot 14.1.1](./screenshots/14.1.1.png)  
![Screenshot 14.1.2](./screenshots/14.1.2.png)

### 2) Make a Commit with New Changes that Discard Previous Changes
To cancel the commit, we need to create a commit that deletes the changes saved by the unwanted commit.  
![Screenshot 14.2](./screenshots/14.2.png)

### 3) Check the Log
Checking the log shows the unwanted cancellations and commits in our repository.  
![Screenshot 14.3](./screenshots/14.3.png)

## 15. Removing a Commit from a Branch

### 1) Mark This Branch First
Let us do a quick scan of our commit history. Let us mark the last commit with a tag, so you can find it after removing a commit(s).  
![Screenshot 15.1](./screenshots/15.1.png)

### 2) Reset Commit to Before Oops
As the branch has a tag, we can use the tag name in the reset command.  
![Screenshot 15.2](./screenshots/15.2.png)  
Our main branch is pointing at commit `v1`, and the "Revert Oops" and "Oops" commits no longer exist in the branch. The `--hard` parameter makes the working directory reflect the new branch head.

### 3) Nothing is Ever Lost
What happened to the wrong commits? They are still in the repository. Actually, we can still refer to them. Let us take a look at all commits.  
![Screenshot 15.3](./screenshots/15.3.png)  
We can see that the wrong commits are not gone. They are not listed in the main branch anymore but still remain in the repository. They would still be in the repository if we did not tag them, but then we could reference them only by their hashes.

## 16. Removing the Oops Tag

### 1) Removal of the Oops Tag
The oops tag has performed its function. Let us remove that tag and permit the garbage collector to delete the referenced commit.  
![Screenshot 16.1](./screenshots/16.1.png)  
The oops tag will no longer appear in the repository.

## 17. Amending Commits

### 1) Change the Page and Commit
Put an author comment on the page.  
![Screenshot 17.1.1](./screenshots/17.1.1.png)  
![Screenshot 17.1.2](./screenshots/17.1.2.png)

### 2) Oops... Email Required
After making the commit, you understand that every good comment should include the author's email. Edit the `hello.html` page to provide an email.  
![Screenshot 17.2](./screenshots/17.2.png)

### 3) Change the Previous Commit
We do not want to create another commit for adding the email address. Let us change the previous commit and add an email address.  
![Screenshot 17.3](./screenshots/17.3.png)

### 4) View History
The new "author/email" commit replaces the original "author" commit. The same effect can be achieved by resetting the last commit in the branch and recommitting new changes.  
![Screenshot 17.4](./screenshots/17.4.png)

## 18. Creating a Branch

### 1) Create a Branch
It is time to make our page more stylish with a touch of CSS. We'll develop this feature in a new branch called `style`.  
![Screenshot 18.1](./screenshots/18.1.png)

### 2) Add the style.css File
![Screenshot 18.2.1](./screenshots/18.2.1.png)  
![Screenshot 18.2.2](./screenshots/18.2.2.png)

### 3) Change hello.html to Use style.css
![Screenshot 18.3.1](./screenshots/18.3.1.png)  
![Screenshot 18.3.2](./screenshots/18.3.2.png)

## 19. Switching Branches

Now our project has two branches.  
![Screenshot 19.0](./screenshots/19.0.png)

### 1) Switching to the Main Branch
To switch between branches, use the `git switch` command.  
![Screenshot 19.1](./screenshots/19.1.png)

### 2) Let Us Return to the Style Branch
We are back to the `style` branch. As you can see, our CSS-related changes are present.  
![Screenshot 19.2](./screenshots/19.2.png)

## 20. Moving Files

### 1) Examining the History of Changes in a Specific File
Let's take a look at the change log for the `hello.html` file before we proceed with renaming it.  
![Screenshot 20.1](./screenshots/20.1.png)

### 2) Comparing Different Versions of a Specific File
The `show` command is used to display the changes in a specific commit. Let's examine the changes in the `hello.html` file in the commit tagged with `v1`.  
![Screenshot 20.2](./screenshots/20.2.png)

### 3) Renaming hello.html
Let's proceed to rename our `hello.html` file to `index.html` using the standard `mv` command and observe the outcome.  
![Screenshot 20.3.1](./screenshots/20.3.1.png)  
Git interprets our modification as if we've deleted the file and created a new one. We need to inform Git that we've renamed the file, not deleted and created a new one.  
![Screenshot 20.3.2](./screenshots/20.3.2.png)

### 4) Safely Moving style.css
Let's move our `style.css` file to the `css` directory. This time, however, we'll use the `git mv` command to ensure the move is recorded in Git's history as a move, not as a deletion and addition of a new file.  
![Screenshot 20.4.1](./screenshots/20.4.1.png)  
Now, let's commit our changes and examine the change history of the `css/styles.css` file. To see the file's history prior to its relocation, we'll need to include the `--follow` option. Let's execute both versions of the command to understand the difference.  
![Screenshot 20.4.2](./screenshots/20.4.2.png)

## 21. Changes in the Main Branch

### 1) Commit the README File to the Main Branch
We are currently in the `style` branch. The `README` file is not part of this branch, so we must switch to the `main` branch before committing the changes.  
![Screenshot 21.1](./screenshots/21.1.png)

## 22. Viewing Diverging Branches

### 1) View Current Branches
We now have two diverging branches in the repository. Use the following log command to view the branches and how they diverge.  
![Screenshot 22.1](./screenshots/22.1.png)

## 23. Merging

### 1) Merge the Branches
Merging brings changes from two branches into one. Let us go back to the `style` branch and merge it with `main`.  
![Screenshot 23.1](./screenshots/23.1.png)

## 24. Creating a Merge Conflict

### 1) Switch Back to the Main and Create Conflict
In our `main` branch, the page is still called `hello.html`. Switch back to the `main` branch and make the following changes.  
![Screenshot 24.1.1](./screenshots/24.1.1.png)  
![Screenshot 24.1.2](./screenshots/24.1.2.png)

### 2) View Branches
After the "Added README" commit, the `main` branch has been merged with the `style` branch, but there is an additional `main` commit, which was not merged back to the `style` branch.  
![Screenshot 24.2](./screenshots/24.2.png)

## 25. Resolving Conflicts

### 1) Merge the Main Branch into the Style Branch
Let us return to the `style` branch and merge in all the recent changes from `main`.  
![Screenshot 25.1.1](./screenshots/25.1.1.png)  
It seems that we have a conflict. Let us see what Git has to say about it.  
![Screenshot 25.1.2](./screenshots/25.1.2.png)  
If you open the `index.html`, you will see.  
![Screenshot 25.1.3](./screenshots/25.1.3.png)  

### 2) Aborting Merge
Jumping straight to the conflict resolution may not be the best strategy. The conflict may be caused by changes you are unaware of, or the changes are too significant to address right away. For this reason, Git allows you to abort the merge and return to the state before the merge. To do that, you can use the `git merge --abort` command, as suggested by the status command we ran earlier.  
![Screenshot 25.2](./screenshots/25.2.png)  

### 3) Resolving the Conflict
After some meditation, we are ready to handle the conflict. Let us rerun the merge.  
![Screenshot 25.3](./screenshots/25.3.png)  

### 4) Commit the Resolved Conflict
Let us look at the current state of our repository and make sure that everything is okay.  
![Screenshot 25.4](./screenshots/25.4.png)

## 27. Resetting the Style Branch

### 1) Resetting the Style Branch
Let us go to the `style` branch to the point before we had merged it with the `main` branch. We can reset the branch to any commit. In fact, the `reset` command can change the branch pointer to point to any commit in the tree. Here, we want to go back in the `style` branch to a point before merging with the `main`. We have to find the last commit before the merge.  
![Screenshot 27.1.1](./screenshots/27.1.1.png)  
We can see from the output that the "Renamed hello.html; moved style.css" commit was the latest on the `style` branch prior to the first merging with `main`. Let us reset the `style` branch to this commit. To reference that commit, we either use its hash or deduce that this commit is 2 commits before the `HEAD`, or `HEAD~2` in Git notation.  
![Screenshot 27.1.2](./screenshots/27.1.2.png)  

### 2) Check the Branch
Now, let's check the log of the `style` branch. There should be no merge commits in the log.  
![Screenshot 27.2](./screenshots/27.2.png)

## 28. Rebase

### 1) Rebase the Style Branch onto Main
![Screenshot 28.1.1](./screenshots/28.1.1.png)  
Note that the conflict is in `hello.html`, not in `index.html` as the last time. It is because rebase was in the process of applying the style changes on top of the main branch. The file `hello.html` hasn't been renamed in `main` yet, so it still has its old name. When merging, we would have a "reverse" conflict. During the merge, the changes of the `main` branch are applied on top of the `style` branch. The `style` branch has the file renamed, so the conflict would be in `index.html`.  
![Screenshot 28.1.2](./screenshots/28.1.2.png)  

### 2) Resolve the Conflict
The conflict itself can be resolved in the same way we did before. First, we edit the `hello.html` file to meet our expectations. But after that, we don't need to commit the changes. We can just add the file to the index and continue the rebase process. This allows us to fix conflicts without creating a bunch of ugly merge commits. For simplicity's sake, we can add all files using `.` which stands for the path of the current directory. Git interprets this as "add all files in the current directory and its subdirectories".  
![Screenshot 28.2.1](./screenshots/28.2.1.png)  
Upon saving changes, Git will finish the rebase process, and we can proceed with the following commands.  
![Screenshot 28.2.2](./screenshots/28.2.2.png)


# Part II: Working with Multiple Repositories

## 30. Cloning Repositories

### 1) Go to Your Repositories Directory
At this point, you should be in your repositories directory. It should contain a single repository named `work`.  
![Screenshot 30.1](./screenshots/30.1.png)

### 2) Create a Clone of the Work Repository
Let's create a clone of the repository.  
![Screenshot 30.2](./screenshots/30.2.png)

## 31. Examine the Cloned Repository

### 1) Viewing the Cloned Repository
Let's have a look at our cloned repository.  
![Screenshot 31.1](./screenshots/31.1.png)  
We will see a list of all files in the top level of the original repository.

### 2) View the History of the Cloned Repository
We will see a list of all the commits in the new repository, and it should match the commit history of the original repository. The only difference should be in the names of the branches.  
![Screenshot 31.2](./screenshots/31.2.png)

## 32. What is Origin?

![Screenshot 32.1](./screenshots/32.1.png)  
We see that the cloned repository knows the default name of the remote repository. To get more information about origin, see below.  
![Screenshot 31.2](./screenshots/31.2.png)  
We can see that the origin of the remote repository is the original work repo. Remote repos are typically stored on a separate machine or a centralized server. However, as we see, they can also point to a repository on the same machine.

## 33. Remote Branches

Let's take a look at the branches in our cloned repository. ![Screenshot 33.0](./screenshots/33.0.png)  
As we can see, only the main branch is listed in it. The `git branch` command only lists the local branches by default.

### 1) List of the Remote Branches

To see all the branches, you need to use the following command. ![Screenshot 33.1](./screenshots/33.1.png)  
Git lists all the branches from the original repo, but the remote repository branches are not treated as local ones.

## 34. Changing the Original Repository

### 1) Make a Change in the Original Work Repository

![Screenshot 34.1.1](./screenshots/34.1.1.png)  
We are now in the work repository. Make the following changes to the README file.  
![Screenshot 34.1.2](./screenshots/34.1.2.png)  
Now add and commit this change.  
![Screenshot 34.1.3](./screenshots/34.1.3.png)

## 35. Fetching Changes

![Screenshot 35.0](./screenshots/35.0.png)  
We are now in the home repository.

### 1) Check the README

We can show that the cloned README file has not been changed.  
![Screenshot 35.1](./screenshots/35.1.png)  
No changes, as you can see.

## 36. Merging Pulled Changes

### 1) Merge the Pulled Changes into the Local Main Branch

![Screenshot 36.1](./screenshots/36.1.png)  

### 2) Check the README Again

Now we should see the changes.  
![Screenshot 36.2](./screenshots/36.2.png)  
These are the changes.

<h2>37. Adding a tracking branch</h2>
<h3>1) Add a local branch tracking the remote branch</h3>
<a href="screenshots/37.1.png">Screenshot 37.1</a> Now we can see the style branch in the branch list and log.

## 38. Bare Repos

### 1) Creating a Bare Repository

![Screenshot 38.1](./screenshots/38.1.png)  

Now we are in the repositories directory. The convention is that repositories ending in `.git` are bare repositories. We can see that there is no working directory in the `work.git` repo. Essentially, it is nothing but the `.git` directory of a regular repo.

## 39. Adding a Remote Repository

Let's add the `work.git` repository to our original repository. ![Screenshot 39.0](./screenshots/39.0.png)

## 40. Pushing Changes

Let’s start by creating a change to be pushed. Edit the README and commit it. 
![Screenshot 40.0.1](./screenshots/40.0.1.png) 
![Screenshot 40.0.2](./screenshots/40.0.2.png)

Now send changes to the shared repository. 
![Screenshot 40.0.3](./screenshots/40.0.3.png) 
The shared repository is the one receiving changes sent by us.

## 41. Pulling Shared Changes

Quickly switch to the home repository and pull the changes we just sent to the shared repository. 
![Screenshot 41.0.1](./screenshots/41.0.1.png)

Continue with... 
![Screenshot 41.0.2](./screenshots/41.0.2.png)

## 42. Hosting Your Git Repository

### 1) Launch the Git Server
![Screenshot 42.1.1](./screenshots/42.1.1.png)

Now, go to your repositories directory in a separate terminal window. 
![Screenshot 42.1.2](./screenshots/42.1.2.png)

You will find a copy of the work project.
