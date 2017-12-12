# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

pwd = show current working directory.  
mkdir = make a directory.  
rm -r = delete a directory.  
touch "file name" = creates a file inside of the working directory.  
rm = deletes a file.  
mv CurrentFileName.txt NewFileName.txt = rename a file.  
ls -a = lists all files including hidden files.  
cp SourceDirectory/SourceFile DestinationDirectory/ = copy a file from one directory to another.  
sort = sorts alphabetically.  
uniq = removes duplicates.  
cat = outputs the contents of a file to the terminal.  
> = redirects the std output into a file. Rewrites the file.  
>> = redirects the std output into a file.  Appends to the file.  
grep -l = searches for lines that match a pattern and returns the results. -l means not case sensitive.  
grep -R = outputs file names and lines containing materials searched.  
sed = find and replace.  sed s/_ 1/_ 2/g with g will replace all instances of 1 with 2. without g, only the first instance.  

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

ls = list the files in the working directory.  
ls -a = list the files in the working directory including the hidden files.  
ls -l = list the long form of the files in the working directory.  
ls -lh = lists both the long form and the sizes in a readable format.  
ls -lah = lists files and hidden files in long format and their sizes in a readable format.  
ls -t = lists the files sorted by the time they were last modified.  
ls -GLp = lists long form files without the group names and with a slash after the child directories.  


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

ls -d = displays only directories.  
ls -u = displays files by file access time.  
ls -L = displays the file or directory referenced by a sybolic link.  
ls -m = displays the file names as a comman separated list.  
ls -q = displays all nonprinting characters as ?.  


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

The xargs command converts input from standard input into arguments in a command.


Example: $xargs  
Hello world  
* if I then press ctrl+D to tell xargs I am done the output will be.*  
Hello world  

This is because the defaut command that xargs will excecute.  

an example of xargs using a different command:  
$ xargs find -name  
*.txt  
the function would then output all files ending in .txt  
 

