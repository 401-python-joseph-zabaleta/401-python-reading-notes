# Reading Prework - The Command Line  
This is a summary of a beginners guide to Linux command line (BASH). There are 14 parts to cover and below is the link to the article covering each in detail.

[Linux Tutorial for Beginners - Ryan Tutorials](https://ryanstutorials.net/linuxtutorial/)  

1. [The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)  
    - A command line or terminal is a text based interface to the system.  
    - You can issue commands and receive feedback.  
    - Opening terminal on Linux: Applications > System or Applications > Utilities  

2. [Basic Navigation](https://ryanstutorials.net/linuxtutorial/navigation.php)  
    - `pwd`: print working directory to find out where we are.  
    - `ls`: what is in our current directory, lists all files inside.  
    - Two types of Paths: Absolute or Relative
        - Absolute path: A file or directory location in relation to the root of the file system.  
        - Relative path: A file or directory location to where we currently are in the file system.  
        - `~`: shortcut for your home directory  
        - `.`: reference to your current directory  
        - `..`: reference to your parent directory  
    - `cd`: change directory, allows us to move around the files in our system.
        - Shortcut: if you use `cd` without and arguments this will bring you to your home directory  
        - Writing paths can be tedious. There is a mechanism called tab completion this lets you start a file name and press `tab` to finish it.  

3. [More About Files](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)  
    - Everything is a file. Even directories.  
    - Linux is an extensionless system: Unlike Windows, that uses extensions to determine the type of file. Linux looks inside the file to determine its file type.  
    - `file[path]`: This will tell you the type of file you are working with.  
    - Linux is most definitely case sensitive. FILE.txt is not the same as File.txt  
    - File names can have spaces but we have to treat them differently when working with them.  
        - Quotes: Changing to a file with a space in the name use `'name space'` quotes around them.  
        - Escape Characters: `\` this is used to escape the next character in the line of code, for us a space.  
    - Hidden files and Directories:
        - `ls` will list all our items in a given directory but hidden files remain hidden unless we pass ls an argument. 
        - `ls -a` list all , will show all files including hidden files.  

4. [Manual Pages](https://ryanstutorials.net/linuxtutorial/manual.php)  
    - Manuals are set of pages that explain every command available on your system and what they do.  
    - `man<command to look up>`: This will look up the documentation for a command.
    - Tip: to exit man pages press 'q' for quit.  
    - `man -k <search term>`: Its possible to search by a keyword with the `-k` argument.  
    - `/<term>`: When inside a manual you perform a search for a 'term'.  
    - `n`: After performing a search you can select the next found item with `n`.  
    - Remember we do not have to memorize anything we just need to be able to reference everything.  

5. [File Manipulation](https://ryanstutorials.net/linuxtutorial/filemanipulation.php)  
    - `mkdir[options]<directory>`: this command makes a new directory and has options if you choose.  
        - `mkdir -p`: tells mkdir to make parent directories as needed.  
        - `mkdir -v`: makes mkdir tell us what it is doing  
    - `rmdir[option]<directory>`: this command removes a directory if it is empty.  
    - `touch[option]<filename>`: Creates a new file. 
    - `cp[options]<source><destination>`: Copy a file from point a to point b.  
    - `mv[options]<source><destination>`: Move a file from point a to point b.  
        - mv can be used to rename a file: `mv file1 file2` this makes file1 now named file2.  
    - `rm[option]<file>`: rm or remove , to remove a file.  
    - there is the `r` option for removing directories or files. This is recursive, or will remove all files from directory down.  
    - NOTE: Linux is not forgiving: There is no undo feature.  

6. [Vi Text Editor](https://ryanstutorials.net/linuxtutorial/vi.php)  
    - Build int text editor accessed by using `vi<file>`. It has two modes "insert" and "edit".  
        - when you vi into a file you start off in edit mode. Press `i` to enter insert mode.  
        - When you are done inserting new lines of text press `esc` to return back to edit mode.  
    - Saving and exiting: as long as you are not in insert mode.  
        - `ZZ`: save and exit  
        - `:q!`: discard all changes, since last save, and exit  
        - `:w`: save file but don't exit  
        - `:wq`: save and exit  
    - Another way to view a file is using the `cat<file>` command. Which stands for concatenate. This prints the file in the terminal to read.  
    - For large or larger files use the command `less<file>`. This allows you to move up and down the page within a file using arrow keys. You can move forward a whole page using spacebar or back a page by pressing b. When you are done just press q for quit.  
    - NOTE: No mouse, Vi editor is text and key input based.  

7. [Wildcards](https://ryanstutorials.net/linuxtutorial/wildcards.php)  
    - Are a set of building blocks that allow you to create a pattern defining a set of files or directories.  
    - Here is the basic set of wildcards:  
        - `*`: represents zero or more characters  
        - `?`: represents a single character  
        - `[]`: represents a range of characters  
    - Great reference to look up is regex or regular expressions.  

8. [Permissions](https://ryanstutorials.net/linuxtutorial/permissions.php)  
    - Permissions allow users to do three actions on a file:  
        - `r` read: you may view a contents of a file.  
        - `w` write: you may change the contents of the file.  
        - `x` execute: you may execute or run the file if it is a program or script.  
    - For every file there is a set that people belong to:
        - `owner`: A single person who owns the file.  
        - `group`: every file belongs to a single group.  
        - `others`: everyone else who is not in the group or the owner.  
    - `ls -l[path]`: To view the permission for a file.
    - `ls -ld`: View the permissions for a specific directory.  
        - first 10 characters of the output covers the the permissions.  
        - 1st character is the file type  
        - next 3 are owner permissions  
        - next 3 are group permissions  
        - last 3 are other permissions  
    - `chmod[permissions][path]`: To change permissions on a file.  

9. [Filters](https://ryanstutorials.net/linuxtutorial/filters.php)  
    - Filters are used to transform data in a particular way. It can take raw data, data stored in files, and manipulate it to be displayed in a way more desired view.  
    - `cat somefile.txt` might display 100 lines of text and we only want the first few lines.  
        - Use `head` filter, `head somefile.txt` by default will show first 10 lines, but we can change it more if we chooose.  
        - `tail` is the same but from the bottom of the file up.  
    - `sort somefile.txt`: will sort the data by default alphabetically.  
    - `nl`: number lines, will print n-th number of lines in a file.  
    - `wc`: word count, will do just that, count words.  
    - `cut`: Great if you need to seperate columns out of a files.  
    - `sed`: Stream editor, allows us to search and replace on our data.
    - `uniq`: unique, can remove duplciates from a file.  
    - `tac`: its cat in reverse on purpose. It does the opposite of cat and prints last line to first line.  

10. [Grep and Regular Expressions](https://ryanstutorials.net/linuxtutorial/grep.php)  
    - `egrep` is a program that searches a given set of data and prints every line that matches a given pattern.  
    - `egrep[command line options]<pattern>[path]`
    - This requires a lot of practice with regex and is a powerful way to identify pieces of information and manipulate data.  

11. [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)  
    - Every program we run on the command line has three data streams:  
        - STDIN(0), STDOUT(1), and STDERR(2)  
    - Normally we get our outputs in the terminal but we can redirect them to a file to save, send or review.  
    - NOTE: When piping and redirecting, the actual data will always be the same, but formatting of that data may be slightly different to what is normally printed to the screen.  
    - Commands:  
        - `>` save output to a file  
        - `>>` append output to a file  
        - `<` Read input from a file.  
        - `2>` Redirect error messages  
        - `|` Send the output from one program as input to another program  
    
12. [Process Management](https://ryanstutorials.net/linuxtutorial/processes.php)  
    - This is how we control and manage a program. A program is a series of instructions to tell the computer what to do.  
    - Linux like most modern OS's is a multitasking operating system.  
    - `top`: gives us a snap shotof what is currently happening on the system.
    - `ps`: Is another command that stands for processes.  
    - Sometimes programs crash and browsers freeze up and we need to end that process with `kill[signal]<PID>`  
    - CONTROL: WE have quite a bit of control over the running of our programs.  
    - NOTE: Normal users may only kill processes which they are the owner for. The root user on the system may kill anyones processes.  


13. [Bash Scripting](https://ryanstutorials.net/linuxtutorial/scripting.php)  
    - There is a whole tutorial dedicated to scripting: [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/)  
    - Bash script in computing terms is similiar to a script in a theatrical terms. Its a document with a list of things to do.  
    - Allows us to define a series of actions to do without us inputing the commands.  
    - Interpreter is used to read and act on the bash script.  
    - `echo<message>` This is a simple bash script example.  
    - In our scripts the first line defines the interpreter to use.  
    - NOTE: Bash is picky about formatting. Ensure spaces are where they are needed and not put when they are not required.  

14. [Cheatsheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)  
    - This is a great reference sheet. It covers the main concepts of the terminal and has a small description of what each command does. Something good to look at from time to time and remember that "Oh I have manual pages!" might be good tool over Google.  

