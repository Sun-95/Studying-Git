**2. Creating a project**
1) Create a “Hello, World!” page
Get started in an empty directory (for example, repositories, if you downloaded the file from the previous step) and add an empty subdirectory named work, then create a hello.html file in it with the following contents.
[screenshots/2.1.png ]
Run
mkdir work
cd work
touch hello.html
File: hello.html
Hello, World!
02Create a repository
So you have a directory that contains one file. Run git init in order to create a Git repo from that directory.

Run
git init
Result
Initialized empty Git repository in /home/alex/githowto/repositories/work/.git/
03Add the page to the repository
Now let's add the “Hello, World” page to the repository.

Run
git add hello.html
git commit -m "Initial Commit"
You will see:

Result
$ git add hello.html
$ git commit -m "Initial commit"
[main (root-commit) 5836970] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 hello.html
