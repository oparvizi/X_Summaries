Source: Efficient Linux at the Command Line: https://www.oreilly.com/library/view/efficient-linux-at/9781098113391/       
## Part I. Core Concepts
  1. Combining Commands   
  
    $ ls -l /bin                   # list a large directory---------------------------------              
    $ less myfile                  # displays a file one screenful at a time       
    $ ls -l /bin | less            # Use a pipe to send the output of ls to the input of less             

<img width="308" alt="image" src="https://user-images.githubusercontent.com/105786517/218336990-3991db00-b13a-4694-b3cd-15cc7128cbb4.png">

    $ man wc                       # display full documentation-----------------------------
    $ wc animals.txt               # prints the number of lines, words, and characters in a file
    $ wc -l animals.txt
    $ wc -w animals.txt
    $ wc -c animals.txt

    $ ls -1
    $ ls -1 | wc -l                # How many files are visible in my current directory?
    $ wc animals.txt | wc -w | wc


    $ ls /bin                     # ls Changes Its Behavior When Redirected
    $ ls /bin | cat               #
    $ ls                          #
    $ ls | wc -l                  #
    
    $ head -n3 animals.txt                # Print the first three lines---------------------- 
    $ head -n3 animals.txt | wc -w        # Count the number of words in the first three lines
    $ ls /bin | head -n5                  # list the first five filenames in the /bin directory
    
    $ cut -f2 animals.txt                 # print all book titles from animals.txt, which appear in the second column 
    $ cut -f2 animals.txt | head -n3      # pipe it to head to print only the first three lines
    $ cut -f1,3 animals.txt | head -n3    # cut multiple fields
    $ cut -f2-4 animals.txt | head -n3    # Or by numeric range
    $ cut -c1-3 animals.txt               # Print the first three characters from each line of the file
    $ cut -f4 animals.txt | cut -d, -f1   # isolate the authors’ lastnames--------------------

    $ grep Nutshell animals.txt           # displays lines from animals.txt that contain the string Nutshell
    $ grep -v Nutshell animals.txt        # print lines that don’t match a given string, with the -v option
    $ grep Perl *.txt                     # useful for finding files
    $ ls -l /usr/lib
    $ ls -l /usr/lib | cut -c1            # marks directories with a d at the beginning   
    # $ ls -l /usr/lib | cut -c1 | grep d   # keep only the lines containing d
    $ ls -l /usr/lib | cut -c1 | grep d | wc -l   # contains 145 subdirectories--------------

    $ sort animals.txt                    # reorders the lines of a file into ascending order
    $ sort -r animals.txt                 # or descending order
    $ cut -f3 animals.txt
    $ cut -f3 animals.txt | sort -n
    $ cut -f3 animals.txt | sort -nr
    $ cut -f3 animals.txt | sort -nr | head -n1
                      ... | sort -nr | head -n1   # print the maximum value by piping the data
                      ... | sort -n | head -n1    # print the minimum value
   
    $ head -n5 /etc/passwd                        # generate a list of users
    $ head -n5 /etc/passwd | cut -d: -f1          # isolate the usernames
    $ head -n5 /etc/passwd | cut -d: -f1 | sort
    $ cat /etc/passwd | cut -d: -f1 | sort          # generate a list of all user
    $ cut -d: -f1 /etc/passwd | grep -w jones       # username matched or not 

    $ uniq letters                         #------------------------------------------------- 
    $ uniq -c letters                      # uniqe and count occurrences
    $ cut -f1 grades | sort
    $ cut -f1 grades | sort | uniq -c | sort -nr
    $ cut -f1 grades | sort | uniq -c | sort -nr | head -n1
    $ cut -f1 grades | sort | uniq -c | sort -nr | head -n1 | cut -c9
    
    $ md5sum image001.jpg                  # Detecting Duplicate Files-----------------------
    $ md5sum image001.jpg image002.jpg image003.jpg
    $ md5sum *.jpg | cut -c1-32 | sort
    $ md5sum *.jpg | cut -c1-32 | sort | uniq -c
    $ md5sum *.jpg | cut -c1-32 | sort | uniq -c | sort -nr
    $ md5sum *.jpg | cut -c1-32 | sort | uniq -c | sort -nr | grep -v " 1 "
    $ md5sum *.jpg | grep 146b163929b6533f02e91bdf21cb9563
    $ md5sum *.jpg | grep 146b163929b6533f02e91bdf21cb9563 | cut -c35-
  
  2. Introducing the Shell
     
    $ ls *.py
    $ ls data.py main.py user_interface.py
    
   Pattern Matching for Filenames
    
    $ grep Linux chapter*
    $ grep Linux chapter?
    $ grep Linux chapter??
    $ grep Linux chapter[12345]
    $ grep Linux chapter[1-5]
    $ grep Linux chapter*[02468]
    
    $ ls -1 /etc/*.conf                    # list all files in the directory /etc with names ending in .conf using a pattern
    $ cd P*
    $ ls *.doc
  Evaluating Variables
  
    $ printenv HOME                        # print the values of HOME and USER on stdout
    $ printenv USER
    $ echo My name is $USER and my files are in $HOME           # Evaluating variables
    $ echo ch*ter9                                              # Evaluating a pattern
  Where Variables Come From
  
    $ work=$HOME/Projects                              # assign directory /home/smith/Projects name to a variable
    $ cd $work
    $ pwd
    $ cp myfile $work
    $ ls $work
  When defining a variable, no spaces are permitted around the equals sign.
    $ work = $HOME/Projects The shell assumes "work" is a command
    work: command not found
  
  Variables and Superstition

    $ echo $HOME                                        # print the value of a variable with echo
    $ echo /home/smith                                  # you might think that the echo command examines the HOME variable and prints its value. That is not the case. echo knows nothing about variables. It just prints whatever arguments you hand it.
  Patterns Versus Variables
   
    $ ls
    $ ls mammals
      mv mammals/*.txt reptiles          method-1                # files should be moved to the subdirectory
         $ echo mammals/*.txt
         $ mv mammals/lizard.txt mammals/snake.txt reptiles
      
      FILES="lizard.txt snake.txt"       method-2
      mv mammals/$FILES reptiles
        $ echo mammals/$FILES
        $ mv mammals/lizard.txt snake.txt reptiles
        $ mv mammals/$FILES reptiles
   
    FILES="lizard.txt snake.txt"                                  # use a for loop that prepends the directory name mammals to each filename
    for f in $FILES; do
    mv mammals/$f reptiles
    done
  Shortening Commands with Aliases   
    
    $ alias g=grep                                                 # A command with no arguments
    $ alias ll="ls -l"                                             # A command with arguments: quotes are required
    $ ll                                                           # Runs "ls -l"
    $ g Nutshell animals.txt                                       # Runs "grep Nutshell animals.txt"
    $ alias less="less -c"                                         # define an alias that has the same name as an existing command, effectively replacing that command in your shell. This practice is called shadowing the command.
    $ alias
    $ alias g
    $ unalias g
Redirecting Input and Output   
    
    $ grep Perl animals.txt                                         # command writes to stdout by default
    $ grep Perl animals.txt > outfile               (displays no output)
    $ cat outfile
    
    $ grep Perl animals.txt > outfile                Create or overwrite outfile
    $ echo There was just one match >> outfile       Append to outfile
    $ cat outfile
    $ wc animals.txt                                 Reading from a named file
    $ wc < animals.txt                               Reading from redirected stdin
Standard Error (stderr) and Redirection
   
    $ cp nonexistent.txt file.txt                                    # produces this error message
    $ cp nonexistent.txt file.txt > errors
    $ cat errors
    
    $ cp nonexistent.txt file.txt 2> errors
    $ cat errors
    
    $ cp nonexistent.txt file.txt 2> errors
    $ cp another.txt file.txt 2>> errors
    $ cat errors
    
    $ echo This file exists > goodfile.txt              Create a file
    $ cat goodfile.txt nonexistent.txt &> all.output
    $ cat all.output
    
    $ wc < animals.txt > count
    $ cat count
    
    $ grep Perl < animals.txt | wc > count
    $ cat count
Disabling Evaluation with Quotes and Escapes
    
    $ cat Efficient Linux Tips.txt                                    # command may fail because the shell treats the space characters as separators
    $ cat 'Efficient Linux Tips.txt'                                  # force the shell to treat spaces as part of a filename, you have three options—single quotes, double quotes, and backslashes
    $ cat "Efficient Linux Tips.txt"
    $ cat Efficient\ Linux\ Tips.txt
    
    $ echo '$HOME'
    $ echo "Notice that $HOME is evaluated"
    $ echo 'Notice that $HOME is not'
    
    $ echo \$HOME
    $ echo "The value of \$HOME is $HOME"
    $ echo 'The value of \$HOME is $HOME'
    $ echo "This message is \"sort of\" interesting"
    $ echo "This is a very long message that needs to extend \
    onto multiple lines"
    
    $ cut -f1 grades \                                                # Final backslashes are great for making pipelines
    | sort \
    | uniq -c \
    | sort -nr \
    | head -n1 \
    | cut -c9
    
    $ alias less="less -c"                              Define an alias
    $ less myfile                                       Run the alias, which invokes less -c
    $ \less myfile                                      Run the standard less command, not the alias
Locating Programs to Be Run   
    
    $ ls -l /bin/ls
    $ echo $PATH                                                       # The list is stored as the value of the shell variable PATH
    $ echo $PATH | tr : "\n"                                           # translates one character into another

    $ which cp                                                         # locate a program in your search path
    $ which which
    
    $ type cp                                                          # type command, a shell builtin that also locates aliases, functions, and shell builtins
    $ type ll
    $ type type
 Environments and Initialization Files, the Short Version  
    
    $ ls $HOME
    $ ls -a $HOME
    
    # Set the search path                                              # Here is a sample .bashrc file
    PATH=$HOME/bin:/usr/local/bin:/usr/bin:/bin
    # Set the shell prompt
    PS1='$ '
    # Set your preferred text editor
    EDITOR=emacs
    # Start in my work directory
    cd $HOME/Work/Projects
    # Define an alias
    alias g=grep
    # Offer a hearty greeting
    echo "Welcome to Linux, friend!"
  3. Rerunning Commands
  Viewing the Command History
  
    $ md5sum *.jpg | cut -c1-32 | sort | uniq -c | sort -nr            # Detecting Duplicate Files
    $ history
    $ history 3                                                        # Print the 3 most recent commands
    $ history | less                                                   # Earliest to latest entry
    $ history | sort -nr | less                                        # Latest to earliest entry
    $ history | grep -w cd                                             # print only the historical commands containing the word cd
    $ history -c                                                       # To clear (delete) the history for the current shell, use the -c option
  Recalling Commands from the History
   Cursoring Through History
    
    $ echo $HISTSIZE
    $ HISTSIZE=10000
    $ HISTCONTROL=ignoredups
    $ echo $HISTFILE
    $ echo $HISTFILESIZE
    $ HISTFILESIZE=10000
  History Expansion  
    
    $ echo Efficient Linux
    $ !!
    $ !grep
    $ !?grep?
    $ history | grep hosts
    $ !1203
    $ history
    $ !-3
    $ !-3:p
    $ ls -l /etc | head -n3
    $ echo "!!" | wc -w
  Never Delete the Wrong File Again (Thanks to History Expansion)  
    
    $ ls
    $ rm * .txt                                                         # DANGER!! Don't run this! Deletes the wrong files!
        $ ls *.txt                # Verify
        $ head myfile.txt
        $ rm !$                   # Delete
        
        $ ls *.txt *.o *.log
        $ rm !*
 Incremental Search of Command History    
    
    (reverse-i-search)`':                                               # prompt changes to indicate an incremental search
    (reverse-i-search)`': c                                             # Start typing the desired command. For example, type c
    (reverse-i-search)`': less /etc/hosts                               # The shell displays its most recent command that contains the string c, highlighting what you’ve typed: Type the next letter, d:
    (reverse-i-search)`': cd
    (reverse-i-search)`': cd /usr/local                                 # The shell displays its most recent command that contains the string cd, again highlighting what you’ve typed
    (reverse-i-search)`': cd $                                          # Continue typing the command, adding a space and a dollar sign
Command-Line Editing:   
  To fix mistakes, To create a command piece by piece, To construct a new command based on a previous one from your command history
(a key skill for building up complex pipelines):
    - Cursoring: Again, the slowest and least powerful method but simple to learn
    - Caret notation: A form of history expansion
    - Emacs- or Vim-style keystrokes: To edit the command line in powerful ways
    
Cursoring Within a Command   
     
    Keystroke-------------Action
    Left arrow            Move left by one character
    Right arrow           Move right by one character
    Ctrl + left arrow     Move left by one word
    Ctrl + right arrow    Move right by one word
    Home                  Move to beginning of command line
    End                   Move to end of command line
    Backspace             Delete one character before the cursor
    Delete                Delete one character beneath the cursor
History Expansion with Carets 
  
    $ md5sum *.jg | cut -c1-32 | sort | uniq -c | sort -nr
    $ ^jg^jpg
    $ !!:s/jg/jpg/
    $ !md5sum:s/jg/jpg/
Emacs- or Vim-Style Command-Line Editing    
    
    Action------------------------------------------------------------------Emacs-----------Vim
    Move forward by one character                                           Ctrl-f          h 
    Move backward by one character                                          Ctrl-b          l
    Move forward by one word                                                Meta-f          w
    Move backward by one word                                               Meta-b          b
    Move to beginning of line                                               Ctrl-a          0
    Move to end of line                                                     Ctrl-e          $
    Transpose (swap) two characters                                         Ctrl-t          xp
    Transpose (swap) two words                                              Meta-t          n/a
    Capitalize first letter of next word                                    Meta-c          w~
    Uppercase entire next word                                              Meta-u          n/a
    Lowercase entire next word                                              Meta-l          n/a
    Change case of the current character                                    n/a             ~
    Insert the next character verbatim, including control characters        Ctrl-v          Ctrl-v
    Delete forward by one character                                         Ctrl-d          x
    Delete backward by one character Backspace or                           Ctrl-h          X
    Cut forward by one word                                                 Meta-d          dw
    Cut backward by one word Meta-Backspace or                              Ctrl-w          db
    Cut from cursor to beginning of line                                    Ctrl-u          d^
    Cut from cursor to end of line                                          Ctrl-k          D
    Delete the entire line                                                  Ctrl-e Ctrl-u   dd
    Paste (yank) the most recently deleted text                             Ctrl-y          p
    Paste (yank) the next deleted text (after a previous yank)              Meta-y          n/a
    Undo the previous editing operation                                     Ctrl-_          u
    Undo all edits made so far                                              Meta-r          U
    Switch from insertion mode to command mode                              n/a             Escape
    Switch from command mode to insertion mode                              n/a             i
    Abort an edit operation in progress                                     Ctrl-g          n/a
    Clear the display                                                       Ctrl-l          Ctrl-l
  4. Cruising the Filesystem

    $ cd /usr/share/lib/etc/bin
    $ pwd
    $ cd $HOME/Work
    $ cd ~/Work
    $ echo $HOME ~
    $ echo ~jones
    $ cd /usr
    $ cd sha<Tab>                                           # visit the subdirectory share.de
    
    $ cd share/
    $ cd s<Tab>
    $ cd s<Tab><Tab>
    $ cd sh<Tab>
    $ cd share/
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    





## Part II. Next-Level Skills 
  5. Expanding Your Too
  6. Parents, Children, and Environments
  7. More Ways to Run a Command
  8. Building a Brash One-Liner  
  9. Leveraging Text Files
## Part III. Extra Goodies
  10. Efficiency at the Keyboard
  11. Final Time-Savers

A. Linux Refresher
B. If You Use a Different Shell
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    

Source: Linux in a Nutshell, 6th Edition https://www.oreilly.com/library/view/linux-in-a/9780596806088/       
## Introduction
System and Network Administration Overview
Linux Commands
Boot Methods
Package Management
The Bash Shell
Pattern Matching
The Emacs Editor
The vi, ex, and vim Editors
The sed Editor
The gawk Programming Language
Source Code Management: An Overview
The Subversion Version Control System
The Git Version Control System
Virtualization Command-Line Tools


























