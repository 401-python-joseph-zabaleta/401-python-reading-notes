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




