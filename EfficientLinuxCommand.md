Source: Efficient Linux at the Command Line: https://www.oreilly.com/library/view/efficient-linux-at/9781098113391/       
## Part I. Core Concepts
! 1. Combining Commands   
  
    $ ls -l /bin                   # list a large directory---------------------------------
    $ less myfile                  # displays a file one screenful at a time
    $ ls -l /bin | less            # Use a pipe to send the output of ls to the input of less

<img width="308" alt="image" src="https://user-images.githubusercontent.com/105786517/218336990-3991db00-b13a-4694-b3cd-15cc7128cbb4.png"><img width="350" alt="image" src="https://user-images.githubusercontent.com/105786517/218336909-ddb5b396-1480-4c80-b937-8493ccf148b9.png">

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
  
    $ work=$HOME/Projects
    
    
    page 23
  
  
  
  
  
  
  
  
  
  
  
  3. Rerunning Commands
  4. Cruising the Filesystem
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


























