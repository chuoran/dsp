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

> >
  ```
  pwd
  mkdir
  rmdir
  touch xyz.py
  rm xyz.py
  mv xyz zyx
  ls -a    
  cp xyz.py ../zyx    
  ```


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

> > 

  ls: list folders and files in the current directory
  ls -a: list all folders and files in current directory, including hidden files starting with .
  ls -l: list in long format, with details of file mode, number of links, owner name, bytes in the file, date and time the file was last modified, etc.
  ls -lh: list in long format, with unit suffixes.
  ls -lah: list all files/folders, including hidden ones, in long format, with unit suffixes.
  ls -t: list and sort by time modified, with most recent ones first.
  ls -Glp: list in colored format, long format, and adding a "/" after folders


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -a
    ls -R
    ls -G
    ls -u
    ls -t

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs will supply a list of argument to a command (utility?) one by one, so the command could be executed multiple times, each time with one argument from the xargs. It's like looping through the arguments and perform the utility on each one.

The following example copies all python script files in the DataScience folder to another folder

```bash
find ~/DataScience/ -iname "*.py" -print |xargs -I {} cp {} ~/DataScience/Metis/PyFiles/
```
 

